<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Saito es un tontín</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f9;
      text-align: center;
      padding: 50px;
    }
    #output {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
    }
    button {
      margin: 10px;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      background-color: #4CAF50;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>
  <h1>Saito es un tontín</h1>
  <p id="question">Saito es un tontin?:</p>
  <button onclick="preguntar('si')">Sí</button>
  <button onclick="preguntar('no')">No</button>

  <div id="output"></div>

  <script>
    let etapa = 0; // 0 = pregunta principal, 1 = repetir

    function preguntar(opcion) {
      const output = document.getElementById("output");
      const question = document.getElementById("question");

      if (etapa === 0) { // Pregunta principal
        if (opcion === "si") {
          output.innerText = "Si es super duper mega tontin, no cabe duda de que es el mas tontin entre tontines, osea imaginate que hagan una pagina web para decirte tontin";
        } else if (opcion === "no") {
          output.innerText = "Pues igual sigue siendo un tontin!!!!!!";
        } else {
          output.innerText = "Pensaste que decir otra cosa haria que dejara de ser un tontin?!?!?!?!";
        }
        // Pasar a la etapa de repetir
        question.innerText = "Decirle tontin de nuevo? (si/no):";
        etapa = 1;
      } else if (etapa === 1) { // Pregunta de repetir
        if (opcion === "si") {
          output.innerText = "Bien hecho!!!! Sin duda es el mayor tontin que existe";
        } else if (opcion === "no") {
          output.innerText = "ERROR!!!!!!! Sigue siendo un tontin";
        } else {
          output.innerText = "Buen intento pero todos sabemos que sigue siendo un tontin";
        }
        // Volver a la pregunta principal
        question.innerText = "Saito es un tontin?:";
        etapa = 0;
      }
    }
  </script>
</body>
</html>
