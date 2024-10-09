<script>
    let nombre = "";
    let apellido = "";
    let email = "";
    let password = "";
    let telefono = "";
    let ciudad = "";
    let isLoading = false;
    let isSuccess = false;
    let errors = {};
    let ciudades = ["Bogotá", "Medellín", "Cali", "Barranquilla", "Cartagena", "Valledupar", "Bucaramanga", "Pereira"];
  
    const handleSubmit = () => {
      errors = {};
  
      if (nombre.length === 0) {
        errors.nombre = "Field should not be empty";
      }
      if (apellido.length === 0) {
        errors.apellido = "Field should not be empty";
      }
      if (email.length === 0) {
        errors.email = "Field should not be empty";
      }
      if (password.length === 0) {
        errors.password = "Field should not be empty";
      }
      if (telefono.length === 0) {
        errors.telefono = "Field should not be empty";
      }
      if (ciudad.length === 0) {
        errors.ciudad = "Field should not be empty";
      }
  
      if (Object.keys(errors).length === 0) {
        isLoading = true;
        setTimeout(() => {
          isSuccess = true;
          isLoading = false;
        }, 1500);
      }
    };
  </script>
  
  <style>
    .register-container {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(to right, #ffffff, #f0f0f0);
    }
  
    form {
      background: #fff;
      padding: 30px;
      width: 500px;
      border-radius: 15px;
      box-shadow: 0px 20px 14px 8px rgba(0, 0, 0, 0.2);
      animation: fadeIn 0.7s ease-in-out;
    }
  
    .input-group {
      display: flex;
      justify-content: space-between;
      margin-bottom: 20px;
    }
  
    .input-group input,
    .input-group select {
      width: 48%; /* Ajuste para que se muestren lado a lado */
      border: none;
      border-bottom: 1px solid #ccc;
      padding: 5px;
    }
  
    .input-group input:focus,
    .input-group select:focus {
      outline: none;
      border-bottom: 1px solid #666;
    }
  
    button {
      background: black;
      color: white;
      padding: 10px 0;
      width: 100%;
      border-radius: 25px;
      font-weight: bold;
      cursor: pointer;
      transition: all 300ms ease-in-out;
    }
  
    button:hover {
      transform: translateY(-2.5px);
      box-shadow: 0px 1px 10px rgba(0, 0, 0, 0.58);
    }
  
    h1 {
      text-align: center;
      font-size: 1.8rem;
      margin-bottom: 20px;
      font-weight: bold;
    }
  
    .errors {
      list-style-type: none;
      padding: 10px;
      margin-top: 10px;
      color: #be6283;
      background: rgba(190, 98, 131, 0.3);
    }
  
    .success {
      text-align: center;
      font-size: 1.5rem;
      color: green;
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
  </style>
  
  <div class="register-container">
    <form on:submit|preventDefault={handleSubmit}>
      {#if isSuccess}
        <div class="success">
          ✔ Registro completado exitosamente.
        </div>
      {:else}
        <h1>Registro de Usuario</h1>
  
        <div class="input-group">
          <input type="text" placeholder="Nombre" bind:value={nombre} />
          <input type="text" placeholder="Apellido" bind:value={apellido} />
        </div>
  
        <div class="input-group">
          <input type="email" placeholder="Correo Electrónico" bind:value={email} />
          <input type="password" placeholder="Contraseña" bind:value={password} />
        </div>
  
        <div class="input-group">
          <input type="tel" placeholder="Número de Teléfono" bind:value={telefono} />
          <select bind:value={ciudad}>
            <option value="" disabled>Seleccione su ciudad</option>
            {#each ciudades as city}
              <option value={city}>{city}</option>
            {/each}
          </select>
        </div>
  
        <button type="submit">{#if isLoading}Registrando...{:else}Registrar{/if}</button>
  
        {#if Object.keys(errors).length > 0}
          <ul class="errors">
            {#each Object.keys(errors) as field}
              <li>{field}: {errors[field]}</li>
            {/each}
          </ul>
        {/if}
      {/if}
    </form>
  </div>
  