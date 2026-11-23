# for-my-cintaku
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For My Cintaku ❤️</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    background: radial-gradient(circle, #17102d, #050816 75%);
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    font-family: cursive;
}

.container {
    width: 100%;
    text-align: center;
}

.heart {
    width: min(90vw, 380px);
    overflow: visible;
    animation: pulse 2s ease-in-out infinite 3s;
}

.heart-path {
    fill: none;
    stroke: #ff2e88;
    stroke-width: 5;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-dasharray: 1000;
    stroke-dashoffset: 1000;
    filter:
        drop-shadow(0 0 5px #ff2e88)
        drop-shadow(0 0 15px #ff2e88)
        drop-shadow(0 0 35px #ff2e88)
        drop-shadow(0 0 60px #ff2e88);
    animation: draw 3s ease forwards;
}

.photo {
    opacity: 0;
    animation: appear 2s ease forwards 3s;
}

.love {
    fill: white;
    font-size: 22px;
    text-anchor: middle;
    opacity: 0;
    filter:
        drop-shadow(0 0 8px #ff2e88)
        drop-shadow(0 0 15px #ff2e88);
    animation: appear 2s ease forwards 3.5s;
}

.subtitle {
    color: #ffb5d5;
    font-size: 14px;
    margin-top: 10px;
    opacity: 0;
    animation: appear 2s ease forwards 4s;
}

@keyframes draw {
    to { stroke-dashoffset: 0; }
}

@keyframes appear {
    to { opacity: 1; }
}

@keyframes pulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.06); }
}
</style>
</head>

<body>

<div class="container">

<svg class="heart" viewBox="0 0 320 320">

    <defs>
        <clipPath id="photoClip">
            <circle cx="160" cy="130" r="42"/>
        </clipPath>
    </defs>

    <!-- FOTO DI TENGAH -->
    <image
        class="photo"
        href="foto.jpg"
        x="118"
        y="88"
        width="84"
        height="84"
        preserveAspectRatio="xMidYMid slice"
        clip-path="url(#photoClip)"
    />

    <!-- LINGKARAN FOTO -->
    <circle
        cx="160"
        cy="130"
        r="44"
        fill="none"
        stroke="#ff75b7"
        stroke-width="2"
        filter="drop-shadow(0 0 8px #ff2e88)"
        class="photo"
    />

    <!-- BENTUK HATI -->
    <path
        class="heart-path"
        d="
        M160 280
        C130 255 25 185 25 105
        C25 35 115 20 160 90
        C205 20 295 35 295 105
        C295 185 190 255 160 280
        Z
        "
    />

    <!-- TULISAN -->
    <text x="160" y="205" class="love">
        I Love You ❤️
    </text>

</svg>

<div class="subtitle">
    You are my favorite person ✨
</div>

</div>

</body>
</html>
