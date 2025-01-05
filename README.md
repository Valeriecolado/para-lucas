<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Amor</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Bienvenido, Mi Amor</h1>
        <p>Un poema romántico que lo introduzca a la experiencia.</p>
    </header>
    <nav>
        <ul>
            <li><a href="#cartitas">Cartitas Diarias</a></li>
            <li><a href="#galeria">Galería de Fotos</a></li>
            <li><a href="#musica">Música</a></li>
            <li><a href="#poemas">Poemas</a></li>
            <li><a href="#formulario">Responde</a></li>
        </ul>
    </nav>
    <main>
        <section id="cartitas">
            <h2>Cartitas Diarias</h2>
            <div class="notas">
                <!-- Aquí irán las notas diarias -->
            </div>
        </section>
        <section id="galeria">
            <h2>Galería de Fotos</h2>
            <div class="fotos">
                <!-- Aquí irán las fotos -->
            </div>
        </section>
        <section id="musica">
            <h2>Música</h2>
            <div class="canciones">
                <!-- Aquí irán los enlaces a canciones -->
            </div>
        </section>
        <section id="poemas">
            <h2>Poemas</h2>
            <div class="poemas">
                <!-- Aquí irán los poemas -->
            </div>
        </section>
        <section id="formulario">
            <h2>Responder a mis notas</h2>
            <form id="respuestaForm">
                <textarea placeholder="Escribe algo bonito..."></textarea>
                <button type="submit">Enviar</button>
            </form>
        </section>
    </main>
    <footer>
        <p>Con todo mi amor, tuyo siempre.</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
