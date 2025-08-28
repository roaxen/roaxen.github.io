<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Redirigir a YouTube</title>
</head>
<body style="display:flex; justify-content:center; align-items:center; height:100vh; background:#222; color:white; flex-direction:column; font-family:sans-serif;">

  <h2>Escribe un nombre y dale a enviar</h2>
  
  <input type="text" id="nombre" placeholder="Tu nombre aquí" style="padding:10px; width:250px; border-radius:8px; border:none;"/>
  
  <button onclick="enviar()" style="margin-top:15px; padding:10px 20px; border:none; border-radius:8px; background:#ff4747; color:white; font-weight:bold; cursor:pointer;">
    Enviar
  </button>

  <script>
    function enviar() {
      const nombre = document.getElementById("nombre").value.trim();
      if(nombre){
        // 👉 aquí puedes cambiar la URL de destino
        window.location.href = "https://www.youtube.com/results?search_query=" + encodeURIComponent(nombre);
      } else {
        alert("Por favor, escribe un nombre antes de enviar.");
      }
    }
  </script>
</body>
</html>
