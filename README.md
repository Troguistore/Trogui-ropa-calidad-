<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trogui - Picador de Frutas y Verduras 5 en 1</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #FF6F00;
            color: white;
            text-align: center;
            padding: 10px;
        }

        .container {
            max-width: 1200px;
            margin: auto;
            padding: 20px;
        }

        h1 {
            text-align: center;
            color: #FF6F00;
        }

        .product {
            text-align: center;
        }

        .carousel {
            display: flex;
            overflow-x: auto;
            gap: 10px;
            margin: 20px 0;
        }

        .carousel img {
            max-width: 300px;
            border-radius: 5px;
        }

        .price {
            font-size: 24px;
            color: #FF6F00;
        }

        .description {
            text-align: left;
            margin: 20px 0;
        }

        .buy-button, .more-products-button {
            display: inline-block;
            padding: 15px 30px;
            margin: 20px;
            background-color: #FF6F00;
            color: white;
            border: none;
            cursor: pointer;
            font-size: 18px;
            border-radius: 5px;
        }

        .buy-button:hover {
            border: 2px solid green;
        }

        .form-popup {
            display: none;
            position: fixed;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            background-color: white;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
            border-radius: 10px;
            z-index: 100;
        }

        .form-popup input {
            display: block;
            width: 100%;
            margin-bottom: 10px;
            padding: 10px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }

        .form-popup button {
            background-color: #FF6F00;
            color: white;
            padding: 10px;
            border: none;
            cursor: pointer;
            font-size: 16px;
            width: 100%;
            border-radius: 5px;
        }

        .footer {
            text-align: center;
            padding: 20px;
            background-color: #FF6F00;
            color: white;
        }

        .footer button {
            background-color: white;
            color: #FF6F00;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            font-size: 16px;
            border-radius: 5px;
        }

    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <p>Trogui, tu tienda online de confianza. Envíos gratis y pagos contra entrega a toda la bella Colombia.</p>
    </header>

    <div class="container">

        <!-- Product Information -->
        <h1>Picador de Frutas y Verduras 5 en 1</h1>
        <div class="product">
            <p class="price">Precio: 49,000 COP</p>
            <div class="carousel">
                <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/1139591/1725023937imageUrl_1.jpg" alt="Imagen 1">
                <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/557426/170241353017.png" alt="Imagen 2">
                <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/557426/170241353015.png" alt="Imagen 3">
            </div>
        </div>

        <!-- Product Description -->
        <div class="description">
            <h2>Descripción del producto:</h2>
            <ul>
                <li>Envío gratis y pago contra entrega.</li>
                <li>Material de calidad: Hoja de acero inoxidable de alto carbono, resistente y duradera.</li>
                <li>Medidas compactas: Diseño plegable para fácil almacenamiento en espacios pequeños.</li>
                <li>Ajuste de grosor: Dial giratorio permite seleccionar el grosor deseado.</li>
                <li>Ventosas antideslizantes: 4 filas de ventosas aseguran estabilidad durante su uso.</li>
                <li>Seguro y práctico: Sistema de empuje evita contacto con las cuchillas, brindando mayor seguridad.</li>
                <li>Tiempo en llegar: menos de 10 días.</li>
                <li>Garantía: producto incompleto, roto, mal funcionamiento o equivocado.</li>
            </ul>
        </div>

        <!-- Buttons -->
        <button class="buy-button" onclick="openForm()">Comprar ahora</button>
        <button class="more-products-button" onclick="window.location.href='https://troguistore.github.io/Trogui-s/'">Ver más productos</button>

        <!-- Form Popup -->
        <div class="form-popup" id="buyForm">
            <h2>Formulario de Compra</h2>
            <input type="text" placeholder="Nombre" required>
            <input type="text" placeholder="Apellido" required>
            <input type="text" placeholder="Contacto" required>
            <input type="text" placeholder="Dirección" required>
            <input type="text" placeholder="Departamento" required>
            <input type="text" placeholder="Ciudad" required>
            <button onclick="sendWhatsApp()">Realizar compra</button>
        </div>

    </div>

    <!-- Footer -->
    <div class="footer">
        <button onclick="requestPassword()">Trogui</button>
    </div>

    <script>
        function openForm() {
            document.getElementById("buyForm").style.display = "block";
        }

        function sendWhatsApp() {
            window.location.href = "https://wa.me/573206572598?text=¡Hola!%20Quisiera%20realizar%20una%20compra%20en%20tu%20tienda.%20¿Puedes%20ayudarme%20con%20los%20detalles%20de%20";
        }

        function requestPassword() {
            let password = prompt("Ingresa la contraseña para ver el análisis:");
            if (password === "321") {
                alert("Enviando análisis al WhatsApp.");
                window.location.href = "https://wa.me/573206572598?text=¡Hola!%20Quisiera%20realizar%20una%20compra%20en%20tu%20tienda.%20¿Puedes%20ayudarme%20con%20los%20detalles%20de%20";
            } else {
                alert("Contraseña incorrecta.");
            }
        }
    </script>

</body>
</html>
