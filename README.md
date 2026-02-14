<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RBA - Real Basketball Association</title>

<style>
html { scroll-behavior: smooth; }

body {
    margin: 0;
    font-family: 'Arial Black', Arial, sans-serif;
    background: #0d0d0d;
    color: white;
    overflow-x: hidden;
    position: relative;
}

/* MOVING BACKGROUND LIGHTS */
@keyframes moveGradient {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
}
.body-bg {
    position: fixed;
    top:0; left:0; width:100%; height:100%;
    background: linear-gradient(270deg, #1a1a1a, #111, #000, #111);
    background-size: 800% 800%;
    animation: moveGradient 30s ease infinite;
    z-index: -2;
}

/* FLOATING BASKETBALLS */
@keyframes floatBall {
    0% {transform: translateY(100vh) rotate(0deg);}
    100% {transform: translateY(-100px) rotate(360deg);}
}
.basketball {
    position: fixed;
    font-size: 50px;
    animation: floatBall linear infinite;
    opacity: 0.7;
    z-index: -1;
    pointer-events: none;
}

/* HEADER */
.top-header {
    background: #000;
    padding: 18px 30px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 4px solid #c8102e;
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo { font-size: 26px; font-weight: bold; letter-spacing: 2px; }
.nav-links a { margin-left: 25px; font-size: 14px; color: #aaa; transition:0.3s; }
.nav-links a:hover { color: #fff; }

/* BREAKING */
.breaking {
    background: #c8102e;
    padding: 12px 25px;
    font-weight: bold;
    display: flex;
    align-items: center;
    gap: 10px;
}
.breaking span {
    background: black;
    padding: 5px 8px;
    font-size: 12px;
    animation: pulse 1s infinite;
}
@keyframes pulse { 0%{opacity:1;}50%{opacity:0.5;}100%{opacity:1;} }

/* HERO */
.hero {
    padding: 80px 30px;
    background: radial-gradient(circle at top left, #1a1a1a, #000);
}
.hero h1 { font-size: 52px; margin:0; color:#fff; }
.hero p { margin-top:15px; font-size:18px; color:#ccc; max-width:700px; }
.join-btn {
    display: inline-block;
    margin-top:20px;
    padding: 14px 30px;
    background: #7289da;
    color: white;
    font-weight: bold;
    border-radius: 8px;
    transition: 0.3s;
    font-size: 16px;
}
.join-btn:hover { background:#5b6eae; transform: scale(1.05); }

/* NEWS */
.news-container {
    padding: 40px 30px;
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(300px,1fr));
    gap:25px;
}
.news-card {
    background:#111; padding:25px; border-radius:10px; transition:0.3s; cursor:pointer;
    border:1px solid #222;
}
.news-card:hover { transform: scale(1.03); background:#1c1c1c; border:1px solid #c8102e; }
.news-card h3 { margin-top:0; color:#c8102e; }

/* PLAYER SPOTLIGHT */
.player-section { padding:60px 30px; background:#000; }
.player-section h2 { font-size:30px; margin-bottom:20px; }
.player-card {
    background: linear-gradient(to right, #98002E, #000);
    padding:25px; border-radius:12px; max-width:450px;
    transition:0.3s; cursor:pointer;
}
.player-card:hover { transform: translateY(-8px); }
.player-card h3 { margin:0; }
.stat { margin:6px 0; }

/* FOOTER */
footer { padding:25px; text-align:center; background:#000; border-top:2px solid #111; color:#777; }

/* MOBILE */
@media(max-width:700px){
    .hero h1{ font-size:32px; }
    .nav-links{ display:none; }
}
</style>
</head>
<body>

<div class="body-bg"></div>

<!-- FLOATING BASKETBALLS USING EMOJI -->
<div class="basketball" style="left:10%; animation-duration:18s;">🏀</div>
<div class="basketball" style="left:25%; font-size:40px; animation-duration:22s;">🏀</div>
<div class="basketball" style="left:45%; font-size:60px; animation-duration:20s;">🏀</div>
<div class="basketball" style="left:65%; font-size:35px; animation-duration:25s;">🏀</div>
<div class="basketball" style="left:80%; font-size:50px; animation-duration:17s;">🏀</div>

<div class="top-header">
    <div class="logo">RBA NETWORK 🏀</div>
    <div class="nav-links">
        <a href="#home">HOME</a>
        <a href="#news">NEWS</a>
        <a href="#players">PLAYERS</a>
    </div>
</div>

<div class="breaking">
    <span>LIVE</span>
    Jay requests trade • Lakers & Knicks aggressively pursuing
</div>

<div class="hero" id="home">
    <h1>JAY SHOCKS THE LEAGUE</h1>
    <p>
    Golden State Warriors star Jay formally requests trade, sending shockwaves across the RBA. Multiple contenders already positioning offers.
    </p>
    <a href="https://discord.gg/nQ7jsPYgtM" target="_blank" class="join-btn">Join Discord</a>
</div>

<div class="news-container" id="news">
    <div class="news-card">
        <h3>Trade Fallout Begins</h3>
        <p>Front offices react as the league braces for a major shift.</p>
    </div>
    <div class="news-card">
        <h3>Tim Returns From Retirement</h3>
        <p>Minnesota adds veteran firepower ahead of playoffs.</p>
    </div>
    <div class="news-card">
        <h3>Power Rankings Update</h3>
        <p>Contenders separate themselves from the pack.</p>
    </div>
</div>

<div class="player-section" id="players">
    <h2>⭐ Player Spotlight</h2>
    <div class="player-card">
        <h3>iTxser ⭐⭐⭐⭐⭐</h3>
        <p>Miami Heat 🔴</p>
        <div class="stat">PPG: 41</div>
        <div class="stat">FG%: 100%</div>
        <div class="stat">APG: 11</div>
        <div class="stat">SPG: 4</div>
        <p>🔥 Scoring Machine</p>
    </div>
</div>

<footer>
© 2026 RBA Network • Real Basketball Association
</footer>
</body>
</html>
