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
    input[type="email"],
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

    .form-actions {
      display: flex;
      justify-content: flex-end;
      margin-bottom: 20px;
    }

    .link-btn {
      color: var(--accent-blue);
      font-size: 13px;
      text-decoration: none;
      font-weight: 600;
      background: none;
      border: none;
      cursor: pointer;
    }

    .link-btn:hover {
      text-decoration: underline;
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

    .signup-text {
      text-align: center;
      margin-top: 20px;
      font-size: 14px;
      color: var(--text-dark);
    }

    #message {
      margin-top: 15px;
      text-align: center;
      font-size: 14px;
      font-weight: 600;
    }

    /* Modal Styles */
    .modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(10, 37, 64, 0.5);
      justify-content: center;
      align-items: center;
    }

    .modal-content {
      background-color: var(--cream-card);
      padding: 30px;
      border-radius: 12px;
      width: 100%;
      max-width: 380px;
      position: relative;
    }

    .close-btn {
      position: absolute;
      top: 15px;
      right: 15px;
      font-size: 20px;
      cursor: pointer;
      color: var(--primary-blue);
    }
  </style>
</head>
<body>

  <!-- Main Login Card -->
  <div class="login-container">
    <div class="logo-container">
      <div class="logo">PRESIDO <span>BANK</span></div>
      <p class="subtitle">Secure Online Banking</p>
    </div>

    <form id="loginForm">
      <div class="form-group">
        <label for="username">Username / Account ID</label>
        <input type="text" id="username" required>
      </div>

      <div class="form-group">
        <label for="password">Password</label>
        <input type="password" id="password" required>
      </div>

      <div class="form-actions">
        <button type="button" class="link-btn" id="openForgot">Forgot Password?</button>
      </div>

      <button type="submit" class="login-btn">Log In</button>
    </form>

    <p class="signup-text">Don't have an account? <button class="link-btn" id="openSignup">Sign Up</button></p>
    <div id="message"></div>
  </div>

  <!-- Forgot Password Modal -->
  <div class="modal" id="forgotModal">
    <div class="modal-content">
      <span class="close-btn" id="closeForgot">&times;</span>
      <h3 style="color: var(--primary-blue); margin-bottom: 15px;">Reset Password</h3>
      <form id="forgotForm">
        <div class="form-group">
          <label for="forgotEmail">Email Address</label>
          <input type="email" id="forgotEmail" required>
        </div>
        <button type="submit" class="login-btn">Send Reset Link</button>
      </form>
    </div>
  </div>

  <!-- Sign Up Modal -->
  <div class="modal" id="signupModal">
    <div class="modal-content">
      <span class="close-btn" id="closeSignup">&times;</span>
      <h3 style="color: var(--primary-blue); margin-bottom: 15px;">Create Account</h3>
      <form id="signupForm">
        <div class="form-group">
          <label for="signupUser">Username</label>
          <input type="text" id="signupUser" required>
        </div>
        <div class="form-group">
          <label for="signupEmail">Email</label>
          <input type="email" id="signupEmail" required>
        </div>
        <div class="form-group">
          <label for="signupPass">Password</label>
          <input type="password" id="signupPass" required>
        </div>
        <button type="submit" class="login-btn">Register</button>
      </form>
    </div>
  </div>

  <script>
    const forgotModal = document.getElementById('forgotModal');
    const signupModal = document.getElementById('signupModal');
    const messageDiv = document.getElementById('message');

    // Modal controls
    document.getElementById('openForgot').onclick = () => forgotModal.style.display = 'flex';
    document.getElementById('closeForgot').onclick = () => forgotModal.style.display = 'none';
    document.getElementById('openSignup').onclick = () => signupModal.style.display = 'flex';
    document.getElementById('closeSignup').onclick = () => signupModal.style.display = 'none';

    // Login Request
    document.getElementById('loginForm').addEventListener('submit', async (e) => {
      e.preventDefault();
      const response = await fetch('http://localhost:3000/api/login', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({
          username: document.getElementById('username').value,
          password: document.getElementById('password').value
        })
      });
      const data = await response.json();
      messageDiv.style.color = response.ok ? '#1b5e20' : '#b71c1c';
      messageDiv.textContent = data.message;
    });

    // Forgot Password Request
    document.getElementById('forgotForm').addEventListener('submit', async (e) => {
      e.preventDefault();
      const response = await fetch('http://localhost:3000/api/forgot-password', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ email: document.getElementById('forgotEmail').value })
      });
      const data = await response.json();
      alert(data.message);
      forgotModal.style.display = 'none';
    });

    // Sign Up Request
    document.getElementById('signupForm').addEventListener('submit', async (e) => {
      e.preventDefault();
      const response = await fetch('http://localhost:3000/api/signup', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({
          username: document.getElementById('signupUser').value,
          email: document.getElementById('signupEmail').value,
          password: document.getElementById('signupPass').value
        })
      });
      const data = await response.json();
      alert(data.message);
      if (response.ok) signupModal.style.display = 'none';
    });
  </script>
</body>
</html>
