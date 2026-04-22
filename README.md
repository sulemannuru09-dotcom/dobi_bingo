<!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Dobi Bingo</title>
    <style>
        body { background: #1a1a2e; color: white; font-family: sans-serif; margin: 0; padding: 10px; overflow-x: hidden; }
        .header-stats { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; margin-bottom: 20px; }
        .stat-box { background: #2d2d44; padding: 10px; border-radius: 8px; text-align: center; }
        .label { font-size: 10px; color: #aaa; display: block; }
        .val { font-size: 16px; font-weight: bold; color: #4ecca3; }

        .grid-container { 
            display: grid; grid-template-columns: repeat(8, 1fr); gap: 6px; 
            background: rgba(255,255,255,0.03); padding: 10px; border-radius: 12px;
            max-height: 450px; overflow-y: auto;
        }
        .num-btn { background: #3d3d5c; color: white; border: 1px solid #555; padding: 12px 0; border-radius: 6px; font-weight: bold; font-size: 13px; }
        .num-btn:active { background: #e94560; }

        .nav-bar { position: fixed; bottom: 0; left: 0; width: 100%; background: #16213e; display: flex; justify-content: space-around; padding: 12px 0; border-top: 1px solid #333; }
        .nav-item { font-size: 10px; color: #888; text-align: center; }
        .active { color: #4ecca3; }
    </style>
</head>
<body>
    <div class="header-stats">
        <div class="stat-box"><span class="label">Main Wallet</span><span class="val">0</span></div>
        <div class="stat-box"><span class="label">Play Wallet</span><span class="val">0</span></div>
        <div class="stat-box"><span class="label">Stake</span><span class="val">10</span></div>
    </div>

    <div class="grid-container" id="bingoGrid"></div>

    <div style="height: 70px;"></div>

    <div class="nav-bar">
        <div class="nav-item active">🎮<br>Game</div>
        <div class="nav-item">🕒<br>History</div>
        <div class="nav-item">💰<br>Wallet</div>
        <div class="nav-item">👤<br>Profile</div>
    </div>

    <script>
        const grid = document.getElementById('bingoGrid');
        for (let i = 1; i <= 100; i++) {
            const b = document.createElement('button');
            b.className = 'num-btn';
            b.innerText = i;
            b.onclick = () => alert("ካርቴላ ቁጥር " + i + " ተመርጧል!");
            grid.appendChild(b);
        }
    </script>
</body>
</html>
