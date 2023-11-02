    }

    repositories {
        maven {
            name = "comugamersRepository"
            credentials(PasswordCredentials::class)

            url = if (project.version.toString().contains("-SNAPSHOT")) {
                uri("https://repo.comugamers.com/repository/maven-snapshots/")
            } else {
                uri("https://repo.comugamers.com/repository/maven-releases/")
            }
        }
    }
}

tasks {
    java {
        toolchain {
            languageVersion.set(JavaLanguageVersion.of(8))
        }
    }

    withType<JavaCompile>().configureEach {
        options.encoding = "UTF-8"
    }

    compileJava {
        options.compilerArgs.add("-parameters")
    }

    getByName<Test>("test") {
        useJUnitPlatform()
    }

    named("build") {
        dependsOn(named("shadowJar"))
    }

    withType<ShadowJar> {
        val pkg = "com.comugamers.sentey.internal"
        val version = project.version.toString()

        relocate("dev.triumphteam.cmd", "$pkg.triumphteam.cmd")
        relocate("org.apache.http", "$pkg.apache.http")
        relocate("org.apache.commons.logging", "$pkg.apache.commons.logging")
        relocate("org.apache.commons.codec", "$pkg.apache.commons.codec")
        relocate("javax.inject", "$pkg.javax.inject")
        relocate("team.unnamed.inject", "$pkg.trew")
        relocate("org.bstats", "$pkg.bstats")

        archiveFileName.set("sentey-$version.jar")
    }
}

bukkit {
    main = "com.comugamers.sentey.Sentey"
    apiVersion = "1.13"
    version = "${project.version}"
    authors = listOf("Pabszito", "Jojo1545")
    description = "${findProperty("plugin-description")}"
    name = "${findProperty("plugin-name")}"
    website = "www.comugamers.com"
    softDepend = listOf("CG-Core")
}
