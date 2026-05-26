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
    padding:20px;
}

.page{
    width:1100px;
    margin:auto;
    background:white;
    padding:30px;
    border-radius:25px;
    box-shadow:0 0 20px rgba(0,0,0,0.15);
    position:relative;
    overflow:hidden;
}

/* TITULO CENTRAL */

.center-title{
    width:420px;
    margin:30px auto 60px auto;
    background:#ffb3c1;
    color:#222;
    text-align:center;
    padding:25px;
    border-radius:25px;
    font-size:32px;
    font-weight:bold;
    box-shadow:10px 10px 0 #d81b60;
    position:relative;
    z-index:10;
}

/* CONTENEDOR */

.map{
    position:relative;
    width:100%;
    height:1200px;
}

/* TARJETAS */

.card{
    width:280px;
    padding:18px;
    border-radius:25px;
    position:absolute;
    box-shadow:8px 8px 0 rgba(0,0,0,0.18);
    transition:0.3s;
}

.card:hover{
    transform:scale(1.03);
}

.card h2{
    text-align:center;
    margin-bottom:10px;
    font-size:21px;
    color:#222;
}

.card p{
    font-size:14px;
    line-height:1.5;
    color:#333;
}

/* COLORES */

.purple{background:#d7b8ff;}
.yellow{background:#fff0a6;}
.pink{background:#ffc9c9;}
.blue{background:#b8e3ff;}
.orange{background:#ffd0a8;}
.green{background:#d8f7b2;}
.red{background:#ffb2b2;}
.gray{background:#e4e4e4;}

/* POSICIONES */

.c1{top:0; left:30px;}
.c2{top:0; left:400px;}
.c3{top:0; right:30px;}

.c4{top:350px; left:20px;}
.c5{top:350px; left:410px;}
.c6{top:350px; right:20px;}

.c7{top:720px; left:20px;}
.c8{top:720px; left:410px;}
.c9{top:720px; right:20px;}

/* FLECHAS SVG */

svg{
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:100%;
    pointer-events:none;
}

.line{
    stroke:#222;
    stroke-width:4;
    fill:none;
    marker-end:url(#arrow);
}

.footer{
    text-align:center;
    margin-top:20px;
    font-size:18px;
    font-weight:bold;
    color:#444;
}

</style>
</head>

<body>

<div class="page">

<div class="center-title">
MAPA CONCEPTUAL<br>
Falacias y Paralogismos
</div>

<div class="map">

<!-- FLECHAS -->
<svg>

<defs>
<marker id="arrow" markerWidth="10" markerHeight="10" refX="6" refY="3" orient="auto">
<path d="M0,0 L0,6 L9,3 z" fill="#222"></path>
</marker>
</defs>

<!-- FILA SUPERIOR -->
<line class="line" x1="550" y1="120" x2="180" y2="180"/>
<line class="line" x1="550" y1="120" x2="550" y2="180"/>
<line class="line" x1="550" y1="120" x2="930" y2="180"/>

<!-- FILA MEDIA -->
<line class="line" x1="550" y1="120" x2="180" y2="530"/>
<line class="line" x1="550" y1="120" x2="550" y2="530"/>
<line class="line" x1="550" y1="120" x2="930" y2="530"/>

<!-- FILA INFERIOR -->
<line class="line" x1="550" y1="120" x2="180" y2="900"/>
<line class="line" x1="550" y1="120" x2="550" y2="900"/>
<line class="line" x1="550" y1="120" x2="930" y2="900"/>

</svg>

<!-- TARJETAS -->

<div class="card purple c1">
<h2>¿Qué son?</h2>
<p>
Son errores en el razonamiento donde la conclusión no se deriva correctamente de las premisas.
Muy comunes en debates jurídicos y argumentaciones.
</p>
</div>

<div class="card yellow c2">
<h2>Homonimia</h2>
<p>
Una palabra tiene varios significados.
<br><br>
Ejemplo:
“Derecho” puede significar ley o facultad personal.
</p>
</div>

<div class="card pink c3">
<h2>Falsa Causa</h2>
<p>
Se atribuye una causa equivocada.
<br><br>
Ejemplo:
“Me puse la camiseta de Colombia y por eso ganó la selección”.
</p>
</div>

<div class="card blue c4">
<h2>Afirmar el Consecuente</h2>
<p>
Si llueve → la calle se moja.
<br>
La calle está mojada.
<br>
Entonces llovió.
<br><br>
❌ Puede haber otra causa.
</p>
</div>

<div class="card orange c5">
<h2>Negar el Antecedente</h2>
<p>
Si estudio → apruebo.
<br>
No estudié.
<br>
Entonces no aprobaré.
<br><br>
❌ Puede aprobar igualmente.
</p>
</div>

<div class="card green c6">
<h2>Petición de Principio</h2>
<p>
Intentar demostrar algo usando la misma idea.
<br><br>
“El acusado es culpable porque cometió el delito”.
</p>
</div>

<div class="card red c7">
<h2>Argumento por Ignorancia</h2>
<p>
Se considera verdadero algo porque nadie ha probado lo contrario.
<br><br>
Ejemplo:
“Los fantasmas existen porque nadie ha demostrado que no existen”.
</p>
</div>

<div class="card gray c8">
<h2>Falsa Generalización</h2>
<p>
Tomar pocos casos y aplicarlos a todos.
<br><br>
Ejemplo:
“Dos políticos fueron corruptos, entonces todos lo son”.
</p>
</div>

<div class="card purple c9">
<h2>Idea Principal</h2>
<p>
En Derecho no basta con hablar bonito.
<br><br>
✔ Debe existir lógica
<br>
✔ coherencia
<br>
✔ pruebas
<br>
✔ motivación jurídica
</p>
</div>

</div>

<div class="footer">
Florencio Mixán Mass – Razonamiento Incorrecto
</div>

</div>

</body>
</html>
