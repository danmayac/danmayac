<meta charset="UTF-8>">
<body>
<canvas width="600" height="400"></canvas>

    <script>

    var tela = document.querySelector("canvas");
    var pincel = tela.getContext("2d");
    pincel.fillStyle = "lightgray";
    pincel.fillRect(0, 0, 600, 400);

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2*3.14);
        pincel.fill();
    }

    function desenhaFlor(x, y){
    desenhaCirculo(x, y, 20, "red");
    desenhaCirculo(x, y - 40, 20, "yellow");
    desenhaCirculo(x, y + 40, 20, "blue");
    desenhaCirculo(x - 40, y, 20, "orange");
    desenhaCirculo(x + 40, y, 20, "black");
}

function desenhaBuquê(){
for(var x = 100; x <= 500; x = x + 200){
desenhaFlor(x, 200);
desenhaFlor(x, 65);
desenhaFlor(x, 335);
}
}

desenhaBuquê();

    </script>
</body>

