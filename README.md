<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        .login-container {
            background: white;
            padding: 20px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            border-radius: 5px;
            text-align: center;
        }
        .login-container h2 {
            margin-bottom: 20px;
        }
        .login-container input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .login-container button {
            background-color: #333;
            color: white;
            padding: 10px;
            width: 100%;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .login-container button:hover {
            background-color: #555;
        }
        .error-message {
            color: red;
            display: none;
            margin-top: 10px;
        }
    </style>
    <script>
        function handleLogin(event) {
            event.preventDefault(); // ป้องกันการรีเฟรชหน้า
            
            var username = document.getElementById("username").value;
            var password = document.getElementById("password").value;
            var errorMessage = document.getElementById("error-message");
            
            if (username === "Phat" && password === "270350") {
                window.location.href = "https://www.facebook.com/profile.php?id=100023578087605";
            } else {
                errorMessage.textContent = "Incorrect username or password"; // แสดงข้อความผิดพลาด
                errorMessage.style.display = "block"; // ทำให้ข้อความมองเห็น
            }
        }
    </script>
</head>
<body>
    <div class="login-container">
        <h2>Login</h2>
        <form onsubmit="handleLogin(event)">
            <input type="text" id="username" placeholder="Username" required>
            <input type="password" id="password" placeholder="Password" required>
            <button type="submit">Login</button>
            <p id="error-message" class="error-message">Incorrect username or password</p>
        </form>
    </div>
</body>
</html>
