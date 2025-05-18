<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>تسجيل الدخول - لعبة صندوق الحظ</title>
  <style>
    body {
      font-family: 'Tahoma', sans-serif;
      background: linear-gradient(to bottom, #f9f9f9, #e0e0e0);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .container {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 0 20px rgba(0,0,0,0.1);
      width: 90%;
      max-width: 400px;
    }
    h2 {
      text-align: center;
      color: #333;
    }
    input {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 10px;
      font-size: 16px;
    }
    button {
      width: 100%;
      padding: 14px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 10px;
      font-size: 18px;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
    .switch {
      text-align: center;
      margin-top: 15px;
      font-size: 14px;
    }
    .switch a {
      color: #007BFF;
      text-decoration: none;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="container" id="loginBox">
    <h2>تسجيل الدخول</h2>
    <input type="tel" placeholder="رقم الجوال" id="phone">
    <input type="password" placeholder="كلمة المرور" id="password">
    <button onclick="login()">دخول</button>
    <div class="switch">لا تملك حساب؟ <a onclick="showRegister()">إنشاء حساب</a></div>
  </div>

  <div class="container" id="registerBox" style="display: none;">
    <h2>إنشاء حساب جديد</h2>
    <input type="tel" placeholder="رقم الجوال" id="regPhone">
    <input type="password" placeholder="كلمة المرور" id="regPassword">
    <button onclick="register()">إنشاء حساب</button>
    <div class="switch">لديك حساب؟ <a onclick="showLogin()">دخول</a></div>
  </div>

  <script>
    function showRegister() {
      document.getElementById('loginBox').style.display = 'none';
      document.getElementById('registerBox').style.display = 'block';
    }
    function showLogin() {
      document.getElementById('registerBox').style.display = 'none';
      document.getElementById('loginBox').style.display = 'block';
    }
    function login() {
      // هنا من المفترض التحقق من البيانات ثم نقل المستخدم للصفحة التالية
      alert('تم تسجيل الدخول!')
      // window.location.href = 'subscription.html'; // بعد التجهيز
    }
    function register() {
      alert('تم إنشاء الحساب!')
      showLogin();
    }
  </script>
</body>
</html>
