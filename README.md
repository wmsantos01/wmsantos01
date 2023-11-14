# Esse e o meu primeiro projeto#
# Um relógio digital feito em HTML, CSS e javascript#
<!doctype html>
<html lang="pt-br"> 
 <head> 
  <meta charset="UTF-8"> 
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
  <title>Relogio Digital 2 </title> 
 </head> 
 <body> 
  <div class="relogio"> 
   <div> <span id="horas">00</span> <span class="tempo">Horas</span> 
   </div> 
   <div> <span id="minutos">00</span> <span class="tempo">Minutos</span> 
   </div> 
   <div> <span id="segundos">00</span> <span class="tempo">Minutos</span> 
   </div> 
  </div> 
  <script>
  function atualizarRelogio() {
    var agora = new Date();
    var horas = agora.getHours().toString().padStart(2, '0');
    var minutos = agora.getMinutes().toString().padStart(2, '0');
    var segundos = agora.getSeconds().toString().padStart(2, '0');

    document.getElementById('horas').innerText = horas;
    document.getElementById('minutos').innerText = minutos;
    document.getElementById('segundos').innerText = segundos;
  }

  setInterval(atualizarRelogio, 1000); // Atualiza a cada segundo
</script> 
 </body>
</html>
