<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Primera Página Web</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f2f2f2;
            color: #333;
        }

        header {
            background-color: #6a1b9a;
            color: #fff;
            padding: 20px;
            text-align: center;
        }

        header img {
            max-width: 100%;
            height: auto;
            border-radius: 15px;
        }

        nav {
            background-color: #8e24aa;
            padding: 10px;
            text-align: right;
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
            justify-content: flex-end;
        }

        nav ul li {
            margin: 0 15px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
            font-size: 16px;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: #ffeb3b;
        }

        main {
            padding: 20px;
            background-color: #ffffff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            margin: 20px;
        }

        section {
            margin-bottom: 20px;
            padding: 20px;
            background-color: #f8bbd0;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        section h2 {
            color: #6a1b9a;
        }

        footer {
            background-color: #6a1b9a;
            color: #fff;
            text-align: center;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        footer p {
            margin: 0;
        }

        /* Estilos adicionales para el eslogan */
        #inicio h1 {
            font-size: 2.5em;
            color: #8e24aa;
            margin-bottom: 20px;
        }

        #inicio p {
            font-size: 1.2em;
            color: #555;
        }

        /* Estilos para el carrusel */
        .carousel-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin: auto;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .carousel-slide {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }

        .carousel-slide img {
            width: 100%;
            border-radius: 10px;
        }

        .carousel-quote {
            text-align: center;
            font-style: italic;
            margin-top: 10px;
            color: #6a1b9a;
        }

        .carousel-quote p {
            margin: 5px 0;
        }

        .prev,
        .next {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background-color: rgba(0, 0, 0, 0.5);
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            border-radius: 50%;
        }

        .prev {
            left: 10px;
        }

        .next {
            right: 10px;
        }

        /* Estilos para el formulario de contacto */
        .contact-form {
            background-color: #f8bbd0; /* Color rosa pastel */
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .contact-form label {
            font-family: 'Arial', sans-serif;
            color: #333;
            display: block;
            margin: 10px 0 5px;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-bottom: 15px;
        }

        .contact-form button {
            background-color: #6a1b9a; /* Color morado */
            color: white; /* Letras en blanco */
            border: none;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            font-size: 16px;
        }

        .contact-form button:hover {
            background-color: #8e24aa; /* Color morado más claro al pasar el mouse */
        }
    </style>
    <script>
        let slideIndex = 0;

        function showSlides(n) {
            let slides = document.getElementsByClassName("carousel-slide")[0];
            let totalSlides = slides.children.length;

            slideIndex += n;
            if (slideIndex >= totalSlides) {
                slideIndex = 0;
            } else if (slideIndex < 0) {
                slideIndex = totalSlides - 1;
            }

            slides.style.transform = "translateX(" + (-slideIndex * 100) + "%)";
        }

        function mostrarSeccion(id) {
            const secciones = document.querySelectorAll('section');
            secciones.forEach(seccion => {
                seccion.style.display = 'none';
            });
            document.getElementById(id).style.display = 'block';
        }

        document.addEventListener('DOMContentLoaded', () => {
            mostrarSeccion('inicio'); // Mostrar la sección de inicio por defecto
        });
    </script>
</head>

<body>
    <header>
        <img src="https://markmorrisdancegroup.org/wp-content/uploads/2019/05/The_Seattle-2015_Mat-Hayward-099-resize.jpg" alt="Banner de la Página Web">
        <h1>Bienvenido a Mi Página Web</h1>
    </header>

    <nav>
        <ul>
            <li><a href="javascript:void(0)" onclick="mostrarSeccion('inicio')">Inicio</a></li>
            <li><a href="javascript:void(0)" onclick="mostrarSeccion('nosotros')">Nosotros</a></li>
            <li><a href="javascript:void(0)" onclick="mostrarSeccion('productos')">Productos</a></li>
            <li><a href="javascript:void(0)" onclick="mostrarSeccion('contacto')">Contacto</a></li>
        </ul>
    </nav>

    <main>
        <section id="inicio">
            <h1>Sana tu mente, danza conmigo</h1>
            <p>En Studio Etéreo, transformamos la pasión por la danza en una experiencia inolvidable. Nos especializamos en desarrollar el talento y la creatividad de cada estudiante, ofreciéndote un ambiente acogedor y profesional donde cada movimiento es un paso hacia tu bienestar físico y emocional. ¡Únete a nosotros y descubre el poder transformador de la danza!</p>
        </section>

        <section id="nosotros">
            <h2>Acerca de Nosotros</h2>
            <p>Somos una empresa dedicada a brindar experiencias únicas relacionadas estrechamente con la expresión y el movimiento. Damos clases de Contempo, Jazz, Lírico, ballet y urbano.</p>
            <h3>Misión:</h3>
            <p>Ofrecer una formación de excelencia y calidad, formando con valores y responsabilidad emocional, permitiendo y educando bajo la autodisciplina con profesionales que despierten el interés del educado sobre este arte expresivo. Una formación basada en el desarrollo de las capacidades con enfoque profesional.</p>
            <h3>Visión:</h3>
            <p>Studio Etéreo busca el reconocimiento por su calidad en formación artística y emocional, creando profesionales. Siendo una academia de libre expresión, creatividad y multidisciplinaria. Nuestro ideal es dar la oportunidad de formación a personas con bajos recursos para tomar la danza como alternativa de educación y formación.</p>
        </section>
        <section id="productos">
            <h2>Nuestros Productos</h2>
            <div class="carousel-container">
                <div class="carousel-slide">
                    <div class="carousel-item">
                        <img src="https://cdn.pixabay.com/photo/2023/11/14/20/08/woman-8388428_1280.jpg" alt="Danza">
                        <div class="carousel-quote">
                            <p>"La danza es el lenguaje oculto del alma."</p>
                            <p>- Martha Graham, 1937</p>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <img src="https://cdn.pixabay.com/photo/2020/06/20/16/32/dance-5321562_1280.jpg" alt="Bailar">
                        <div class="carousel-quote">
                            <p>"Bailar es soñar con los pies."</p>
                            <p>- Constanze Mozart, 1777</p>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <img src="https://cdn.pixabay.com/photo/2016/12/30/10/03/dance-1940245_1280.jpg" alt="Danza Poesía">
                        <div class="carousel-quote">
                            <p>"La danza es la poesía de los pies."</p>
                            <p>- John Dryden, 1682</p>
                        </div>
                    </div>
                </div>
                <button class="prev" onclick="showSlides(-1)">&#10094;</button>
                <button class="next" onclick="showSlides(1)">&#10095;</button>
            </div>
        </section>
        
        <style>
            .carousel-container {
                position: relative;
                width: 80%;
                margin: auto;
                overflow: hidden;
                border: 1px solid #ddd;
            }
        
            .carousel-slide {
                display: flex;
                transition: transform 0.5s ease;
            }
        
            .carousel-item {
                min-width: 100%;
                box-sizing: border-box;
                text-align: center;
            }
        
            .carousel-quote {
                margin-top: 10px;
            }
        
            .prev, .next {
                position: absolute;
                top: 50%;
                width: auto;
                padding: 16px;
                color: white;
                background-color: rgba(0, 0, 0, 0.5);
                border: none;
                cursor: pointer;
                transform: translateY(-50%);
            }
        
            .prev {
                left: 10px;
            }
        
            .next {
                right: 10px;
            }
        </style>
        
        <script>
            let slideIndex = 0;
            showSlides(slideIndex);
        
            function showSlides(n) {
                const slides = document.querySelectorAll('.carousel-item');
                slideIndex += n;
        
                if (slideIndex >= slides.length) {
                    slideIndex = 0; // Vuelve al principio
                }
                if (slideIndex < 0) {
                    slideIndex = slides.length - 1; // Vuelve al final
                }
        
                slides.forEach((slide, index) => {
                    slide.style.display = (index === slideIndex) ? 'block' : 'none';
                });
            }
        </script>        

        <section id="contacto">
            <h2>Contacto</h2>
            <p>Puedes contactarnos en nuestro correo electrónico: studioetero@gmail.com</p>
            <p>Número de contacto: 3196031681</p>
            
            <div style="background-color: #f8bbd0; padding: 20px; border-radius: 10px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);">
                <h3>Encuesta de Contacto</h3>
                <form>
                    <label for="nombre" style="font-family: 'Arial', sans-serif; color: #333;">Nombre:</label><br>
                    <input type="text" id="nombre" name="nombre" style="width: 100%; padding: 10px; margin-bottom: 10px; border-radius: 5px; border: 1px solid #ccc;"><br>
        
                    <label for="email" style="font-family: 'Arial', sans-serif; color: #333;">Correo Electrónico:</label><br>
                    <input type="email" id="email" name="email" style="width: 100%; padding: 10px; margin-bottom: 10px; border-radius: 5px; border: 1px solid #ccc;"><br>
        
                    <label for="asunto" style="font-family: 'Arial', sans-serif; color: #333;">Asunto:</label><br>
                    <input type="text" id="asunto" name="asunto" style="width: 100%; padding: 10px; margin-bottom: 10px; border-radius: 5px; border: 1px solid #ccc;"><br>
        
                    <label for="mensaje" style="font-family: 'Arial', sans-serif; color: #333;">Mensaje:</label><br>
                    <textarea id="mensaje" name="mensaje" rows="4" style="width: 100%; padding: 10px; margin-bottom: 10px; border-radius: 5px; border: 1px solid #ccc;"></textarea><br>
        
                    <button type="submit" style="background-color: #6a1b9a; color: #fff; padding: 10px 15px; border: none; border-radius: 5px; cursor: pointer;">Enviar Datos</button>
                </form>
            </div>
        </section>

    </main>

    <footer>
        <p>© 2024 Studio Etéreo. Todos los derechos reservados.</p>
    </footer>
</body>

</html>
