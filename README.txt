<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Encuesta de Satisfacción del Parque Tecnológico</title>
    <link rel="stylesheet" href="public/vendor/bootstrap/bootstrap-5/css/bootstrap.min.css">
    <link rel="stylesheet" href="public/css/style.css">
</head>
<body>

    <header class="bg-primary text-white p-4">
        <h1 class="display-4">Encuesta del Parque Tecnológico</h1>
        [span_0](start_span)<p class="lead">¡Tu opinión impulsa la innovación y la naturaleza[span_0](end_span)!</p>
    </header>

    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item"><a class="nav-link" href="#">Inicio</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Encuestas</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Resultados</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Contacto</a></li>
            </ul>
        </div>
    </nav>

    <div class="container my-5">
        <div class="row">

            <main class="col-lg-8">
                <h2 class="mb-4">Formulario de Satisfacción</h2>

                <form action="#" method="post">
                    <fieldset class="border p-3 mb-4">
                        <legend class="float-none w-auto px-2">Datos Personales</legend>

                        <div class="mb-3">
                            <label for="nombreCompleto" class="form-label">Nombre completo:</label>
                            <input type="text" class="form-control" id="nombreCompleto" name="nombreCompleto"
                                required
                                pattern="[A-Za-ZÁÉÍÓÚáéíóúÑñ ]+"
                                [span_1](start_span)title="Solo letras y espacios.[span_1](end_span)"
                                aria-describedby="nombreHelp">
                            <div id="nombreHelp" class="form-text">Por favor, evite usar números o caracteres especiales.</div>
                        </div>

                        <div class="mb-3">
                            <label for="email" class="form-label">Correo electrónico:</label>
                            <input type="email" class="form-control" id="email" name="email" required>
                        </div>

                        <div class="mb-3">
                            <label for="edad" class="form-label">Edad:</label>
                            <input type="number" class="form-control" id="edad" name="edad"
                                min="10" max="100" required>
                        </div>
                    </fieldset>

                    <fieldset class="border p-3 mb-4">
                        <legend class="float-none w-auto px-2">Opinión General</legend>

                        <div class="mb-3">
                            <label for="satisfaccion" class="form-label">Nivel de satisfacción (1=Malo a 10=Excelente):</label>
                            <input type="range" class="form-range" id="satisfaccion" name="satisfaccion"
                                min="1" max="10" step="1" value="5">
                        </div>

                        <div class="mb-3">
                            <label for="progreso" class="form-label">Satisfacción simulada:</label>
                            <progress id="progreso" max="100" value="70">70%</progress>
                        </div>

                        <div class="mb-3">
                            <label for="fechaVisita" class="form-label">Fecha de la visita:</label>
                            <input type="date" class="form-control" id="fechaVisita" name="fechaVisita" required>
                        </div>

                        <div class="mb-3">
                            <label for="horaLlegada" class="form-label">Hora de llegada:</label>
                            <input type="time" class="form-control" id="horaLlegada" name="horaLlegada" required>
                        </div>

                        <div class="mb-3">
                            <p>¿Qué te gustó más? [span_2](start_span)<small>(Selecciona al menos uno)</small>[span_2](end_span)</p>
                            <div class="form-check form-check-inline">
                                <input class="form-check-input" type="checkbox" id="checkTec" name="gusto[]" value="Tecnologia" required>
                                <label class="form-check-label" for="checkTec">Tecnología</label>
                            </div>
                            <div class="form-check form-check-inline">
                                <input class="form-check-input" type="checkbox" id="checkNat" name="gusto[]" value="Naturaleza">
                                <label class="form-check-label" for="checkNat">Naturaleza</label>
                            </div>
                            <div class="form-check form-check-inline">
                                <input class="form-check-input" type="checkbox" id="checkAct" name="gusto[]" value="Actividades">
                                <label class="form-check-label" for="checkAct">Actividades</label>
                            </div>
                        </div>

                        <div class="mb-3">
                            <p>¿Recomendarías el parque? [span_3](start_span)<small>(Selecciona uno)</small>[span_3](end_span)</p>
                            <div class="form-check form-check-inline">
                                <input class="form-check-input" type="radio" id="radioSi" name="recomienda" value="si" required>
                                <label class="form-check-label" for="radioSi">Sí</label>
                            </div>
                            <div class="form-check form-check-inline">
                                <input class="form-check-input" type="radio" id="radioNo" name="recomienda" value="no">
                                <label class="form-check-label" for="radioNo">No</label>
                            </div>
                            <div class="form-check form-check-inline">
                                <input class="form-check-input" type="radio" id="radioQuizas" name="recomienda" value="quizas">
                                <label class="form-check-label" for="radioQuizas">Quizás</label>
                            </div>
                        </div>
                    </fieldset>

                    <fieldset class="border p-3 mb-4">
                        <legend class="float-none w-auto px-2">Sugerencias</legend>

                        <div class="mb-3">
                            <label for="comentario" class="form-label">Comentario (máx. 200 caracteres):</label>
                            <textarea class="form-control" id="comentario" name="comentario"
                                maxlength="200"
                                [span_4](start_span)[span_5](start_span)placeholder="Escribe tu opinión o sugerencias para mejorar la experiencia...[span_4](end_span)[span_5](end_span)"
                                rows="3"></textarea>
                        </div>

                        <div class="mb-3">
                            <label for="codigoVerificacion" class="form-label">Código de verificación (6 dígitos):</label>
                            <input type="text" class="form-control" id="codigoVerificacion" name="codigoVerificacion"
                                required
                                pattern="\d{6}"
                                [span_6](start_span)[span_7](start_span)title="Debe contener exactamente 6 números.[span_6](end_span)[span_7](end_span)">
                        </div>
                    </fieldset>

                    <div class="d-grid gap-2 d-md-block">
                        <button type="submit" class="btn btn-success me-2">Enviar encuesta</button>
                        <button type="reset" class="btn btn-secondary">Borrar todo</button>
                    </div>
                </form>

                <hr class="my-5">

                <details class="alert alert-info">
                    <summary>Reglas de Privacidad del Formulario</summary>
                    <p>La información recopilada en esta encuesta es confidencial y se utilizará únicamente con el fin de mejorar los servicios e instalaciones del Parque Tecnológico. No compartiremos sus datos personales con terceros.</p>
                </details>
            </main>

            <aside class="col-lg-4">
                <h3 class="mt-4 mt-lg-0">Conoce el Parque</h3>
                <figure class="figure">
                    <img src="placeholder-parque.jpg" class="figure-img img-fluid rounded" alt="Vista del Parque Tecnológico.">
                    <figcaption class="figure-caption text-end">Una vista de nuestras instalaciones de innovación.</figcaption>
                </figure>

                <div class="mt-4">
                    <p>Mensaje de Agradecimiento:</p>
                    <audio controls>
                        <source src="public/media/gracias-por-participar.mp3" type="audio/mp3">
                        Tu navegador no soporta el elemento de audio.
                    </audio>
                </div>

            </aside>
        </div>
    </div>

    <footer class="bg-dark text-white text-center p-3 mt-5">
        <p>&copy; 2025 Derechos reservados. | <a href="#" class="text-white">Contacto</a></p>
    </footer>

    <script src="public/vendor/bootstrap/bootstrap-5/js/bootstrap.bundle.min.js"></script>
    <script src="public/js/script.js"></script>
</body>
</html>
