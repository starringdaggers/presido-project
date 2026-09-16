<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Presido Bank - Login</title>
  <style>
    :root {
      --primary-blue: #0A2540;
      --accent-blue: #1A4971;
      --cream-bg: #FDFBF7;
      --cream-card: #F5EFEB;
      --text-dark: #2C3E50;
      --white: #FFFFFF;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: var(--cream-bg);
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
    }

    .login-container {
      background-color: var(--cream-card);
      padding: 40px;
      border-radius: 12px;
      box-shadow: 0 8px 24px rgba(10, 37, 64, 0.1);
      width: 100%;
      max-width: 400px;
      border: 1px solid rgba(10, 37, 64, 0.08);
    }

    .logo-container {
      text-align: center;
      margin-bottom: 24px;
    }

    .logo {
      font-size: 32px;
      font-weight: 800;
      color: var(--primary-blue);
      letter-spacing: 1px;
    }

    .logo span {
      color: var(--accent-blue);
      font-weight: 300;
    }

    .subtitle {
      color: var(--text-dark);
      font-size: 14px;
      margin-top: 4px;
    }

    .form-group {
      margin-bottom: 20px;
    }

    label {
      display: block;
      margin-bottom: 8px;
      color: var(--primary-blue);
      font-weight: 600;
      font-size: 14px;
    }

    input[type="text"],
    input[type="password"] {
      width: 100%;
      padding: 12px;
      border: 1.5px solid #D1C7BD;
      border-radius: 6px;
      background-color: var(--white);
      color: var(--text-dark);
      font-size: 14px;
      outline: none;
      transition: border-color 0.2s;
    }

    input:focus {
      border-color: var(--primary-blue);
    }

    .login-btn {
      width: 100%;
      padding: 12px;
      background-color: var(--primary-blue);
      color: var(--cream-bg);
      border: none;
      border-radius: 6px;
      font-size: 16px;
      font-weight: 600;
      cursor: pointer;
      transition: background-color 0.2s;
    }

    .login-btn:hover {
      background-color: var(--accent-blue);
    }

    #message {
      margin-top: 15px;
      text-align: center;
      font-size: 14px;
      font-weight: 600;
    }
  </style>
</head>
<body>

  <div class="login-container">
    <div class="logo-container">
      <div class="logo">PRESIDO <span>BANK</span></div>
      <p class="subtitle">Secure Online Banking</p>
    </div>

    <form id="loginForm">
      <div class="form-group">
        <label for="username">Username / Account ID</label>
        <input type="text" id="username" name="username" required>
      </div>

      <div class="form-group">
        <label for="password">Password</label>
        <input type="password" id="password" name="password" required>
      </div>

      <button type="submit" class="login-btn">Log In</button>
    </form>

    <div id="message"></div>
  </div>

  <script>
    document.getElementById('loginForm').addEventListener('submit', async (e) => {
      e.preventDefault();
      const username = document.getElementById('username').value;
      const password = document.getElementById('password').value;
      const messageDiv = document.getElementById('message');

      try {
        const response = await fetch('http://localhost:3000/api/login', {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify({ username, password })
        });

        const result = await response.json();

        if (response.ok) {
          messageDiv.style.color = '#1b5e20';
          messageDiv.textContent = result.message;
        } else {
          messageDiv.style.color = '#b71c1c';
          messageDiv.textContent = result.message;
        }
      } catch (err) {
        messageDiv.style.color = '#b71c1c';
        messageDiv.textContent = 'Server connection failed.';
      }
    });
  </script>
</body>
</html>
