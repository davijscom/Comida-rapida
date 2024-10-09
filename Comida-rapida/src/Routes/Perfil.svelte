<script>
    export let user; // Puedes recibir el usuario como prop
  </script>
  
  <style>
    .profile-container {
      padding: 20px;
      background-color: #f8f9fa;
      border-radius: 10px;
      box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.1);
    }
  
    h1 {
      text-align: center;
    }
  
    .user-info {
      margin: 20px 0;
    }
  
    .user-info p {
      margin: 5px 0;
    }
  
    .settings {
      margin-top: 20px;
      text-align: center;
    }
  </style>
  
  <div class="profile-container">
    <h1>Perfil de Usuario</h1>
    <div class="user-info">
      <p><strong>Email:</strong> {user.email}</p>
      <p><strong>Nombre:</strong> {user.name}</p>
      <p><strong>Teléfono:</strong> {user.phone}</p>
    </div>
  
    <div class="settings">
      <a href="/configuracion">Configuración de cuenta</a> |
      <a href="/cambiar-contrasena">Cambiar contraseña</a>
    </div>
  </div>
  