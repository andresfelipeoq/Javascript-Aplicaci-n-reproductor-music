# Javascript-Aplicaci-n-reproductor-music

Crear un reproductor de música en JavaScript requiere una combinación de HTML, CSS y JavaScript. A continuación, te proporciono un ejemplo básico de cómo crear un reproductor de música simple:

1. **HTML**:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Reproductor de Música</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
    <h1>Reproductor de Música</h1>
    <audio id="music-player" controls>
        <source src="tu_cancion.mp3" type="audio/mpeg">
        Tu navegador no soporta la reproducción de audio.
    </audio>
    <script src="script.js"></script>
</body>
</html>
```

2. **CSS** (Guárdalo en un archivo llamado `styles.css`):

```css
body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #f9f9f9;
}

h1 {
    color: #333;
}
```

3. **JavaScript** (Guárdalo en un archivo llamado `script.js`):

```javascript
document.addEventListener('DOMContentLoaded', function () {
    const musicPlayer = document.getElementById('music-player');

    musicPlayer.addEventListener('play', function () {
        console.log('Reproduciendo música');
    });

    musicPlayer.addEventListener('pause', function () {
        console.log('Pausa en la reproducción de música');
    });

    musicPlayer.addEventListener('ended', function () {
        console.log('Música finalizada');
    });
});
```

Este es un reproductor de música simple que utiliza el elemento `audio` de HTML5. Puedes personalizarlo incluyendo tu canción en el atributo `src` del elemento `source`. También, hemos agregado algunos eventos JavaScript para mostrar mensajes en la consola cuando comienza la reproducción, se pausa o la canción termina.

Puedes expandir este reproductor de música incorporando más características, como controles personalizados, lista de reproducción, temporizador, etc. Para una experiencia más completa, considera el uso de bibliotecas de reproductores de música en JavaScript como `Howler.js` o `jPlayer`. Estas bibliotecas proporcionan una funcionalidad más avanzada y una mejor experiencia de usuario.
