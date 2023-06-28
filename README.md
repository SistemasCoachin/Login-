<!DOCTYPE html>
<html>
<head>
  <title>Tela de Login</title>
  <style>
    body {
      background-color: #E1F3E1;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial, sans-serif;
    }

    .login-container {
      display: flex;
      align-items: center;
      background-color: white;
      padding: 20px;
      border-radius: 5px;
      box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    }

    .login-form {
      display: flex;
      flex-direction: column;
      margin-left: 20px;
    }

    .login-form label {
      margin-bottom: 10px;
    }

    .login-form input[type="text"],
    .login-form input[type="password"] {
      padding: 5px;
      margin-bottom: 10px;
    }

    .login-form input[type="submit"] {
      background-color: #4CAF50;
      color: white;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
    }

    .error-message {
      color: red;
      margin-top: 10px;
      font-size: 14px;
      display: none; /* Esconder mensagem de erro por padrão */
    }

    h1 {
      font-size: 24px;
      color: #4CAF50;
      margin-bottom: 20px;
    }
  </style>
  <script>
    function validateForm() {
      var username = document.getElementById("username").value;
      var password = document.getElementById("password").value;

      if (username === "admin" && password === "admin") {
        // Login successful
        return true;
      } else {
        // Login failed
        var errorMessage = document.getElementById("error-message");
        errorMessage.style.display = "block"; // Exibir mensagem de erro
        return false;
      }
    }
  </script>
</head>
<body>
  <div class="login-container">
    <img src="https://drive.google.com/uc?id=1lYi-W7s23S9fiqmRv5jO8DzhDuZ8Wuv5" alt="Logo" width="150" height="150">
    <form class="login-form" onsubmit="return validateForm()">
      <h1>Sistema Administrativo</h1>
      <label for="username">Usuário:</label>
      <input type="text" id="username" name="username">
      
      <label for="password">Senha:</label>
      <input type="password" id="password" name="password">
      
      <input type="submit" value="Entrar">
      <p id="error-message" class="error-message">Você não é um colaborador CoachinGente, favor verificar as credenciais</p> <!-- Espaço reservado para a mensagem de erro -->
    </form>
  </div>
</body>
</html>
