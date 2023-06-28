<!DOCTYPE html>
<html>
<head>
  <title>Tela de Menus</title>
  <style>
    body {
      background-color: #E1F3E1;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial, sans-serif;
    }

    .menu-container {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      background-color: white;
      padding: 20px;
      border-radius: 5px;
      box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    }

    .welcome-message {
      font-size: 18px;
      color: #4CAF50;
      margin-bottom: 20px;
    }

    .menu-buttons {
      display: flex;
      flex-direction: column;
    }

    .menu-buttons button {
      background-color: #4CAF50;
      color: white;
      border: none;
      padding: 10px 20px;
      margin-bottom: 10px;
      cursor: pointer;
    }

    .logo-container {
      display: flex;
      align-items: center;
      justify-content: flex-end;
      margin-top: -20px;
      margin-right: -20px;
    }

    .logo-container img {
      width: 80px;
      height: 80px;
      margin-right: 10px;
    }

  </style>
  <script>
    // Verifica se o usuário está logado ao carregar a página
    window.onload = function() {
      var isLoggedIn = checkLoginStatus();
      if (!isLoggedIn) {
        redirectToLogin();
      }
    };

    // Função para verificar o status do login
    function checkLoginStatus() {
      // Verifique o status do login aqui (pode ser uma verificação de cookie, token, etc.)
      var isLoggedIn = false; // Defina como true se o login estiver válido

      return isLoggedIn;
    }

    // Função para redirecionar para a página de login
    function redirectToLogin() {
      window.location.href = "https://sistemascoachin.github.io/Login-/";
    }

    // Função para redirecionar para a tela de menus
    function redirectToMenu() {
      window.location.href = "https://sistemascoachin.github.io/menu2/";
    }
  </script>
</head>
<body>
  <div class="menu-container">
    <div class="logo-container">
      <img src="https://drive.google.com/uc?id=1lYi-W7s23S9fiqmRv5jO8DzhDuZ8Wuv5" alt="Logo">
      <p>Bem-vindo de volta!</p>
    </div>
    <div class="welcome-message">Selecione uma opção:</div>
    <div class="menu-buttons">
      <button onclick="redirectToMenu()">Lançar Sublocações</button>
      <button onclick="redirectToMenu()">Lançar Particulares da Clínica</button>
    </div>
  </div>
</body>
</html>
