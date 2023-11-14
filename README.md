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



##Essa parte de baixo e o CSS##

@import url('https://fonts.googleapis.com/css2?family=Kdam+Thmor+Pro&family=Open+Sans:wght@300;400&display=swap');

    * {
      margin: 0;
      padding: 0;
      font-family: 'Open Sans', sans-serif;
    }

    body {
      height: 100vh;
      background: linear-gradient(120deg, #3bc7ffc0, #253bffda);
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0; /* Remove a margem padrão do corpo */
    }

    h2 {
      color: #fff;
      text-align: center;
    }

    .relogio {
      display: flex;
      align-items: center;
      justify-content: space-around;
      height: 200px;
      width: 550px;
      background: transparent;
      border-radius: 3px;
      box-shadow: 0px 8px 10px rgba(0, 0, 0, .5);
    }

    .relogio div {
      height: 170px;
      width: 150px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      color: #fff;
      background: rgba(5, 5, 5, .9);
      box-shadow: 5px 5px 15px rgba(0, 0, 0, .7);
      border: 7px;
      }
