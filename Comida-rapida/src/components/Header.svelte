<main>
    <div class="banner">
        
        <div class="banner-content">
            <h1 class="title">Disfruta la mejor comida rápida</h1>
            <p class="subtitle">Pedidos rápidos, frescos y deliciosos</p>
        </div>
    </div>
</main>

<style>
    .banner {
        position: relative;
        background-image: url('/fondo4.jpg');
        background-size: cover; /* La imagen ocupa todo el fondo */
        background-repeat: no-repeat;
        background-position: center; /* Imagen centrada */
        min-height: 79vh; /* Altura mínima del banner */
        display: flex;
        justify-content: center; /* Centrar horizontalmente */
        align-items: center; /* Centrar verticalmente */
        padding: 0 20px;
    
    }

    .banner-content {
        position: absolute; /* Posiciona el contenido sobre la imagen */
        left: 1%;
        text-align: center; /* Centra el texto */
        color: white; /* Texto blanco para mayor contraste */
        background-color: rgba(0, 0, 0, 0.5); /* Fondo semitransparente para mejorar la legibilidad */
        padding: 20px;
        border-radius: 10px; /* Bordes redondeados */
    }

    .title {
        font-size: 3rem;
        font-weight: bold;
        margin: 0;
        color: #ff9933;
    }

    .subtitle {
        font-size: 1.5rem;
        margin-top: 10px;
        color: #ff9933;
    }

    @media (max-width: 768px) {
        .banner-content {
            max-width: 90%; /* Ajustar ancho del contenido en pantallas pequeñas */
        }
        .title {
            font-size: 2rem; /* Ajustar tamaño del texto en pantallas pequeñas */
        }
        .subtitle {
            font-size: 1.2rem;
        }
    }
</style>
