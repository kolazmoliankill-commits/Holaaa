<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Leslie ✨</title>
    <style>
        body, html {
            margin: 0; padding: 0;
            width: 100%; height: 100%;
            display: flex; justify-content: center; align-items: center;
            background: #000; /* Fondo negro para que resalten los colores */
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
        }

        /* FONDO DINÁMICO DE COLORES */
        #bg-color {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle, #ff80ab 0%, #ad1457 100%);
            transition: all 2s ease;
            z-index: -2;
        }

        /* ESTRELLAS DE LA GALAXIA */
        #stars-container {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            display: none; z-index: -1;
        }

        .star {
            position: absolute; background: white; border-radius: 50%;
            animation: fall linear infinite;
        }

        @keyframes fall {
            from { transform: translateY(-10vh); opacity: 1; }
            to { transform: translateY(110vh); opacity: 0; }
        }

        #container { text-align: center; width: 100%; z-index: 10; }

        .item { display: none; }

        /* FLORES REALES CON BRILLO */
        .flores {
            width: 280px;
            filter: drop-shadow(0 0 30px rgba(255, 255, 255, 0.8));
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) scale(1); }
            50% { transform: translateY(-20px) scale(1.05); }
        }

        /* ZOOM MASIVO DEL CORAZÓN */
        .mega-zoom {
            animation: zoomFinal 2s forwards, heartbeat 0.8s infinite 2s;
        }

        @keyframes zoomFinal {
            0% { transform: scale(0) rotate(-45deg); opacity: 0; }
            100% { transform: scale(5) rotate(0deg); opacity: 1; filter: drop-shadow(0 0 50px #ff1744); }
        }

        @keyframes heartbeat {
            0%, 100% { transform: scale(5); }
            50% { transform: scale(5.5); }
        }

        /* TEXTOS */
        .texto {
            font-size: 35px; color: white; font-weight: bold;
            text-shadow: 0 0 15px rgba(0,0,0,0.5); margin-top: 20px;
            animation: pop 0.5s ease-out;
        }

        .texto-galaxia {
            color: #ffeb3b; font-size: 18px; letter-spacing: 5px;
            margin-top: 60px; text-transform: uppercase;
        }

        @keyframes pop {
            0% { transform: scale(0); } 100% { transform: scale(1); }
        }

        /* BOTÓN DESCUBRIR */
        #btn-main {
            background: linear-gradient(45deg, #ff4081, #ff80ab);
            color: white; border: none; padding: 20px 50px;
            border-radius: 50px; font-size: 22px; font-weight: bold;
            cursor: pointer; box-shadow: 0 10px 30px rgba(255, 64, 129, 0.5);
            transition: 0.3s;
        }

        #btn-main:hover { transform: scale(1.1); }
    </style>
</head>
<body>

    <div id="bg-color"></div>
    <div id="stars-container"></div>

    <div id="container">
        <div id="s1" class="item">
            <div style="font-size: 120px;">🎁</div>
            <div class="texto">¡Algo para ti!</div>
        </div>
        
        <div id="s2" class="item">
            <img src="https://i.ibb.co/Vp6qH8S/flowers-aesthetic.png" class="flores">
            <div style="font-size: 60px;">🍫</div>
            <div class="texto">Eres la mejor</div>
        </div>

        <div id="s3" class="item">
            <div id="heart" style="font-size: 80px; color: #ff1744;">❤️</div>
            <div class="texto-galaxia">¡TE AMO LESLIE! ✨</div>
        </div>

        <div style="margin-top: 50px;">
            <button id="btn-main">Descubrir</button>
        </div>
    </div>

    <script>
        let step = 0;
        const btn = document.getElementById('btn-main');
        const bg = document.getElementById('
        
