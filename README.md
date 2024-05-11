# javascr
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Photo Gallery</title>
    <style>
        body {
            margin: 2%;
            border: 1px solid black;
            background-color: #b3b3b3;
        }

        #image {
            line-height: 650px;
            width: 575px;
            height: 650px;
            border: 5px solid black;
            margin: 0 auto;
            background-color: #8e68ff;
            background-image: url('');
            background-repeat: no-repeat;
            color: #FFFFFF;
            text-align: center;
            background-size: 100%;
            margin-bottom: 25px;
            font-size: 150%;
        }

        .preview {
            width: 10%;
            margin-left: 17%;
            border: 10px solid black;
        }

        img {
            width: 95%;
        }
    </style>
</head>

<body>

    <div id="image">
        Hover over an image below to display here.
    </div>

    <img class="preview" alt="Carrera de invierno" src="https://intro-webdesign.com/v3/images/xmasraceb.jpg"
        onmouseover="upDate(this)" onmouseout="unDo()">

    <img class="preview" alt="Campamento Michigania" src="https://intro-webdesign.com/v3/images/camp2b.jpg"
        onmouseover="upDate(this)" onmouseout="unDo()">

    <img class="preview" src="https://intro-webdesign.com/v3/images/disneyb.jpg" alt="disney" onmouseover="upDate(this)"
        onmouseout="unDo()">

    <img class="preview" src="https://intro-webdesign.com/v3/images/trib.jpg" alt="Triatlón" onmouseover="upDate(this)"
        onmouseout="unDo()">

    <img class="preview" src="https://intro-webdesign.com/v3/images/raceb.jpg" alt="carrera de barro"
        onmouseover="upDate(this)" onmouseout="unDo()">

    <img class="preview" src="https://intro-webdesign.com/v3/images/dqb.jpg" alt="pleta de hielo"
        onmouseover="upDate(this)" onmouseout="unDo()">

    <script>
        function upDate(previewPic) {
            var imageDiv = document.getElementById('image');
            imageDiv.style.backgroundImage = "url('" + previewPic.src + "')";
            imageDiv.style.border = "2px solid red"; // Establecer un borde rojo
            imageDiv.style.color = "black"; // Establecer el color del texto en azul
            imageDiv.innerHTML = previewPic.alt; // Cambiar el texto del div al texto alternativo de la imagen previa
        }

        function unDo() {
            var imageDiv = document.getElementById('image');
            imageDiv.style.backgroundImage = "url('')"; // Restaurar la URL de la imagen de fondo a una cadena vacía
            imageDiv.style.border = "none"; // Restaurar el borde a ninguno
            imageDiv.style.color = "black"; // Restaurar el color del texto a negro
            imageDiv.innerHTML = "Hover over an image below to display here."; // Restaurar el texto del div al texto original
        }
    </script>

</body>

</html>
