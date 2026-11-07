---
permalink: /puzzles/2025/
title: "Christmas Codebreak 2025 — Psychology"
---

<style>
  body { margin:0; }
  .cb-game { color:#1c1a17; font-family: Georgia, 'Times New Roman', serif; }
  .wrap { max-width:1180px; margin:0 auto; padding:20px 14px 40px; }
  .cb-game h1 { font-size:1.55rem; margin:.2em 0 .35em; }
  .cb-game p.intro { max-width:72ch; line-height:1.45; }
  .cb-game .bar { display:flex; flex-wrap:wrap; gap:10px; align-items:center; margin:14px 0 6px; }
  .cb-game .clock { font-size:1.9rem; font-variant-numeric:tabular-nums; background:#fffdf6; border:2px solid #1c1a17; padding:2px 14px; border-radius:4px; min-width:130px; text-align:center; }
  .cb-game button { font:inherit; background:#fffdf6; border:2px solid #1c1a17; border-radius:4px; padding:5px 12px; cursor:pointer; }
  .cb-game button:hover { background:#efe7d3; }
  .cb-game #status { font-style:italic; }
  .cb-game #warn { display:none; margin:10px 0; padding:9px 13px; border-radius:4px; font-weight:bold; }
  .cb-game #warn.warn { display:block; background:#fbe3e0; border:2px solid #b3372a; color:#7c1d12; }
  .cb-game #warn.info { display:block; background:#fdf3d8; border:2px solid #a97b12; color:#6b4d08; }
  .cb-game .stage { display:flex; gap:18px; align-items:flex-start; margin-top:12px; }
  .cb-game .key { background:#fffdf6; border:2.5px solid #1c1a17; border-collapse:collapse; flex:0 0 auto; }
  .cb-game .key th, .cb-game .key td { border:1.5px solid #1c1a17; text-align:center; padding:0; }
  .cb-game .key th { font-family:'Bradley Hand','Segoe Print','Comic Sans MS',cursive; font-size:1.05rem; padding:3px 8px; }
  .cb-game .key td.letter { font-family:'Bradley Hand','Segoe Print','Comic Sans MS',cursive; font-size:1.15rem; width:34px; height:27px; }
  .cb-game .key td.c2h, .cb-game .key td.c2 { border-left:3px dashed #1c1a17; }
  .cb-game .key input { width:40px; height:27px; border:0; background:transparent; text-align:center; font:inherit; font-size:1.02rem; padding:0; }
  .cb-game .key input:focus { outline:2.5px solid #2b50c8; outline-offset:-2.5px; background:#eaf0ff; }
  .cb-game .key input.locked { font-weight:bold; color:#444; }
  .cb-game .key input.err { background:#f8d7d2; }
  .cb-game .key caption { caption-side:top; text-align:left; font-style:italic; padding-bottom:5px; }
  .cb-game .art { position:relative; flex:1 1 auto; min-width:0; border:2.5px solid #1c1a17; background:#fff; line-height:0; }
  .cb-game .art img { width:100%; height:auto; display:block; }
  .cb-game .cell { position:absolute; width:2.45%; height:3.42%; transform:translate(-50%,-50%); display:flex; align-items:center; justify-content:center; cursor:text; line-height:1; }
  .cb-game .cell .ch { font-family:'Bradley Hand','Segoe Print','Comic Sans MS',cursive; font-size:var(--chfs, 14px); color:#20306e; pointer-events:none; }
  .cb-game .cell.hl { background:rgba(255,205,55,.38); }
  .cb-game .cell.sel { box-shadow:0 0 0 2.5px #b3372a inset; background:rgba(255,205,55,.25); }
  .cb-game .cell.sel::after { content:''; width:2px; height:62%; background:#b3372a; animation:cbblink 1s steps(1) infinite; margin-left:1px; }
  @keyframes cbblink { 50% { opacity:0; } }
  .cb-game .cell .dot { position:absolute; top:1px; left:1px; width:4px; height:4px; border-radius:50%; background:#d9930d; pointer-events:none; }
  .cb-game .foot { margin-top:14px; font-size:.92rem; font-style:italic; max-width:72ch; }
  @media (max-width:760px){ .cb-game .stage{flex-direction:column;} .cb-game .art{order:-1; width:100%; flex:none;} .cb-game .key{align-self:center;} }
</style>

<div class="cb-game">
<div class="bar">
  <div class="clock" id="clock">0:00</div>
<div id="warn" role="alert"></div>
<div class="stage">
  <table class="key" id="keyTable" aria-label="Cipher key">
    
    <tr><th>&Omega;</th><th>C&sup1;</th><th class="c2h">C&sup2;</th></tr>
  </table>
  <div class="art" id="art">
    <img src="/assets/images/puzzle-2025-bg.png" alt="The hand-drawn 2025 Christmas codebreak lattice">
  </div>
</div>
</div>
<input id="kbd" type="text" autocomplete="off" style="position:fixed;opacity:0;pointer-events:none;bottom:0;left:0;height:1px;width:1px;">

<script>
const CELLS = [{"n": 8, "s": 0, "u": 0, "g": null, "x": 0.132, "y": 7.978}, {"n": 4, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 11.461}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 4.048, "y": 11.461}, {"n": 22, "s": 0, "u": 0, "g": null, "x": 6.64, "y": 11.461}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 8.73, "y": 11.461}, {"n": 1, "s": 0, "u": 0, "g": null, "x": 21.032, "y": 11.461}, {"n": 18, "s": 1, "u": 0, "g": null, "x": 90.767, "y": 11.461}, {"n": 10, "s": 1, "u": 0, "g": null, "x": 93.175, "y": 11.461}, {"n": 23, "s": 1, "u": 0, "g": null, "x": 95.582, "y": 11.461}, {"n": 21, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 14.794}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 17.063, "y": 14.794}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 21.746, "y": 14.794}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 37.381, "y": 14.794}, {"n": 21, "s": 1, "u": 0, "g": null, "x": 60.423, "y": 14.794}, {"n": 3, "s": 1, "u": 0, "g": null, "x": 65.741, "y": 14.794}, {"n": 13, "s": 1, "u": 0, "g": null, "x": 71.508, "y": 14.794}, {"n": 16, "s": 1, "u": 0, "g": null, "x": 81.138, "y": 14.794}, {"n": 2, "s": 1, "u": 0, "g": null, "x": 85.952, "y": 14.794}, {"n": 25, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 18.202}, {"n": 1, "s": 0, "u": 0, "g": null, "x": 2.989, "y": 18.202}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 5.608, "y": 18.202}, {"n": 4, "s": 0, "u": 0, "g": null, "x": 8.73, "y": 18.202}, {"n": 22, "s": 0, "u": 0, "g": null, "x": 11.323, "y": 18.202}, {"n": 1, "s": 0, "u": 0, "g": null, "x": 14.471, "y": 18.202}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 17.063, "y": 18.202}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 21.746, "y": 18.202}, {"n": 16, "s": 0, "u": 0, "g": null, "x": 25.926, "y": 18.202}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 40.529, "y": 18.202}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 43.122, "y": 18.202}, {"n": 22, "s": 0, "u": 0, "g": null, "x": 45.741, "y": 18.202}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 48.333, "y": 18.202}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 50.423, "y": 18.202}, {"n": 17, "s": 1, "u": 0, "g": null, "x": 58.995, "y": 18.202}, {"n": 13, "s": 1, "u": 0, "g": null, "x": 63.81, "y": 18.202}, {"n": 3, "s": 1, "u": 0, "g": null, "x": 69.101, "y": 18.202}, {"n": 6, "s": 1, "u": 0, "g": null, "x": 86.905, "y": 18.202}, {"n": 3, "s": 1, "u": 0, "g": null, "x": 93.175, "y": 18.202}, {"n": 23, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 21.835}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 17.063, "y": 21.835}, {"n": 14, "s": 0, "u": 0, "g": null, "x": 22.804, "y": 21.835}, {"n": 3, "s": 0, "u": 0, "g": null, "x": 25.926, "y": 21.835}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 29.048, "y": 21.835}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 31.667, "y": 21.835}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 34.788, "y": 21.835}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 37.381, "y": 21.835}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 43.122, "y": 21.835}, {"n": 9, "s": 1, "u": 0, "g": null, "x": 58.995, "y": 21.835}, {"n": 8, "s": 1, "u": 0, "g": null, "x": 64.286, "y": 21.835}, {"n": 8, "s": 1, "u": 0, "g": null, "x": 69.577, "y": 21.835}, {"n": 7, "s": 1, "u": 0, "g": null, "x": 75.37, "y": 21.835}, {"n": 2, "s": 1, "u": 0, "g": null, "x": 81.138, "y": 21.835}, {"n": 16, "s": 1, "u": 0, "g": null, "x": 86.429, "y": 21.835}, {"n": 16, "s": 0, "u": 0, "g": null, "x": 5.079, "y": 25.318}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 22.804, "y": 25.318}, {"n": 10, "s": 0, "u": 0, "g": null, "x": 27.487, "y": 25.318}, {"n": 6, "s": 0, "u": 0, "g": null, "x": 40.529, "y": 25.318}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 47.804, "y": 25.318}, {"n": 18, "s": 1, "u": 0, "g": null, "x": 53.307, "y": 25.318}, {"n": 8, "s": 1, "u": 1, "g": null, "x": 52.249, "y": 25.318}, {"n": 16, "s": 1, "u": 0, "g": null, "x": 58.519, "y": 25.318}, {"n": 22, "s": 1, "u": 0, "g": null, "x": 72.46, "y": 25.318}, {"n": 10, "s": 1, "u": 1, "g": null, "x": 89.815, "y": 25.318}, {"n": 23, "s": 1, "u": 0, "g": null, "x": 94.63, "y": 25.318}, {"n": 15, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 28.801}, {"n": 6, "s": 0, "u": 0, "g": null, "x": 2.989, "y": 28.801}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 6.111, "y": 28.801}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 9.762, "y": 28.801}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 12.884, "y": 28.801}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 16.032, "y": 28.801}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 18.624, "y": 28.801}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 23.307, "y": 28.801}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 27.487, "y": 28.801}, {"n": 1, "s": 0, "u": 0, "g": null, "x": 32.698, "y": 28.801}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 35.317, "y": 28.801}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 38.439, "y": 28.801}, {"n": 10, "s": 0, "u": 0, "g": null, "x": 41.032, "y": 28.801}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 43.651, "y": 28.801}, {"n": 1, "s": 0, "u": 0, "g": null, "x": 46.772, "y": 28.801}, {"n": 3, "s": 1, "u": 0, "g": null, "x": 52.275, "y": 28.801}, {"n": 1, "s": 1, "u": 0, "g": null, "x": 59.947, "y": 28.801}, {"n": 21, "s": 1, "u": 0, "g": null, "x": 65.238, "y": 28.801}, {"n": 3, "s": 1, "u": 1, "g": null, "x": 85.952, "y": 28.801}, {"n": 10, "s": 1, "u": 0, "g": null, "x": 92.222, "y": 28.801}, {"n": 4, "s": 0, "u": 0, "g": null, "x": 6.111, "y": 32.285}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 27.487, "y": 32.285}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 46.772, "y": 32.285}, {"n": 8, "s": 1, "u": 0, "g": null, "x": 57.54, "y": 32.285}, {"n": 10, "s": 1, "u": 0, "g": null, "x": 62.831, "y": 32.285}, {"n": 4, "s": 1, "u": 1, "g": null, "x": 65.238, "y": 32.285}, {"n": 2, "s": 1, "u": 0, "g": null, "x": 68.624, "y": 32.285}, {"n": 1, "s": 1, "u": 1, "g": null, "x": 73.915, "y": 32.285}, {"n": 6, "s": 1, "u": 1, "g": null, "x": 79.206, "y": 32.285}, {"n": 0, "s": 1, "u": 1, "g": null, "x": 84.021, "y": 32.285}, {"n": 7, "s": 1, "u": 0, "g": null, "x": 91.72, "y": 32.285}, {"n": 5, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 35.805}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 2.46, "y": 35.805}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 5.608, "y": 35.805}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 8.201, "y": 35.805}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 10.82, "y": 35.805}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 13.413, "y": 35.805}, {"n": 10, "s": 0, "u": 0, "g": null, "x": 15.503, "y": 35.805}, {"n": 3, "s": 0, "u": 0, "g": null, "x": 20.714, "y": 35.805}, {"n": 24, "s": 0, "u": 0, "g": null, "x": 24.365, "y": 35.805}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 26.958, "y": 35.805}, {"n": 4, "s": 0, "u": 0, "g": null, "x": 30.106, "y": 35.805}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 32.698, "y": 35.805}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 35.317, "y": 35.805}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 37.91, "y": 35.805}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 40.529, "y": 35.805}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 43.122, "y": 35.805}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 45.212, "y": 35.805}, {"n": 9, "s": 1, "u": 0, "g": null, "x": 53.307, "y": 35.805}, {"n": 6, "s": 1, "u": 1, "g": null, "x": 58.519, "y": 35.805}, {"n": 9, "s": 1, "u": 0, "g": null, "x": 63.81, "y": 35.805}, {"n": 8, "s": 1, "u": 1, "g": null, "x": 68.148, "y": 35.805}, {"n": 2, "s": 1, "u": 1, "g": null, "x": 73.439, "y": 35.805}, {"n": 1, "s": 1, "u": 0, "g": null, "x": 78.73, "y": 35.805}, {"n": 1, "s": 1, "u": 0, "g": null, "x": 83.545, "y": 35.805}, {"n": 24, "s": 1, "u": 0, "g": null, "x": 89.815, "y": 35.805}, {"n": 8, "s": 1, "u": 0, "g": null, "x": 92.698, "y": 35.805}, {"n": 11, "s": 1, "u": 0, "g": null, "x": 95.582, "y": 35.805}, {"n": 26, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 39.326}, {"n": 9, "s": 0, "u": 0, "g": null, "x": 5.608, "y": 39.326}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 10.82, "y": 39.326}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 20.714, "y": 39.326}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 45.212, "y": 39.326}, {"n": 9, "s": 1, "u": 0, "g": null, "x": 53.307, "y": 39.326}, {"n": 23, "s": 1, "u": 1, "g": null, "x": 65.238, "y": 39.326}, {"n": 8, "s": 1, "u": 1, "g": null, "x": 81.138, "y": 39.326}, {"n": 5, "s": 1, "u": 1, "g": null, "x": 86.905, "y": 39.326}, {"n": 18, "s": 1, "u": 1, "g": null, "x": 92.222, "y": 39.326}, {"n": 13, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 42.734}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 5.608, "y": 42.734}, {"n": 10, "s": 0, "u": 0, "g": null, "x": 10.82, "y": 42.734}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 16.032, "y": 42.734}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 20.714, "y": 42.734}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 23.836, "y": 42.734}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 26.455, "y": 42.734}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 29.577, "y": 42.734}, {"n": 10, "s": 0, "u": 0, "g": null, "x": 32.169, "y": 42.734}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 34.788, "y": 42.734}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 37.381, "y": 42.734}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 40.0, "y": 42.734}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 42.593, "y": 42.734}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 45.212, "y": 42.734}, {"n": 19, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 46.255}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 6.64, "y": 46.255}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 12.381, "y": 46.255}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 17.063, "y": 46.255}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 22.804, "y": 46.255}, {"n": 1, "s": 0, "u": 0, "g": null, "x": 27.487, "y": 46.255}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 34.259, "y": 46.255}, {"n": 2, "s": 1, "u": 0, "g": null, "x": 53.307, "y": 46.255}, {"n": 10, "s": 1, "u": 0, "g": null, "x": 60.423, "y": 46.255}, {"n": 7, "s": 1, "u": 1, "g": null, "x": 65.741, "y": 46.255}, {"n": 5, "s": 1, "u": 1, "g": null, "x": 70.556, "y": 46.255}, {"n": 1, "s": 1, "u": 0, "g": null, "x": 80.185, "y": 46.255}, {"n": 15, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 49.738}, {"n": 12, "s": 0, "u": 0, "g": null, "x": 6.64, "y": 49.738}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 12.381, "y": 49.738}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 14.471, "y": 49.738}, {"n": 14, "s": 0, "u": 0, "g": null, "x": 17.063, "y": 49.738}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 22.804, "y": 49.738}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 27.487, "y": 49.738}, {"n": 6, "s": 0, "u": 0, "g": null, "x": 34.259, "y": 49.738}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 36.349, "y": 49.738}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 38.968, "y": 49.738}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 41.561, "y": 49.738}, {"n": 19, "s": 0, "u": 0, "g": null, "x": 44.153, "y": 49.738}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 46.243, "y": 49.738}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 48.333, "y": 49.738}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 50.423, "y": 49.738}, {"n": 5, "s": 1, "u": 0, "g": null, "x": 67.646, "y": 49.738}, {"n": 7, "s": 1, "u": 0, "g": null, "x": 82.09, "y": 49.738}, {"n": 6, "s": 1, "u": 1, "g": null, "x": 85.952, "y": 49.738}, {"n": 4, "s": 1, "u": 0, "g": null, "x": 90.767, "y": 49.738}, {"n": 1, "s": 0, "u": 0, "g": null, "x": 0.899, "y": 53.221}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 2.989, "y": 53.221}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 5.608, "y": 53.221}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 8.201, "y": 53.221}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 10.82, "y": 53.221}, {"n": 10, "s": 0, "u": 0, "g": null, "x": 13.413, "y": 53.221}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 17.063, "y": 53.221}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 22.804, "y": 53.221}, {"n": 6, "s": 0, "u": 0, "g": null, "x": 27.487, "y": 53.221}, {"n": 23, "s": 0, "u": 1, "g": null, "x": 34.259, "y": 53.221}, {"n": 4, "s": 1, "u": 1, "g": null, "x": 59.471, "y": 53.221}, {"n": 6, "s": 1, "u": 1, "g": null, "x": 64.762, "y": 53.221}, {"n": 2, "s": 1, "u": 1, "g": null, "x": 70.053, "y": 53.221}, {"n": 1, "s": 1, "u": 0, "g": null, "x": 80.185, "y": 53.221}, {"n": 10, "s": 0, "u": 0, "g": null, "x": 12.566, "y": 56.704}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 16.005, "y": 56.704}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 21.296, "y": 56.704}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 26.058, "y": 56.704}, {"n": 14, "s": 0, "u": 0, "g": null, "x": 28.439, "y": 56.704}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 30.106, "y": 56.704}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 32.698, "y": 56.704}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 35.317, "y": 56.704}, {"n": 19, "s": 0, "u": 0, "g": null, "x": 37.91, "y": 56.704}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 40.529, "y": 56.704}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 43.651, "y": 56.704}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 46.243, "y": 56.704}, {"n": 18, "s": 1, "u": 0, "g": null, "x": 52.275, "y": 56.704}, {"n": 6, "s": 1, "u": 0, "g": null, "x": 55.132, "y": 56.704}, {"n": 4, "s": 1, "u": 1, "g": null, "x": 86.429, "y": 56.704}, {"n": 23, "s": 1, "u": 1, "g": null, "x": 90.767, "y": 56.704}, {"n": 25, "s": 0, "u": 1, "g": null, "x": 16.005, "y": 60.112}, {"n": 10, "s": 0, "u": 1, "g": null, "x": 21.296, "y": 60.112}, {"n": 3, "s": 1, "u": 1, "g": null, "x": 58.519, "y": 60.112}, {"n": 7, "s": 1, "u": 1, "g": null, "x": 63.81, "y": 60.112}, {"n": 2, "s": 1, "u": 1, "g": null, "x": 69.577, "y": 60.112}, {"n": 1, "s": 1, "u": 0, "g": null, "x": 74.868, "y": 60.112}, {"n": 6, "s": 1, "u": 1, "g": null, "x": 79.683, "y": 60.112}, {"n": 10, "s": 1, "u": 0, "g": null, "x": 84.021, "y": 60.112}, {"n": 3, "s": 1, "u": 1, "g": null, "x": 89.312, "y": 60.112}, {"n": 1, "s": 0, "u": 0, "g": null, "x": 0.899, "y": 63.745}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 2.989, "y": 63.745}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 5.608, "y": 63.745}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 8.201, "y": 63.745}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 10.82, "y": 63.745}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 13.413, "y": 63.745}, {"n": 12, "s": 0, "u": 0, "g": null, "x": 17.063, "y": 63.745}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 21.243, "y": 63.745}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 23.836, "y": 63.745}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 26.455, "y": 63.745}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 29.048, "y": 63.745}, {"n": 6, "s": 0, "u": 0, "g": null, "x": 31.667, "y": 63.745}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 34.259, "y": 63.745}, {"n": 5, "s": 0, "u": 0, "g": null, "x": 36.878, "y": 63.745}, {"n": 12, "s": 0, "u": 0, "g": null, "x": 39.471, "y": 63.745}, {"n": 16, "s": 0, "u": 0, "g": null, "x": 50.132, "y": 63.745}, {"n": 3, "s": 1, "u": 0, "g": null, "x": 53.386, "y": 63.745}, {"n": 1, "s": 1, "u": 0, "g": null, "x": 55.132, "y": 63.745}, {"n": 1, "s": 1, "u": 0, "g": null, "x": 59.947, "y": 63.745}, {"n": 1, "s": 1, "u": 0, "g": null, "x": 86.429, "y": 63.745}, {"n": 10, "s": 1, "u": 0, "g": null, "x": 90.767, "y": 63.745}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 27.381, "y": 67.266}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 45.026, "y": 67.266}, {"n": 10, "s": 0, "u": 0, "g": null, "x": 50.132, "y": 67.266}, {"n": 25, "s": 1, "u": 0, "g": null, "x": 63.81, "y": 67.266}, {"n": 7, "s": 1, "u": 1, "g": null, "x": 69.577, "y": 67.266}, {"n": 10, "s": 1, "u": 0, "g": null, "x": 75.37, "y": 67.266}, {"n": 1, "s": 1, "u": 0, "g": null, "x": 83.545, "y": 67.266}, {"n": 25, "s": 1, "u": 0, "g": null, "x": 88.836, "y": 67.266}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 0.397, "y": 70.712}, {"n": 4, "s": 0, "u": 0, "g": null, "x": 2.989, "y": 70.712}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 5.608, "y": 70.712}, {"n": 1, "s": 0, "u": 0, "g": null, "x": 8.201, "y": 70.712}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 10.82, "y": 70.712}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 13.413, "y": 70.712}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 16.032, "y": 70.712}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 18.624, "y": 70.712}, {"n": 12, "s": 0, "u": 0, "g": null, "x": 21.243, "y": 70.712}, {"n": 3, "s": 0, "u": 0, "g": null, "x": 29.577, "y": 70.712}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 31.667, "y": 70.712}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 33.73, "y": 70.712}, {"n": 9, "s": 0, "u": 0, "g": null, "x": 35.82, "y": 70.712}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 38.439, "y": 70.712}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 44.683, "y": 70.712}, {"n": 9, "s": 0, "u": 0, "g": null, "x": 46.772, "y": 70.712}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 48.862, "y": 70.712}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 50.952, "y": 70.712}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 52.778, "y": 70.712}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 54.894, "y": 70.712}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 57.011, "y": 70.712}, {"n": 12, "s": 0, "u": 0, "g": null, "x": 59.127, "y": 70.712}, {"n": 3, "s": 1, "u": 0, "g": null, "x": 81.138, "y": 70.712}, {"n": 25, "s": 1, "u": 0, "g": null, "x": 85.952, "y": 70.712}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 0.397, "y": 74.195}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 21.561, "y": 74.195}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 45.026, "y": 74.195}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 50.132, "y": 74.195}, {"n": 8, "s": 1, "u": 1, "g": null, "x": 66.693, "y": 74.195}, {"n": 7, "s": 1, "u": 1, "g": null, "x": 72.963, "y": 74.195}, {"n": 13, "s": 1, "u": 0, "g": null, "x": 79.206, "y": 74.195}, {"n": 21, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 77.715}, {"n": 8, "s": 0, "u": 0, "g": null, "x": 5.079, "y": 77.715}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 7.698, "y": 77.715}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 10.291, "y": 77.715}, {"n": 10, "s": 0, "u": 0, "g": null, "x": 12.884, "y": 77.715}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 15.503, "y": 77.715}, {"n": 14, "s": 0, "u": 0, "g": null, "x": 19.153, "y": 77.715}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 22.275, "y": 77.715}, {"n": 12, "s": 0, "u": 0, "g": null, "x": 24.894, "y": 77.715}, {"n": 5, "s": 0, "u": 0, "g": null, "x": 30.106, "y": 77.715}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 32.698, "y": 77.715}, {"n": 6, "s": 0, "u": 0, "g": null, "x": 35.317, "y": 77.715}, {"n": 3, "s": 0, "u": 0, "g": null, "x": 37.91, "y": 77.715}, {"n": 4, "s": 0, "u": 0, "g": null, "x": 40.529, "y": 77.715}, {"n": 10, "s": 0, "u": 0, "g": null, "x": 43.122, "y": 77.715}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 45.741, "y": 77.715}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 47.804, "y": 77.715}, {"n": 6, "s": 1, "u": 1, "g": null, "x": 52.275, "y": 77.715}, {"n": 20, "s": 1, "u": 0, "g": null, "x": 56.587, "y": 77.715}, {"n": 10, "s": 1, "u": 0, "g": null, "x": 61.402, "y": 77.715}, {"n": 8, "s": 1, "u": 0, "g": null, "x": 66.217, "y": 77.715}, {"n": 4, "s": 1, "u": 0, "g": null, "x": 81.614, "y": 77.715}, {"n": 11, "s": 1, "u": 1, "g": null, "x": 86.905, "y": 77.715}, {"n": 3, "s": 1, "u": 0, "g": null, "x": 91.72, "y": 77.715}, {"n": 15, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 81.199}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 7.169, "y": 81.199}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 19.153, "y": 81.199}, {"n": 5, "s": 0, "u": 0, "g": null, "x": 32.698, "y": 81.199}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 37.91, "y": 81.199}, {"n": 8, "s": 1, "u": 0, "g": null, "x": 73.439, "y": 81.199}, {"n": 26, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 84.719}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 5.079, "y": 84.719}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 7.698, "y": 84.719}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 10.291, "y": 84.719}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 12.884, "y": 84.719}, {"n": 21, "s": 0, "u": 0, "g": null, "x": 15.503, "y": 84.719}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 19.153, "y": 84.719}, {"n": 2, "s": 0, "u": 0, "g": "N", "x": 23.571, "y": 84.719}, {"n": 15, "s": 0, "u": 0, "g": "E", "x": 25.661, "y": 84.719}, {"n": 15, "s": 0, "u": 0, "g": "E", "x": 27.751, "y": 84.719}, {"n": 9, "s": 0, "u": 0, "g": "D", "x": 29.841, "y": 84.719}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 37.91, "y": 84.719}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 41.561, "y": 84.719}, {"n": 16, "s": 0, "u": 0, "g": null, "x": 46.243, "y": 84.719}, {"n": 5, "s": 1, "u": 0, "g": null, "x": 55.608, "y": 84.719}, {"n": 5, "s": 1, "u": 0, "g": null, "x": 60.926, "y": 84.719}, {"n": 4, "s": 1, "u": 1, "g": null, "x": 66.217, "y": 84.719}, {"n": 8, "s": 1, "u": 1, "g": null, "x": 79.683, "y": 84.719}, {"n": 10, "s": 1, "u": 0, "g": null, "x": 85.0, "y": 84.719}, {"n": 7, "s": 1, "u": 1, "g": null, "x": 89.815, "y": 84.719}, {"n": 25, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 88.202}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 7.169, "y": 88.202}, {"n": 9, "s": 0, "u": 1, "g": null, "x": 37.91, "y": 88.202}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 40.529, "y": 88.202}, {"n": 19, "s": 0, "u": 0, "g": null, "x": 43.122, "y": 88.202}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 45.741, "y": 88.202}, {"n": 10, "s": 0, "u": 0, "g": null, "x": 47.804, "y": 88.202}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 49.894, "y": 88.202}, {"n": 3, "s": 0, "u": 0, "g": null, "x": 51.455, "y": 88.202}, {"n": 3, "s": 1, "u": 0, "g": null, "x": 61.878, "y": 88.202}, {"n": 8, "s": 1, "u": 0, "g": null, "x": 66.693, "y": 88.202}, {"n": 2, "s": 1, "u": 0, "g": null, "x": 73.439, "y": 88.202}, {"n": 3, "s": 1, "u": 0, "g": null, "x": 81.138, "y": 88.202}, {"n": 7, "s": 1, "u": 0, "g": null, "x": 85.952, "y": 88.202}, {"n": 2, "s": 1, "u": 0, "g": null, "x": 90.767, "y": 88.202}, {"n": 15, "s": 0, "u": 0, "g": null, "x": -0.132, "y": 91.61}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 2.989, "y": 91.61}, {"n": 19, "s": 0, "u": 0, "g": null, "x": 5.079, "y": 91.61}, {"n": 12, "s": 0, "u": 0, "g": null, "x": 7.169, "y": 91.61}, {"n": 22, "s": 0, "u": 0, "g": null, "x": 9.762, "y": 91.61}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 12.381, "y": 91.61}, {"n": 13, "s": 0, "u": 0, "g": null, "x": 14.471, "y": 91.61}, {"n": 25, "s": 0, "u": 0, "g": null, "x": 17.063, "y": 91.61}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 19.683, "y": 91.61}, {"n": 24, "s": 0, "u": 0, "g": null, "x": 21.746, "y": 91.61}, {"n": 12, "s": 0, "u": 0, "g": null, "x": 24.365, "y": 91.61}, {"n": 23, "s": 0, "u": 0, "g": null, "x": 26.455, "y": 91.61}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 29.048, "y": 91.61}, {"n": 22, "s": 0, "u": 0, "g": null, "x": 31.138, "y": 91.61}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 37.91, "y": 91.61}, {"n": 15, "s": 0, "u": 0, "g": null, "x": 43.122, "y": 91.61}, {"n": 11, "s": 0, "u": 0, "g": null, "x": 46.772, "y": 91.61}, {"n": 10, "s": 1, "u": 1, "g": null, "x": 52.381, "y": 91.61}, {"n": 10, "s": 1, "u": 1, "g": null, "x": 57.063, "y": 91.61}, {"n": 3, "s": 1, "u": 1, "g": null, "x": 63.81, "y": 91.61}, {"n": 3, "s": 1, "u": 1, "g": null, "x": 69.577, "y": 91.61}, {"n": 2, "s": 1, "u": 1, "g": null, "x": 74.868, "y": 91.61}, {"n": 2, "s": 0, "u": 0, "g": null, "x": 37.91, "y": 95.206}, {"n": 26, "s": 0, "u": 0, "g": null, "x": 43.122, "y": 95.206}, {"n": 5, "s": 0, "u": 0, "g": null, "x": 46.772, "y": 95.206}];
const CIPHER_NAMES = ['conscious', 'subconscious'];
const LOCKED = { '0': { D: 9, E: 15, N: 2 }, '1': {} };
// assign[cipher][letter] = number
let assign = { '0': Object.assign({}, LOCKED['0']), '1': {} };
let manual = {};   // cell index -> { L, st } : letter typed straight into one square
let stamps = { '0': {}, '1': {} };  // per cipher+number counter, bumped whenever the key entry for that number changes
try { const saved = JSON.parse(localStorage.getItem('codebreak2025') || 'null');
  if (saved && saved.a) { assign['0'] = Object.assign({}, LOCKED['0'], saved.a['0'] || {}); assign['1'] = saved.a['1'] || {}; manual = saved.m || {}; stamps = saved.st || { '0': {}, '1': {} }; } } catch (e) {}
function stampOf(cp, num) { return stamps[String(cp)][num] || 0; }
function bump(cp, num) { const k = String(cp); stamps[k][num] = (stamps[k][num] || 0) + 1; }
let selected = null; // index into CELLS
const art = document.getElementById('art');
const cellEls = [];
CELLS.forEach((c, i) => {
  const d = document.createElement('div');
  d.className = 'cell'; d.style.left = c.x + '%'; d.style.top = c.y + '%';
  d.dataset.i = i;
  if (c.u) { const dot = document.createElement('span'); dot.className = 'dot'; d.appendChild(dot); }
  const ch = document.createElement('span'); ch.className = 'ch'; d.appendChild(ch);
  d.addEventListener('click', () => { selectCell(i); document.getElementById('kbd').focus({ preventScroll: true }); });
  art.appendChild(d); cellEls.push(d);
});
// build key panel
const keyTable = document.getElementById('keyTable');
const keyInputs = { '0': {}, '1': {} };
'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('').forEach(L => {
  const tr = document.createElement('tr');
  const tdL = document.createElement('td'); tdL.className = 'letter'; tdL.textContent = L; tr.appendChild(tdL);
  [0, 1].forEach(cp => {
    const td = document.createElement('td'); if (cp === 1) td.className = 'c2';
    const inp = document.createElement('input');
    inp.setAttribute('inputmode', 'numeric'); inp.setAttribute('aria-label', 'Number for ' + L + ' in C' + (cp + 1));
    if (LOCKED[String(cp)][L]) { inp.classList.add('locked'); inp.disabled = true; }
    inp.addEventListener('change', () => commitKey(cp, L, inp.value));
    inp.addEventListener('keydown', ev => { if (ev.key === 'Enter') inp.blur(); });
    td.appendChild(inp); tr.appendChild(td); keyInputs[String(cp)][L] = inp;
  });
  keyTable.appendChild(tr);
});
function letterFor(cp, num) { for (const L in assign[String(cp)]) if (assign[String(cp)][L] === num) return L; return null; }
function save() { try { localStorage.setItem('codebreak2025', JSON.stringify({ a: assign, m: manual, st: stamps })); } catch (e) {} }
let warnTimer = null;
function warn(msg, kind) {
  const w = document.getElementById('warn'); w.textContent = msg; w.className = kind || 'warn';
  clearTimeout(warnTimer); warnTimer = setTimeout(() => { w.className = ''; w.style.display = 'none'; }, 5000);
  w.style.display = 'block';
}
function setAssign(cp, letter, num) {
  // returns true if applied
  const key = String(cp);
  const holder = letterFor(cp, num);
  if (holder && holder !== letter) {
    warn(num + ' is already filled in for ' + holder + ' in the ' + CIPHER_NAMES[cp] + ' key (C' + (cp + 1) + ').');
    return false;
  }
  if (LOCKED[key][letter] && LOCKED[key][letter] !== num) {
    warn(letter + ' is given as ' + LOCKED[key][letter] + ' in the ' + CIPHER_NAMES[cp] + ' key, so it can’t be changed.');
    return false;
  }
  const prev = assign[key][letter];
  assign[key][letter] = num; bump(cp, num); if (prev && prev !== num) bump(cp, prev);
  save(); render();
  const count = CELLS.filter(c => c.s === cp && c.n === num).length;
  if (count === 0) warn('There are no ' + num + ' squares in the ' + CIPHER_NAMES[cp] + ' half.', 'info');
  return true;
}
function clearAssign(cp, letter) {
  const key = String(cp);
  if (LOCKED[key][letter]) return;
  const prev = assign[key][letter];
  delete assign[key][letter]; if (prev) bump(cp, prev);
  save(); render();
}
function commitKey(cp, letter, raw) {
  const inp = keyInputs[String(cp)][letter];
  const v = String(raw).trim();
  if (v === '') { clearAssign(cp, letter); inp.value = ''; return; }
  if (!/^\d{1,2}$/.test(v) || +v < 1 || +v > 26) {
    warn('“' + v + '” isn’t a number from 1 to 26.');
    inp.value = assign[String(cp)][letter] || ''; flashErr(inp); return;
  }
  if (!setAssign(cp, letter, +v)) { inp.value = assign[String(cp)][letter] || ''; flashErr(inp); }
}
function flashErr(inp) { inp.classList.add('err'); setTimeout(() => inp.classList.remove('err'), 1200); }
function selectCell(i) {
  selected = i;
  cellEls.forEach((el, j) => {
    const c = CELLS[j];
    el.classList.toggle('sel', j === i);
    el.classList.toggle('hl', c.s === CELLS[i].s && c.n === CELLS[i].n && j !== i);
  });
}
function displayLetter(i) {
  const c = CELLS[i];
  if (c.g) return '';
  const kl = letterFor(c.s, c.n);
  const m = manual[i];
  if (kl && (!m || m.st < stampOf(c.s, c.n))) return kl;
  if (m) return m.L;
  return kl || '';
}
function render() {
  CELLS.forEach((c, i) => {
    cellEls[i].querySelector('.ch').textContent = displayLetter(i);
  });
  for (const cp of ['0', '1']) for (const L in keyInputs[cp]) keyInputs[cp][L].value = assign[cp][L] || '';
  const parts = [0, 1].map(cp => {
    const nums = new Set(CELLS.filter(c => c.s === cp).map(c => c.n));
    const done = [...nums].filter(n => letterFor(cp, n)).length;
    return CIPHER_NAMES[cp] + ': ' + done + ' of ' + nums.size + ' numbers filled in';
  });
  document.getElementById('status').textContent = parts.join(' · ');
  if (selected !== null) selectCell(selected);
}
document.addEventListener('keydown', ev => {
  if (selected === null) return;
  if (ev.target && ev.target.tagName === 'INPUT') return;
  const c = CELLS[selected];
  if (/^[a-zA-Z]$/.test(ev.key)) {
    if (c.g) return;
    manual[selected] = { L: ev.key.toUpperCase(), st: stampOf(c.s, c.n) };
    save(); render(); ev.preventDefault();
  } else if (ev.key === 'Backspace' || ev.key === 'Delete') {
    if (manual[selected]) { delete manual[selected]; save(); render(); }
    ev.preventDefault();
  }
});
// timer — manual start/stop, no solve checker
let t0 = null, elapsed = 0, tick = null;
const clock = document.getElementById('clock');
function fmt(ms) { const s = Math.floor(ms / 1000); const m = Math.floor(s / 60); const h = Math.floor(m / 60);
  const ss = String(s % 60).padStart(2, '0'); const mm = String(m % 60).padStart(2, '0');
  return h > 0 ? h + ':' + mm + ':' + ss : m + ':' + ss; }
function showClock() { clock.textContent = fmt(elapsed + (t0 ? Date.now() - t0 : 0)); }
document.getElementById('btnTimer').addEventListener('click', ev => {
  if (t0) { elapsed += Date.now() - t0; t0 = null; clearInterval(tick); ev.target.textContent = 'Start'; }
  else { t0 = Date.now(); tick = setInterval(showClock, 250); ev.target.textContent = 'Pause'; }
  showClock();
});
document.getElementById('btnResetClock').addEventListener('click', () => {
  t0 = null; elapsed = 0; clearInterval(tick); document.getElementById('btnTimer').textContent = 'Start'; showClock();
});
document.getElementById('btnClear').addEventListener('click', () => {
  assign = { '0': Object.assign({}, LOCKED['0']), '1': {} }; manual = {}; save(); render();
});
function fitText() { const w = art.clientWidth; if (w) art.style.setProperty('--chfs', Math.max(7, w * 0.0155).toFixed(1) + 'px'); }
window.addEventListener('resize', fitText);
const artImg = art.querySelector('img'); if (artImg) artImg.addEventListener('load', fitText);
render(); showClock(); fitText();
</script>
