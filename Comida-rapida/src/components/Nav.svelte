<script>
    let search = "";
</script>

<style>
    
    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background: linear-gradient(to right, #ffffff, #f0f0f0); /* Degradado blanco */
        padding: 10px 20px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        width: 90%;
        position: fixed;
        top: 5px;
        left: 50%;
        transform: translateX(-50%); /* Centrar la barra de navegación */
        z-index: 1000;
        border-radius: 10px;
        transition: cubic-bezier(0.175, 0.885, 0.32, 1.275) 0.3s ease; /* Transición para el fondo */
    }
    

    .logo {
        font-size: 2rem;
        font-weight: bold;
        color: #ffcc00; /* Color naranja claro similar al de McDonald's */
        margin-right: 20px; /* Espacio entre el logo y los enlaces */
    }

    .nav-links {
        display: flex;
        gap: 20px;
        align-items: center;
    }

    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        display: flex;
        gap: 20px;
    }

    li {
        cursor: pointer;
        transition: color 0.3s, transform 0.2s; /* Transiciones suaves */
    }

    li:hover {
        color: #ff9933; /* Color al pasar el mouse */
        transform: scale(1.05); /* Efecto de escalado */
    }

    .right-section {
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .search-bar {
        padding: 8px;
        border: 1px solid #ccc;
        border-radius: 4px;
        width: 200px; /* Ajuste de ancho */
        transition: border-color 0.3s; /* Transición para el borde */
    }

    .search-bar:focus {
        border-color: #ff9933; /* Color del borde al enfocar */
        outline: none; /* Eliminar el contorno */
    }

    .circular-image {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background-color: gray;
        margin-right: 5px;
    }

    .button-ingresar,
    .button-register {
        background-color: #ff9933;
        color: white;
        padding: 8px 16px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.3s, transform 0.2s; /* Transiciones suaves */
    }

    .button-ingresar:hover,
    .button-register:hover {
        background-color: #ff9933; /* Color al pasar el mouse */
        transform: scale(1.05); /* Efecto de escalado */
    }

    .cart-icon {
        font-size: 1.5rem; /* Tamaño del icono de carrito */
        cursor: pointer;
    }

    @media (max-width: 768px) {
        nav {
            flex-direction: column; /* Cambiar a columna en pantallas pequeñas */
            align-items: flex-start; /* Alinear a la izquierda */
            margin: 0 20px; /* Ajuste del margen */
        }

        .nav-links {
            margin-top: 10px; /* Espacio entre el logo y los enlaces */
        }

        .search-bar {
            width: 100%; /* Ocupa todo el ancho en pantallas pequeñas */
        }
    }
    

        
</style>

<nav>
    <div class="left-section" style="display: flex; align-items: center;">
        <a href="/" class="logo text-decoration-none">Mello Burguer</a>
        <div class="nav-links">
            <ul>
                <li>Productos</li>
                
                <a class="text-dark text-decoration-none" href="/combos">Combos</a>
                <li>Servicios</li>
                <li>Soporte</li>
            </ul>
        </div>
        
    </div>
    
    <div class="right-section">
        <input class="search-bar" type="text" placeholder="Buscar..." bind:value={search}/>
        <span class="material-symbols-outlined">
            shopping_cart
            </span>
        <a href="/login" class="button-ingresar">Ingresar</a>
        
        <a href="/Register" class="button-register">Registrarse</a> <!-- Botón de registrarse -->
    </div>
</nav>
