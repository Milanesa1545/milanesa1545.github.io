<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pagina web de SpaceMc</title>
</head>
<body>
    <header>
        <h1>Bienvenido a Mi Página Web</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#">Inicio</a></li>
            <li><a href="#">Acerca de</a></li>
            <li><a href="#">Enlaces</a></li>
            <li><a href="#">Contacto</a></li>
        </ul>
    </nav>
    <main>
        <section>
            <h2>Acerca de Nosotros</h2>
            <p>Somos una Comunidad de Discord.</p>
        </section>
        <section>
            <h2>Nuestros Enlaces de interes</h2>
            <ul>
                <li>Enlaces de interes</li>
                <li>discord https://discord.gg/EDnfSHZEep</li>
                <li>X https://twitter.com/SpaceMc_Java</li>
            </ul>
        </section>
    </main>
    <footer>
        <p>&copy; Contacta con el Owner Milanesa1521SpaceMc@gmail.com
        /* Estilos generales */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f5f5f5;
}

header {
    background-color: #333;
    color: #fff;
    padding: 20px 0;
}

nav ul {
    list-style: none;
    text-align: center;
}

nav li {
    display: inline;
    margin-right: 20px;
}

nav a {
    text-decoration: none;
    color: #fff;
}

main {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
}

section {
    margin-bottom: 30px;
}

h1, h2 {
    color: #333;
}

/* Estilos específicos */
#hero {
    background-image: url('hero-image.jpg');
    background-size: cover;
    text-align: center;
    padding: 200px 0;
    color: #fff;
}

#hero h1 {
    font-size: 36px;
}

#hero p {
    font-size: 18px;
}

.cta-button {
    display: inline-block;
    padding: 15px 30px;
    background-color: #ff5722;
    color: #fff;
    text-decoration: none;
    border-radius: 5px;
    font-weight: bold;
    font-size: 16px;
}

#about, #services {
    background-color: #fff;
    padding: 20px;
    border-radius: 5px;
}

footer {
    text-align: center;
    padding: 10px 0;
    background-color: #333;
    color: #fff;
}

