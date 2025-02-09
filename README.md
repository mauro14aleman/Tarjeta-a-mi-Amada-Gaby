<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lo Siento, Mi Amor</title>
    <style>
        body {
            background-color: #121212;
            color: #ffd700;
            font-family: 'Pacifico', cursive;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
            position: relative;
        }
        h1 {
            font-size: 3rem;
            text-shadow: 0 0 10px #ffcc00, 0 0 20px #ff9900;
            animation: glow 1.5s infinite alternate;
        }
        p {
            font-size: 1.5rem;
            max-width: 80%;
            margin: 10px auto;
            color: #fff;
            text-shadow: 0 0 5px #ffd700;
        }
        @keyframes glow {
            0% { text-shadow: 0 0 10px #ffcc00, 0 0 20px #ff9900; }
            100% { text-shadow: 0 0 20px #ffcc00, 0 0 30px #ff6600; }
        }
        .hearts {
            position: absolute;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }
        .heart {
            position: absolute;
            width: 30px;
            height: 30px;
            background: url('https://i.imgur.com/ZbWb9OJ.png'); /* Imagen de corazón */
            background-size: cover;
            opacity: 0;
            animation: pop 3s ease-in-out;
        }
        @keyframes pop {
            0% { transform: scale(0.5); opacity: 0; }
            50% { transform: scale(1.2); opacity: 1; }
            100% { transform: scale(1); opacity: 0; }
        }
        .video-container {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="hearts"></div>
    <h1>Mi amada novia Jensi, lamento si de alguna manera siempre causo disgustos en tu persona. 💛</h1>
    <p>Eres mi paz, mi amor y mi refugio. Nada cambiará cuánto te quiero. Lo que más deseo es hacerte muy feliz y que sientas lo importante que eres para mí. 💖</p>
    <p>Siempre estaré aquí para ti, pase lo que pase. Tú eres mi hogar. 🏡💕</p>
    <div class="video-container">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/q9ZAnJ5C9xA?autoplay=1" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>
    <script>
        function createHeart() {
            let heart = document.createElement("div");
            heart.className = "heart";
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.top = Math.random() * 100 + "vh";
            document.querySelector(".hearts").appendChild(heart);
            setTimeout(() => heart.remove(), 3000);
        }
        
        setInterval(createHeart, 1000);
        
        document.body.addEventListener("click", createHeart);
    </script>
</body>
</html>

</html>
