<script>
  let username = localStorage.getItem('userName'); // Obtener el nombre de usuario de localStorage

  // cerrar sesion 
function logout() {
  localStorage.removeItem('username'); // Eliminar el nombre de usuario de localStorage
  window.location.href = '/'; // Redirigir al inicio
}
</script>

  <style>
    .admin-container {
      padding: 20px;
      background-color: #f8f9fa;
      border-radius: 10px;
      box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.1);
    }
  </style>
  
  <div class="admin-container">
    <h1>Bienvenido, {username}!</h1>
    <h2>Perfil de Usuario</h2>
    <p><strong>Email:</strong> {username}</p>
    <p><strong>Descripción:</strong> Aquí puedes agregar una descripción del usuario.</p>
  
    <h2>Configuración</h2>
    <ul>
      <li><a href="/configuracion">Configuración de cuenta</a></li>
      <li><a href="/cambiar-contrasena">Cambiar contraseña</a></li>
      <button on:click={logout}>Cerrar sesión</button>
      <li><a href="/seguridad">Seguridad</a></li>
    </ul>
  </div>
  