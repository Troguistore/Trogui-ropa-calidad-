<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mapa Conceptual - Falacias y Paralogismos</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:'Trebuchet MS', sans-serif;
    background:#f5f5f5;
    padding:40px;
}

h1{
    text-align:center;
    margin-bottom:60px;
    background:#ffb6c1;
    width:500px;
    margin-left:auto;
    margin-right:auto;
    padding:20px;
    border-radius:25px;
    box-shadow:10px 10px 0 #d81b60;
    font-size:40px;
}

.map{
    position:relative;
    width:1400px;
    margin:auto;
    height:1400px;
}

/* TARJETAS */

.box{
    position:absolute;
    width:300px;
    padding:20px;
    border-radius:25px;
    box-shadow:8px 8px 0 rgba(0,0,0,0.2);
    transition:0.3s;
}

.box:hover{
    transform:scale(1.03);
}

.box h2{
    text-align:center;
    margin-bottom:12px;
    font-size:24px;
}

.box p{
    font-size:15px;
    line-height:1.5;
}

/* COLORES */

.purple{ background:#d2b4ff; }
.yellow{ background:#fff4a3; }
.pink{ background:#ffd1dc; }
.blue{ background:#b8e7ff; }
.orange{ background:#ffd0a6; }
.green{ background:#d9f8b4; }
.red{ background:#ffb3b3; }
.gray{ background:#e3e3e3; }

/* POSICIONES */

.central{
    top:560px;
    left:480px;
    width:400px;
    text-align:center;
    background:#ffb6c1;
    font-size:24px;
    font-weight:bold;
    z-index:2;
}

.b1{ top:40px; left:60px; }
.b2{ top:40px; left:550px; }
.b3{ top:40px; right:60px; }

.b4{ top:360px; left:40px; }
.b5{ top:360px; right:40px; }

.b6{ top:920px; left:40px; }
.b7{ top:920px; left:380px; }
.b8{ top:920px; right:380px; }
.b9{ top:920px; right:40px; }

/* FLECHAS */

.arrow{
    position:absolute;
    background:black;
}

.vertical{
    width:6px;
}

.horizontal{
    height:6px;
}

/* FLECHAS SUPERIORES */

.a1{
    height:180px;
    top:280px;
    left:210px;
}

.a2{
    height:180px;
    top:280px;
    left:700px;
}

.a3{
    height:180px;
    top:280px;
    right:210px;
}

/* FLECHAS LATERALES */

.a4{
    width:220px;
    top:650px;
    left:250px;
}

.a5{
    width:220px;
    top:650px;
    right:250px;
}

/* FLECHAS INFERIORES */

.a6{
    height:180px;
    top:760px;
    left:210px;
}

.a7{
    height:180px;
    top:760px;
    left:530px;
}

.a8{
    height:180px;
    top:760px;
    right:530px;
}

.a9{
    height:180px;
    top:760px;
    right:210px;
}

</style>
</head>

<body>

<h1>MAPA CONCEPTUAL<br>Falacias y Paralogismos</h1>

<div class="map">

<!-- FLECHAS -->
<div class="arrow vertical a1"></div>
<div class="arrow vertical a2"></div>
<div class="arrow vertical a3"></div>

<div class="arrow horizontal a4"></div>
<div class="arrow horizontal a5"></div>

<div class="arrow vertical a6"></div>
<div class="arrow vertical a7"></div>
<div class="arrow vertical a8"></div>
<div class="arrow vertical a9"></div>

<!-- CENTRO -->

<div class="box central">
RAZONAMIENTO INCORRECTO<br>
Falacias y Paralogismos
</div>

<!-- ARRIBA -->

<div class="box purple b1">
<h2>¿Qué son?</h2>
<p>
Errores en el razonamiento donde la conclusión no se deriva correctamente de las premisas.
</p>
</div>

<div class="box yellow b2">
<h2>Razonamiento Natural</h2>
<p>
Es cotidiano y espontáneo.
<br><br>
Ejemplo:
“Ese abogado habla duro, entonces tiene razón”.
</p>
</div>

<div class="box pink b3">
<h2>Razonamiento Lógico</h2>
<p>
Busca coherencia y rigor.
Muy importante en el Derecho y las sentencias judiciales.
</p>
</div>

<!-- MEDIO -->

<div class="box blue b4">
<h2>Homonimia</h2>
<p>
Una palabra tiene varios significados.
<br><br>
“Derecho” puede significar:
<br>
• ley
<br>
• facultad
</p>
</div>

<div class="box orange b5">
<h2>Falsa Causa</h2>
<p>
Se atribuye una causa equivocada.
<br><br>
“Ganó Colombia porque me puse la camiseta”.
</p>
</div>

<!-- ABAJO -->

<div class="box green b6">
<h2>Afirmar el Consecuente</h2>
<p>
Si llueve → la calle se moja.
<br>
La calle está mojada.
<br>
Entonces llovió.
<br><br>
❌ Puede existir otra causa.
</p>
</div>

<div class="box red b7">
<h2>Petición de Principio</h2>
<p>
Se intenta probar algo usando la misma idea.
<br><br>
“El acusado es culpable porque cometió el delito”.
</p>
</div>

<div class="box gray b8">
<h2>Falsa Generalización</h2>
<p>
Tomar pocos casos y aplicarlos a todos.
<br><br>
“Dos políticos robaron, entonces todos son corruptos”.
</p>
</div>

<div class="box purple b9">
<h2>Argumento por Ignorancia</h2>
<p>
Algo es verdadero porque nadie ha probado lo contrario.
<br><br>
“Los fantasmas existen porque nadie ha demostrado que no”.
</p>
</div>

</div>

</body>
</html>
