# sitio web
mkdir mi-sitio-web && cd mi-sitio-web && echo '<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sitio Web con Fases</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: Arial, sans-serif; }
        body { background: linear-gradient(135deg, #1e3c72, #2a5298); min-height: 100vh; display: flex; justify-content: center; align-items: center; color: white; text-align: center; }
        .container { background: rgba(255, 255, 255, 0.1); padding: 2rem; border-radius: 15px; box-shadow: 0 0 20px rgba(0, 0, 0, 0.3); max-width: 90%; width: 500px; }
        h1 { font-size: 2.5rem; margin-bottom: 1rem; }
        .timer { font-size: 2rem; margin: 1rem 0; }
        .skip-btn { background: #4CAF50; color: white; border: none; padding: 0.8rem 2rem; border-radius: 25px; cursor: pointer; font-size: 1rem; margin-top: 1rem; transition: background 0.3s; }
        .skip-btn:hover { background: #45a049; }
    </style>
</head>
<body>
    <div class="container">
        <h1>Fase <span id="phase-number">1</span>/4</h1>
        <div class="timer" id="timer">10</div>
        <button class="skip-btn" onclick="skipPhase()">Saltar Fase</button>
    </div>
    <script>
        let currentPhase = 1; let timeLeft = 10; const totalPhases = 4;
        const phaseNumber = document.getElementById("phase-number");
        const timerElement = document.getElementById("timer");
        function startTimer() { const timer = setInterval(() => { timeLeft--; timerElement.textContent = timeLeft; if (timeLeft <= 0) { clearInterval(timer); nextPhase(); } }, 1000); }
        function nextPhase() { if (currentPhase < totalPhases) { currentPhase++; timeLeft = 10; phaseNumber.textContent = currentPhase; startTimer(); } else { window.location.href = "https://mega.nz/TU_ENLACE_AQUI"; } }
        function skipPhase() { nextPhase(); } startTimer();
    </script>
</body>
</html>' > index.html

