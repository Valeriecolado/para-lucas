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

/* styles.css */
body {
    font-family: 'Lato', sans-serif;
    background-color: #fff0f5;
    color: #333;
    margin: 0;
    padding: 0;
}

header {
    text-align: center;
    padding: 2rem;
    background-color: #ffe4e1;
}

header h1 {
    font-family: 'Dancing Script', cursive;
    color: #ff69b4;
}

nav ul {
    display: flex;
    justify-content: center;
    list-style-type: none;
    padding: 0;
}

nav ul li {
    margin: 0 1rem;
}

nav ul li a {
    text-decoration: none;
    color: #ff69b4;
    font-weight: bold;
}

section {
    padding: 2rem;
    text-align: center;
}

section h2 {
    font-family: 'Great Vibes', cursive;
    color: #ff69b4;
    margin-bottom: 1rem;
}

footer {
    text-align: center;
    padding: 1rem;
    background-color: #ffe4e1;
    color: #ff69b4;
}

textarea {
    width: 80%;
    height: 100px;
    margin-bottom: 1rem;
}

button {
    background-color: #ff69b4;
    color: white;
    border: none;
    padding: 0.5rem 1rem;
    cursor: pointer;
}

button:hover {
    background-color: #ff1493;
}
// script.js

// Ejemplo de reacción con botones
document.addEventListener('DOMContentLoaded', function() {
    const notas = document.querySelector('.notas');
    const fotos = document.querySelector('.fotos');
    const canciones = document.querySelector('.canciones');
    const poemas = document.querySelector('.poemas');

    // Añadir una nota
    const nuevaNota = document.createElement('div');
    nuevaNota.classList.add('nota');
    nuevaNota.innerHTML = `
        <p>Te amo más cada día.</p>
        <button class="reaccion">❤️</button>
    `;
    notas.appendChild(nuevaNota);

    // Añadir una foto
    const nuevaFoto = document.createElement('div');
    nuevaFoto.classList.add('foto');
    nuevaFoto.innerHTML = `
        <img src="tu-foto.jpg" alt="Nosotros">
        <button class="reaccion">❤️</button>
    `;
    fotos.appendChild(nuevaFoto);

    // Añadir una canción
    const nuevaCancion = document.createElement('div');
    nuevaCancion.classList.add('cancion');
    nuevaCancion.innerHTML = `
        <a href="tu-cancion.mp3" target="_blank">Nuestra Canción</a>
        <button class="reaccion">❤️</button>
    `;
    canciones.appendChild(nuevaCancion);

    // Añadir un poema
    const nuevoPoema = document.createElement('div');
    nuevoPoema.classList.add('poema');
    nuevoPoema.innerHTML = `
        <p>Rosas son rojas, violetas son azules, mi amor por ti, nunca se reduce.</p>
        <button class="reaccion">❤️</button>
    `;
    poemas.appendChild(nuevoPoema);

    // Añadir evento a los botones de reacción
    document.querySelectorAll('.reaccion').forEach(button => {
        button.addEventListener('click', function() {
            alert('¡Gracias por tu reacción!');
        });
    });

    // Manejar el envío del formulario
    document.getElementById('respuestaForm').addEventListener('submit', function(e) {
        e.preventDefault();
        const noteContent = e.target.querySelector('textarea').value;
        if (noteContent) {
            alert(`Tu respuesta: "${noteContent}" ha sido enviada.`);
            e.target.reset();
        } else {
            alert('Por favor, escribe algo antes de enviar.');
        }
    });
});
