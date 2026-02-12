<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Querés ser mi San Valentín?</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #ffebee;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
            text-align: center;
        }
        .card {
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            z-index: 10;
        }
        h1 {
            color: #d32f2f;
            font-size: 2rem;
            margin-bottom: 20px;
        }
        .btn {
            background-color: #ff4081;
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.2rem;
            border-radius: 50px;
            cursor: pointer;
            transition: transform 0.3s;
            text-decoration: none;
            display: inline-block;
        }
        .btn:hover {
            transform: scale(1.1);
            background-color: #f50057;
        }
        /* Corazones animados */
        .heart {
            position: absolute;
            color: #ff8a80;
            animation: fall linear infinite;
        }
        @keyframes fall {
            to { transform: translateY(100vh) rotate(360deg); }
        }
    </style>
</head>
<body>

    <div class="card">
        <img src="https://cdn-icons-png.flaticon.com/512/838/838610.png" alt="Corazón" width="100">
        <h1>¿Querés ser mi San Valentín? ❤️</h1>
        <p>Haceme la persona más feliz del mundo.</p>
        <button class="btn" onclick="alert('¡Sabía que ibas a decir que sí! 😍 Te amo.')">¡SÍ! 💖</button>
    </div>

    <script>
        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '❤️';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = Math.random() * 3 + 2 + 's';
            heart.style.fontSize = Math.random() * 20 + 10 + 'px';
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 5000);
        }
        setInterval(createHeart, 300);
    </script>
</body>
</html>
