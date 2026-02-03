# Puedo-volver-a-ser-tu-novia-
Petición 
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pregunta</title>
<style>
  body {
    margin: 0;
    height: 100vh;
    background: #faf7f4;
    font-family: 'Georgia', serif;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .contenedor {
    text-align: center;
    position: relative;
    width: 100%;
    max-width: 360px;
    padding: 20px;
  }
  .pregunta {
    font-size: 24px;
    margin-bottom: 50px;
    color: #3a3a3a;
  }
  .boton {
    font-size: 20px;
    padding: 14px 28px;
    border-radius: 30px;
    border: none;
    margin: 10px;
  }
  .si {
    background: #d9ebe3;
    color: #2f4f4f;
  }
  .no {
    background: #f2cccc;
    color: #6b2e2e;
    position: absolute;
    left: 50%;
    top: 60%;
    transform: translate(-50%, -50%);
    transition: transform 0.4s ease;
  }
  .mensaje-final {
    margin-top: 40px;
    font-size: 22px;
    color: #5a2d2d;
    opacity: 0;
    transition: opacity 1.5s ease;
  }
  .mostrar {
    opacity: 1;
  }
</style>
</head>
<body>

<div class="contenedor">
  <div class="pregunta">¿Puedo volver a ser tu novia?</div>

  <button class="boton si" id="si">Sí</button>
  <button class="boton no" id="no">No</button>

  <div class="mensaje-final" id="mensaje">Te amo tanto</div>
</div>

<script>
  const noBtn = document.getElementById("no");
  const siBtn = document.getElementById("si");
  const mensaje = document.getElementById("mensaje");

  function moverNo() {
    const contenedor = document.querySelector(".contenedor");
    const maxX = contenedor.offsetWidth - noBtn.offsetWidth;
    const maxY = contenedor.offsetHeight - noBtn.offsetHeight;
    const x = Math.random() * maxX;
    const y = Math.random() * maxY;
    noBtn.style.transform = `translate(${x - maxX/2}px, ${y - maxY/2}px)`;
  }

  noBtn.addEventListener("touchstart", moverNo);
  noBtn.addEventListener("mouseover", moverNo);

  siBtn.addEventListener("click", () => {
    mensaje.classList.add("mostrar");
  });
</script>

</body>
</html>
