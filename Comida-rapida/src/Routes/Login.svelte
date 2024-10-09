<script>
  import { navigate } from 'svelte-routing'; // Importa la función para redirigir
  let correo = '';
  let password = '';
  let userName = 'Mello burguer';
  let error = '';

  function handleSubmit(event) {
    event.preventDefault();
    
    // Comprobación de credenciales
    if (correo === 'admin@gmail.com' && password === 'admin123') {
      error = ''; // Limpiar el error
      localStorage.setItem('correo', correo); // Guardar el nombre de usuario
      localStorage.setItem('userName', userName); // Guardar el nombre de usuario
      navigate('/administrador'); // Redirigir a /admin
    } else {
      error = 'Credenciales incorrectas. Inténtalo de nuevo.';
    }
  }
</script>

  <style>
    .login-container {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(to right, #ffffff, #f0f0f0);
    }
  
    form {
      background: #fff;
      padding: 50px;
      width: 350px;
      border-radius: 15px;
      box-shadow: 0px 20px 14px 8px rgba(0, 0, 0, 0.2);
      animation: fadeIn 0.7s ease-in-out;
      position: relative; /* Para colocar el mensaje de error de manera absoluta */
    }
  
    label {
      margin: 10px 0;
      align-self: flex-start;
      font-weight: 500;
    }
  
    input {
      border: none;
      border-bottom: 1px solid #ccc;
      margin-bottom: 20px;
      transition: all 300ms ease-in-out;
      width: 100%;
      padding: 5px;
    }
  
    input:focus {
      outline: 0;
      border-bottom: 1px solid #666;
    }
  
    button {
      margin-top: 20px;
      background: black;
      color: white;
      padding: 10px 0;
      width: 100%;
      border-radius: 25px;
      text-transform: uppercase;
      font-weight: bold;
      cursor: pointer;
      transition: all 300ms ease-in-out;
    }
  
    button:hover {
      transform: translateY(-2.5px);
      box-shadow: 0px 1px 10px 0px rgba(0, 0, 0, 0.58);
    }
  
    h1 {
      margin: 10px 20px 30px 20px;
      text-align: center;
      font-size: 40px;
      font-weight: bold; /* Negrita para el título */
    }
  
    .errors {
      list-style-type: none;
      padding: 10px;
      margin: 0;
      border: 2px solid #be6283;
      color: #be6283;
      background: rgba(190, 98, 131, 0.3);
      position: absolute; /* Posición absoluta para que no afecte el tamaño del formulario */
      bottom: 20px; /* Coloca los errores en la parte inferior */
      left: 50%;
      transform: translateX(-50%);
      width: calc(100% - 40px); /* Asegúrate de que quepan bien */
      max-height: 100px; /* Altura máxima para el contenedor de errores */
      overflow-y: auto; /* Permite desplazamiento si hay muchos errores */
    }
  
    .success {
      font-size: 24px;
      text-align: center;
      animation: fadeIn 0.5s ease-in-out;
      position: absolute; /* También se coloca de manera absoluta */
      bottom: 20px; /* Coloca el mensaje de éxito en la parte inferior */
      left: 50%;
      transform: translateX(-50%);
      width: calc(100% - 40px); /* Asegúrate de que quepa bien */
    }
  
    @keyframes fadeIn {
      0% {
        opacity: 0;
        transform: scale(0.9);
      }
      100% {
        opacity: 1;
        transform: scale(1);
      }
    }
  
    .forgot-password {
      text-align: center;
      margin-top: 10px;
      font-size: 14px;
    }
  
    .forgot-password a {
      color: #000000; /* Color acorde al resto del diseño */
      text-decoration: none;
    }
  
    .forgot-password a:hover {
      text-decoration: underline;
      color: #000000; /* Color en hover */
    }
  </style>
  
  <div class="login-container">
    <form  on:submit={handleSubmit}>
      {#if error}
        <p class="error">{error}</p>
      {/if}
        <h1>Inicio Sesión</h1>
  
        <label for="username">Usuario</label>
        <input type="text" id="username" bind:value={correo} required />
  
        <label for="password">Contraseña:</label>
        <input type="password" id="password" bind:value={password} required />
  
        <div class="forgot-password">
          <a href="#">Olvidar contraseña?</a> | 
          <a href="#">Recordar contraseña</a>
        </div>

        <button type="submit">Iniciar sesión</button>
  
    </form>
  </div>
  