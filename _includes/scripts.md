<section id="scripting">
    <script id="cambiaTitolo">

      var parole = [
      'weird',
      'gallery', 
      '...'
      ]

      var ii = 0;
      function cambiaTitolo() {
          document.querySelector("#title").innerHTML = parole[ii];
          if (ii < parole.length -1) {
              ii = ii + 1;
          } else {
              ii = 0;
          }
      }
      setInterval(cambiaTitolo, 3000);

    </script>
      
    <script id="changeMenuStatus">

        //selettore div del menu "ultimo progetto"
        menu1 = document.getElementById('menù_actual');
        menu2 = document.getElementById('menù_previous')
        
        //aggiorna stato menu se si clicca su "previous"
        function updateMenuStatus() {
            if (menu1.classList.contains("visible")) {
                menu1.classList.remove('visible');
                menu1.classList.add('hidden');
                menu2.classList.remove('hidden');
                menu2.classList.add('visible');
            } else {
                menu1.classList.remove('hidden');
                menu1.classList.add('visible');
                menu2.classList.add('hidden');
                menu2.classList.remove('visible');
            }
        }
        
    </script>

    <!-- https://www.youtube.com/watch?v=dc4zyX6DuOc
    <script src="https://cdnjs.cloudflare.com/ajax/libs/parallax/3.1.0/parallax.min.js"></script>
    <script>
        var scene = document.getElementById('scene');
        var parallaxInstance = new Parallax(scene);
    </script>
    -->

    <!-- old
    <script src='https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js'></script>
    <script  src="assets/parallax.js"></script>
    -->

</section>

