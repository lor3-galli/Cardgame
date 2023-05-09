Cardgame
![image](https://github.com/lor3-galli/Cardgame/assets/124684053/adcf5fcc-d129-4ae1-b85d-fe4c1195efd0)


Cardgame is a game, in which the aim is to find the same cards in pairs, until you get to have turned them all over, when the two cards turned over are not equal, they are turned over and you have another attempt.
![image](https://github.com/lor3-galli/Cardgame/assets/124684053/792f8fdf-d317-4808-9aba-d8dff4dcd604)


<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        img {
            width: 100px;
        }
    </style>
</head>

<body>

    <div id="tavoloDaGioco"></div>

    <script>
    let NcarteGirate = 0
    let primaCartGirata = null
    let carte = ["11-2314.jpg", "News9268.jpg", "yu8.jpg", "Cartapokemon.jpg", "11-2312.jpg", "carte-yu-gi-oh.jpg", "49-1463.jpg", "886001659_L.jpg", "12-219.jpg", "s-l225.jpg", "s-l300.jpg", "104.jpg", "Yu-Gi-Oh-Carte-Mago.jpg", "140.jpg", "11-2319.jpg", "12.jpg", "1234.jpg", "60.jpg", "11-2312.jpg", "886001659_L.jpg", "Yu-Gi-Oh-Carte-Mago.jpg", "carte-yu-gi-oh.jpg", "11-2314.jpg", "Cartapokemon.jpg", "12-219.jpg", "News9268.jpg", "49-1463.jpg", "12.jpg", "s-l225.jpg", "s-l300.jpg", "yu8.jpg", "140.jpg", "60.jpg", "104.jpg", "1234.jpg", "11-2319.jpg"]
    let tavolo = document.querySelector('#tavoloDaGioco')
        carte.forEach(element => {
            tavolo.innerHTML += '<img id="'+element+'" src="yugiohretro.jpg" onclick="gira(this)" />'
            console.log('<img id="'+element+'" src="yugiohretro.jpg" />')
        });

        function gira(carta) {
         NcarteGirate++
         carta.src = carta.id
         console.log(carta.src)
         if(NcarteGirate == 1)
           primaCartGirata = carta
        else{
            NcarteGirate = 0
            if(carta.src == primaCartGirata.src)
            console.log('BRAVO +1 punto')
            else {
                console.log('RIPROVACI')
                setTimeout(()=>{
                carta.src = "yugiohretro.jpg"
                primaCartGirata.src = "yugiohretro.jpg"

                }, 2000)
                
            }

          }
            
                //carta.src = "yugiohretro.jpg"
    }
    </script>
</body>

</html>
