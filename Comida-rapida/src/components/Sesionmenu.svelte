<main class="container mx-auto p-4">
  <div class="d-flex flex-row justify-content-between align-items-start">
    <!-- Contenido de la izquierda -->
    <div class="left-content me-3">
      <h1 class="title">Bienvenido a Mello Burguer</h1>
      <p class="subtitle">
        En Mello Burguer, nos enorgullecemos de ofrecer una experiencia culinaria excepcional. 
        Nuestro menú incluye hamburguesas artesanales, pollo crujiente, papas doradas y bebidas refrescantes. 
        Todo preparado con ingredientes frescos y seleccionados.
      </p>
      <div class="left-content ne-3">
        <h1 class="title">Descubre el sabor de Mello Burguer</h1>
        <p class="subtitle">
          Prueba nuestras hamburguesas gourmet, pollo crujiente y papas doradas, todo elaborado con ingredientes frescos. Vive una experiencia de sabor única que te hará volver por más.
        </p>
      </div>
    </div>
    
    <!-- Contenido de la derecha con la tarjeta del jefe -->
    <div class="right-content">
      <div class="card large-card">
        <img src="/jefe1.png" alt="Jefe de Mello Burguer" class="card-image">
        <div class="card-body">
          <h2 class="card-title">Conoce a nuestro Chef</h2>
          <p class="card-text">
            Nuestro jefe se asegura de que cada detalle cuente para ofrecerte una experiencia de comida rápida única. Su dedicación a la calidad y el sabor es el alma de Mello Burguer.
          </p>
        </div>
      </div>
    </div>
  </div>

  <!-- Sección del menú de opciones -->
  <section class="menu-options mx-auto my-4 w-full md:w-[85%]">
    <h2 class="menu-title text-center my-4 shadowed-title">Nuestro Menú</h2>
    <div class="row row-cols-1 row-cols-md-4 g-4">
      <div class="col">
        <div class="card menu-card hover-scale h-100">
          <img src="/hamburgesa.jpg" class="card-img-top menu-image" alt="Hamburguesas">
          <div class="card-body">
            <h5 class="card-title menu-item">Hamburguesa</h5>
            <p class="card-text">Deliciosa hamburguesa de carne con ingredientes frescos y sabor irresistible.</p>
          </div>
          
        </div>
      </div>
      <div class="col">
        <div class="card menu-card hover-scale h-100">
          <img src="/pollo.png" class="card-img-top menu-image" alt="Pollo Frito">
          <div class="card-body">
            <h5 class="card-title menu-item">Pollo Frito</h5>
            <p class="card-text">Crujiente pollo frito acompañado de nuestra salsa especial.</p>
          </div>
          
        </div>
      </div>
      <div class="col">
        <div class="card menu-card hover-scale h-100">
          <img src="/papa-frita.png" class="card-img-top menu-image" alt="Papas Fritas">
          <div class="card-body">
            <h5 class="card-title menu-item">Papas Fritas</h5>
            <p class="card-text">Clásicas papas fritas doradas, perfectas para acompañar tu comida.</p>
          </div>
          
        </div>
      </div>
      <div class="col">
        <div class="card menu-card hover-scale h-100">
          <img src="/gaseosa.png" class="card-img-top menu-image" alt="Gaseosas">
          <div class="card-body">
            <h5 class="card-title menu-item">Gaseosa</h5>
            <p class="card-text">Refresca tu paladar con nuestra selección de bebidas gaseosas.</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</main>

<!-- Footer -->
<footer class="bg-light text-center text-lg-start mt-4" style="background: linear-gradient(to bottom, #ffffff, #f8f9fa);  border-top: 2px solid #ff9933;">
  <div class="container p-4">
    <div class="row">
      <div class="col-lg-4 col-md-12 mb-4">
        <h5 class="text-uppercase" style="color: #ff9933;">Mello Burguer</h5>
        <p>
          Disfruta de nuestras deliciosas hamburguesas y platos preparados con ingredientes frescos y de calidad. ¡Te esperamos!
        </p>
      </div>

      <div class="col-lg-4 col-md-12 mb-4">
        <h5 class="text-uppercase" style="color: #ff9933;">Contacto</h5>
        <ul class="list-unstyled">
          <li><a href="#!" class="text-dark">info@melloburguer.com</a></li>
          <li><a href="#!" class="text-dark">+57 3045678989</a></li>
          <li><a href="#!" class="text-dark">Dirección: Calle 18A3 # 34Abis23</a></li>
        </ul>
      </div>

      <div class="col-lg-4 col-md-12 mb-4">
        <h5 class="text-uppercase" style="color: #ff9933;">Síguenos</h5>
        <ul class="list-unstyled d-flex justify-content-center">
          <li class="me-3">
            <a href="#!" class="text-dark"><i class="fab fa-facebook-f"></i> Facebook</a>
          </li>
          <li class="me-3">
            <a href="#!" class="text-dark"><i class="fab fa-twitter"></i> Twitter</a>
          </li>
          <li class="me-3">
            <a href="#!" class="text-dark"><i class="fab fa-instagram"></i> Instagram</a>
          </li>
        </ul>
      </div>
    </div>
  </div>

  <div class="text-center p-3" style="background-color: #f8f9fa;">
    © 2024 Mello Burguer. Todos los derechos reservados.
  </div>
</footer>

<!-- Estilos CSS -->
<style>
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 10px;
  }

  .left-content {
    flex: 1;
    width: 100%;
  }

  .right-content {
    flex: 1;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: flex-start; /* Alineación en la parte superior */
  }

  .large-card {
    background: white;
    border-radius: 12px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    padding: 10px;
    text-align: center;
    max-width: 350px; /* Aumentar el ancho de la tarjeta */
    display: flex;
    flex-direction: column; /* Asegura que el contenido esté en columna */
    justify-content: space-between; /* Distribuye el espacio uniformemente */
  }

  .card-image {
    width: 100%;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 10px;
  }

  .card-body {
    text-align: center;
    padding: 10px; /* Asegura que el contenido tenga espacio interno */
  }

  .card-title {
    font-size: 1.4rem; /* Aumentar tamaño del título */
    font-weight: bold;
  }

  .card-text {
    font-size: 1rem; /* Ajustar según sea necesario */
  }

  .menu-card {
    background: white; /* Fondo blanco para las tarjetas del menú */
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2); /* Sombra más pronunciada */
    transition: transform 0.3s, box-shadow 0.3s; /* Transición para el hover */
    max-width: 220px; /* Aumentar el ancho máximo de las tarjetas del menú */
    text-align: center;
    margin: 10px; /* Margen entre las tarjetas */
  }

  .menu-card:hover {
    transform: scale(1.05); /* Animación de aumento */
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3); /* Mayor sombra al hacer hover */
  }

  .menu-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 12px;
  }

  .menu-item {
    color: #ff9933;
    font-weight: bold;
  }

  .shadowed-title {
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2); /* Sombra ligera en el título */
  }

  .hover-scale {
    transition: transform 0.2s ease;
  }

  .hover-scale:hover {
    transform: scale(1.05);
  }

  /* Estilos generales */
  body {
    font-family: Arial, sans-serif;
    background-color: #f8f9fa;
  }

  h1.title {
    font-size: 2.5rem;
    color: #ff9933;
    margin-bottom: 10px;
  }

  p.subtitle {
    font-size: 1.2rem;
    color: #333;
    line-height: 1.6;
  }

  .menu-title {
    font-size: 2.2rem;
    color: #333;
  }

  footer a {
    text-decoration: none;
  }
</style>
