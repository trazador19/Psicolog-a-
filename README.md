!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Psicología, Salud y Creatividad</title>
  <style>
    body {
      background-color: #e8f5e9; /* Verde suave de fondo */
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      margin: 0;
      padding: 20px;
      background-image: url('https://www.transparenttextures.com/patterns/ashlar.png');
    }
    h1 {
      color: #81c784; /* Verde menta */
      text-align: center;
      margin-bottom: 10px;
      font-size: 2.5em;
    }
    h2 {
      color: #66bb6a; /* Verde oscuro */
      text-align: center;
      margin-bottom: 30px;
      font-size: 1.5em;
    }
    p {
      text-align: center;
      font-size: 1.2em;
      color: #333;
    }
    .subtitle {
      font-size: 1.3em;
      color: #66bb6a;
      margin-top: 10px;
      font-weight: bold;
    }
    .icon {
      font-size: 2em;
      margin: 5px;
      color: #66bb6a;
    }
    form {
      background-color: #ffffff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
      max-width: 400px;
      width: 100%;
      margin-bottom: 20px;
      border-left: 5px solid #81c784;
    }
    label, select, button {
      display: block;
      width: 100%;
      margin-bottom: 15px;
      font-size: 16px;
    }
    button {
      background-color: #81c784; /* Verde menta */
      color: white;
      border: none;
      padding: 10px;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #66bb6a; /* Verde más oscuro para hover */
    }
    #resultado {
      background-color: #ffffff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
      max-width: 600px;
      width: 100%;
      margin-top: 20px;
    }
    .contact-info {
      font-size: 1.2em;
      color: #333;
      text-align: center;
    }
    .contact-info a {
      color: #66bb6a;
      text-decoration: none;
    }
    .contact-info a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <h1>Psicología, Salud y Creatividad</h1>
  <h2>Algo creativo</h2>
  <p class="subtitle">Psicólogo Enrique Ávila Torres</p>

  <form id="formulario">
    <label for="servicio">Selecciona el tipo de atención:</label>
    <select id="servicio" name="servicio" required>
      <option value="">-- Elige una opción --</option>
      <option value="rezago">Detección de causas de rezago estudiantil</option>
      <option value="orientacion_general">Orientación educativa general e integral</option>
      <option value="vocacional">Orientación vocacional</option>
      <option value="platicas">Solicitud de pláticas de atención psicológica</option>
      <option value="psicologica">Orientación psicológica</option>
    </select>

    <button type="submit">Enviar</button>
  </form>

  <div id="resultado"></div>

  <div class="contact-info">
    <p>Para más información, contáctame:</p>
    <p>📞 <a href="tel:+524921718862">4921718862</a></p>
    <p>📧 <a href="mailto:e.torres.18.av@gmail.com">e.torres.18.av@gmail.com</a></p>
  </div>

  <script>
    const formulario = document.getElementById('formulario');
    const resultado = document.getElementById('resultado');

    formulario.addEventListener('submit', function(event) {
      event.preventDefault();
      
      const servicio = document.getElementById('servicio').value;

      let contenido = "";

      switch(servicio) {
        case "rezago":
          contenido = `
            <h2>Detección de causas de rezago estudiantil</h2>
            <p>Evaluación de factores académicos, emocionales y sociales que afectan el rendimiento escolar. Se aplica una entrevista diagnóstica y pruebas psicopedagógicas.</p>
            <p><strong>Costo por sesión:</strong> $400 MXN</p>
          `;
          break;
        case "orientacion_general":
          contenido = `
            <h2>Orientación educativa general e integral</h2>
            <p>Asesoría personalizada para mejorar técnicas de estudio, organización del tiempo, autoestima académica y resolución de conflictos escolares. Basado en experiencias en CEBARE y Centros Educativos de Zacatecas.</p>
            <p><strong>Costo por sesión:</strong> $350 MXN</p>
          `;
          break;
        case "vocacional":
          contenido = `
            <h2>Orientación vocacional</h2>
            <p>Evaluación de intereses, habilidades y valores para la elección de carrera o área de especialización. Basado en instrumentos psicométricos y entrevistas vocacionales.</p>
            <p><strong>Costo por sesión:</strong> $450 MXN</p>
          `;
          break;
        case "platicas":
          contenido = `
            <h2>Solicitud de pláticas de atención psicológica</h2>
            <p>Pláticas grupales sobre autoestima, manejo emocional, prevención de adicciones y habilidades socioemocionales, dirigidas a estudiantes, padres y docentes. Experiencia en CIJ, escuelas y comunidades rurales.</p>
            <p><strong>Costo por evento:</strong> Desde $1,000 MXN (dependiendo del número de asistentes)</p>
          `;
          break;
        case "psicologica":
          contenido = `
            <h2>Orientación psicológica</h2>
            <p>Atención breve individualizada enfocada en la identificación y resolución de problemáticas emocionales o conductuales. Ideal para adolescentes y jóvenes.</p>
            <p><strong>Costo por sesión:</strong> $400 MXN</p>
          `;
          break;
        default:
          contenido = `<p>Por favor selecciona un servicio.</p>`;
      }

      resultado.innerHTML = contenido;
    });
  </script>

</body>
</html
