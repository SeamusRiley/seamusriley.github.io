---
permalink: /puzzles/2025/
title: "Christmas Codebreak 2025 — Psychology"
---

<style>
  .cb-game { color:#1c1a17; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; }
  .cb-game .tools { display:flex; flex-wrap:wrap; gap:10px; align-items:center; margin:10px 0; }
  .cb-game button { font:inherit; background:#fffdf6; border:2px solid #1c1a17; border-radius:4px; padding:5px 12px; cursor:pointer; }
  .cb-game button:hover { background:#efe7d3; }
  .cb-game #warn { display:none; margin:10px 0; padding:9px 13px; border-radius:4px; font-weight:bold; }
  .cb-game #warn.warn { display:block; background:#fbe3e0; border:2px solid #b3372a; color:#7c1d12; }
  .cb-game #warn.info { display:block; background:#fdf3d8; border:2px solid #a97b12; color:#6b4d08; }
  .cb-game .pane { overflow:auto; max-height:82vh; border:2.5px solid #1c1a17; background:#fff; }
  .cb-game .art { position:relative; line-height:0; }
  .cb-game .art img { width:100%; height:auto; display:block; }
  .cb-game .fld { position:absolute; transform:translate(-50%,-50%); background:transparent; border:0; padding:0; margin:0; text-align:center; color:#20306e; font-family:inherit; text-transform:uppercase; caret-color:#b3372a; }
  .cb-game .fld:focus { outline:none; box-shadow:inset 0 0 0 2px #b3372a; background:rgba(255,205,55,.22); }
  .cb-game .cell { font-size:var(--chfs, 14px); }
  .cb-game .cell.hl { background:rgba(255,205,55,.38); }
  .cb-game .keyfld { width:1.60%; height:2.45%; font-size:var(--kfs, 12px); }
  .cb-game .keyfld.err { background:#f8d7d2; }
</style>

<div class="cb-game">
<div class="tools">
  <button id="btnZoomOut" type="button">Zoom &minus;</button>
  <span id="zoomLabel">100%</span>
  <button id="btnZoomIn" type="button">Zoom +</button>
  <button id="btnClear" type="button">Clear letters</button>
</div>
<div id="warn" role="alert"></div>
<div class="pane" id="pane">
  <div class="art" id="art">
    <img src="/assets/images/puzzle-2025-full.png" alt="The hand-drawn 2025 Christmas codebreak, complete artwork">
  </div>
</div>
</div>

<script>
const CELLS = [{"n": 8, "s": 0, "u": 0, "g": null, "b": 1, "c": 5}, {"n": 4, "s": 0, "u": 0, "g": null, "b": 2, "c": 5}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 2, "c": 6}, {"n": 22, "s": 0, "u": 0, "g": null, "b": 2, "c": 7}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 2, "c": 8}, {"n": 1, "s": 0, "u": 0, "g": null, "b": 2, "c": 13}, {"n": 18, "s": 1, "u": 0, "g": null, "b": 2, "c": 41}, {"n": 10, "s": 1, "u": 0, "g": null, "b": 2, "c": 42}, {"n": 23, "s": 1, "u": 0, "g": null, "b": 2, "c": 43}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 3, "c": 5}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 3, "c": 12}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 3, "c": 13}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 3, "c": 20}, {"n": 21, "s": 1, "u": 0, "g": null, "b": 3, "c": 29}, {"n": 3, "s": 1, "u": 0, "g": null, "b": 3, "c": 31}, {"n": 13, "s": 1, "u": 0, "g": null, "b": 3, "c": 34}, {"n": 16, "s": 1, "u": 0, "g": null, "b": 3, "c": 37}, {"n": 2, "s": 1, "u": 0, "g": null, "b": 3, "c": 39}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 4, "c": 5}, {"n": 1, "s": 0, "u": 0, "g": null, "b": 4, "c": 6}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 4, "c": 7}, {"n": 4, "s": 0, "u": 0, "g": null, "b": 4, "c": 8}, {"n": 22, "s": 0, "u": 0, "g": null, "b": 4, "c": 9}, {"n": 1, "s": 0, "u": 0, "g": null, "b": 4, "c": 11}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 4, "c": 12}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 4, "c": 13}, {"n": 16, "s": 0, "u": 0, "g": null, "b": 4, "c": 15}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 4, "c": 21}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 4, "c": 22}, {"n": 22, "s": 0, "u": 0, "g": null, "b": 4, "c": 23}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 4, "c": 24}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 4, "c": 25}, {"n": 17, "s": 1, "u": 0, "g": null, "b": 4, "c": 29}, {"n": 13, "s": 1, "u": 0, "g": null, "b": 4, "c": 30}, {"n": 3, "s": 1, "u": 0, "g": null, "b": 4, "c": 33}, {"n": 6, "s": 1, "u": 0, "g": null, "b": 4, "c": 40}, {"n": 3, "s": 1, "u": 0, "g": null, "b": 4, "c": 42}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 5, "c": 5}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 5, "c": 12}, {"n": 14, "s": 0, "u": 0, "g": null, "b": 5, "c": 14}, {"n": 3, "s": 0, "u": 0, "g": null, "b": 5, "c": 15}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 5, "c": 16}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 5, "c": 17}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 5, "c": 19}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 5, "c": 20}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 5, "c": 22}, {"n": 9, "s": 1, "u": 0, "g": null, "b": 5, "c": 29}, {"n": 8, "s": 1, "u": 0, "g": null, "b": 5, "c": 31}, {"n": 8, "s": 1, "u": 0, "g": null, "b": 5, "c": 33}, {"n": 7, "s": 1, "u": 0, "g": null, "b": 5, "c": 35}, {"n": 2, "s": 1, "u": 0, "g": null, "b": 5, "c": 37}, {"n": 16, "s": 1, "u": 0, "g": null, "b": 5, "c": 40}, {"n": 16, "s": 0, "u": 0, "g": null, "b": 6, "c": 7}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 6, "c": 14}, {"n": 10, "s": 0, "u": 0, "g": null, "b": 6, "c": 16}, {"n": 6, "s": 0, "u": 0, "g": null, "b": 6, "c": 21}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 6, "c": 24}, {"n": 18, "s": 1, "u": 0, "g": null, "b": 6, "c": 26}, {"n": 8, "s": 1, "u": 1, "g": null, "b": 6, "c": 27}, {"n": 16, "s": 1, "u": 0, "g": null, "b": 6, "c": 28}, {"n": 22, "s": 1, "u": 0, "g": null, "b": 6, "c": 34}, {"n": 10, "s": 1, "u": 1, "g": null, "b": 6, "c": 41}, {"n": 23, "s": 1, "u": 0, "g": null, "b": 6, "c": 43}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 7, "c": 5}, {"n": 6, "s": 0, "u": 0, "g": null, "b": 7, "c": 6}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 7, "c": 7}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 7, "c": 9}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 7, "c": 10}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 7, "c": 11}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 7, "c": 12}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 7, "c": 14}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 7, "c": 16}, {"n": 1, "s": 0, "u": 0, "g": null, "b": 7, "c": 18}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 7, "c": 19}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 7, "c": 20}, {"n": 10, "s": 0, "u": 0, "g": null, "b": 7, "c": 21}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 7, "c": 22}, {"n": 1, "s": 0, "u": 0, "g": null, "b": 7, "c": 24}, {"n": 3, "s": 1, "u": 0, "g": null, "b": 7, "c": 26}, {"n": 1, "s": 1, "u": 0, "g": null, "b": 7, "c": 29}, {"n": 21, "s": 1, "u": 0, "g": null, "b": 7, "c": 31}, {"n": 3, "s": 1, "u": 1, "g": null, "b": 7, "c": 39}, {"n": 10, "s": 1, "u": 0, "g": null, "b": 7, "c": 42}, {"n": 4, "s": 0, "u": 0, "g": null, "b": 8, "c": 7}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 8, "c": 16}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 8, "c": 24}, {"n": 8, "s": 1, "u": 0, "g": null, "b": 8, "c": 28}, {"n": 10, "s": 1, "u": 0, "g": null, "b": 8, "c": 30}, {"n": 4, "s": 1, "u": 1, "g": null, "b": 8, "c": 31}, {"n": 2, "s": 1, "u": 0, "g": null, "b": 8, "c": 32}, {"n": 1, "s": 1, "u": 1, "g": null, "b": 8, "c": 35}, {"n": 6, "s": 1, "u": 1, "g": null, "b": 8, "c": 37}, {"n": 0, "s": 1, "u": 1, "g": null, "b": 8, "c": 39}, {"n": 7, "s": 1, "u": 0, "g": null, "b": 8, "c": 42}, {"n": 5, "s": 0, "u": 0, "g": null, "b": 9, "c": 5}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 9, "c": 6}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 9, "c": 7}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 9, "c": 8}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 9, "c": 9}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 9, "c": 10}, {"n": 10, "s": 0, "u": 0, "g": null, "b": 9, "c": 11}, {"n": 3, "s": 0, "u": 0, "g": null, "b": 9, "c": 13}, {"n": 24, "s": 0, "u": 0, "g": null, "b": 9, "c": 15}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 9, "c": 16}, {"n": 4, "s": 0, "u": 0, "g": null, "b": 9, "c": 17}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 9, "c": 18}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 9, "c": 19}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 9, "c": 20}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 9, "c": 21}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 9, "c": 22}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 9, "c": 23}, {"n": 9, "s": 1, "u": 0, "g": null, "b": 9, "c": 26}, {"n": 6, "s": 1, "u": 1, "g": null, "b": 9, "c": 28}, {"n": 9, "s": 1, "u": 0, "g": null, "b": 9, "c": 30}, {"n": 8, "s": 1, "u": 1, "g": null, "b": 9, "c": 32}, {"n": 2, "s": 1, "u": 1, "g": null, "b": 9, "c": 34}, {"n": 1, "s": 1, "u": 0, "g": null, "b": 9, "c": 36}, {"n": 1, "s": 1, "u": 0, "g": null, "b": 9, "c": 38}, {"n": 24, "s": 1, "u": 0, "g": null, "b": 9, "c": 41}, {"n": 8, "s": 1, "u": 0, "g": null, "b": 9, "c": 42}, {"n": 11, "s": 1, "u": 0, "g": null, "b": 9, "c": 43}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 10, "c": 5}, {"n": 9, "s": 0, "u": 0, "g": null, "b": 10, "c": 7}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 10, "c": 9}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 10, "c": 13}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 10, "c": 23}, {"n": 9, "s": 1, "u": 0, "g": null, "b": 10, "c": 26}, {"n": 23, "s": 1, "u": 1, "g": null, "b": 10, "c": 31}, {"n": 8, "s": 1, "u": 1, "g": null, "b": 10, "c": 37}, {"n": 5, "s": 1, "u": 1, "g": null, "b": 10, "c": 40}, {"n": 18, "s": 1, "u": 1, "g": null, "b": 10, "c": 42}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 11, "c": 5}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 11, "c": 7}, {"n": 10, "s": 0, "u": 0, "g": null, "b": 11, "c": 9}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 11, "c": 11}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 11, "c": 13}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 11, "c": 14}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 11, "c": 15}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 11, "c": 17}, {"n": 10, "s": 0, "u": 0, "g": null, "b": 11, "c": 18}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 11, "c": 19}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 11, "c": 20}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 11, "c": 21}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 11, "c": 22}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 11, "c": 23}, {"n": 19, "s": 0, "u": 0, "g": null, "b": 12, "c": 5}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 12, "c": 7}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 12, "c": 10}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 12, "c": 12}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 12, "c": 14}, {"n": 1, "s": 0, "u": 0, "g": null, "b": 12, "c": 16}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 12, "c": 19}, {"n": 2, "s": 1, "u": 0, "g": null, "b": 12, "c": 26}, {"n": 10, "s": 1, "u": 0, "g": null, "b": 12, "c": 29}, {"n": 7, "s": 1, "u": 1, "g": null, "b": 12, "c": 31}, {"n": 5, "s": 1, "u": 1, "g": null, "b": 12, "c": 33}, {"n": 1, "s": 1, "u": 0, "g": null, "b": 12, "c": 37}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 13, "c": 5}, {"n": 12, "s": 0, "u": 0, "g": null, "b": 13, "c": 7}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 13, "c": 10}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 13, "c": 11}, {"n": 14, "s": 0, "u": 0, "g": null, "b": 13, "c": 12}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 13, "c": 14}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 13, "c": 16}, {"n": 6, "s": 0, "u": 0, "g": null, "b": 13, "c": 19}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 13, "c": 20}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 13, "c": 21}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 13, "c": 22}, {"n": 19, "s": 0, "u": 0, "g": null, "b": 13, "c": 23}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 13, "c": 24}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 13, "c": 25}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 13, "c": 26}, {"n": 5, "s": 1, "u": 0, "g": null, "b": 13, "c": 32}, {"n": 7, "s": 1, "u": 0, "g": null, "b": 13, "c": 38}, {"n": 6, "s": 1, "u": 1, "g": null, "b": 13, "c": 39}, {"n": 4, "s": 1, "u": 0, "g": null, "b": 13, "c": 41}, {"n": 1, "s": 0, "u": 0, "g": null, "b": 14, "c": 5}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 14, "c": 6}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 14, "c": 7}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 14, "c": 8}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 14, "c": 9}, {"n": 10, "s": 0, "u": 0, "g": null, "b": 14, "c": 10}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 14, "c": 12}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 14, "c": 14}, {"n": 6, "s": 0, "u": 0, "g": null, "b": 14, "c": 16}, {"n": 23, "s": 0, "u": 1, "g": null, "b": 14, "c": 19}, {"n": 4, "s": 1, "u": 1, "g": null, "b": 14, "c": 29}, {"n": 6, "s": 1, "u": 1, "g": null, "b": 14, "c": 31}, {"n": 2, "s": 1, "u": 1, "g": null, "b": 14, "c": 33}, {"n": 1, "s": 1, "u": 0, "g": null, "b": 14, "c": 37}, {"n": 10, "s": 0, "u": 0, "g": null, "b": 15, "c": 10}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 15, "c": 11}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 15, "c": 13}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 15, "c": 15}, {"n": 14, "s": 0, "u": 0, "g": null, "b": 15, "c": 16}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 15, "c": 17}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 15, "c": 18}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 15, "c": 19}, {"n": 19, "s": 0, "u": 0, "g": null, "b": 15, "c": 20}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 15, "c": 21}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 15, "c": 22}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 15, "c": 23}, {"n": 18, "s": 1, "u": 0, "g": null, "b": 15, "c": 26}, {"n": 6, "s": 1, "u": 0, "g": null, "b": 15, "c": 27}, {"n": 4, "s": 1, "u": 1, "g": null, "b": 15, "c": 40}, {"n": 23, "s": 1, "u": 1, "g": null, "b": 15, "c": 41}, {"n": 25, "s": 0, "u": 1, "g": null, "b": 16, "c": 11}, {"n": 10, "s": 0, "u": 1, "g": null, "b": 16, "c": 13}, {"n": 3, "s": 1, "u": 1, "g": null, "b": 16, "c": 28}, {"n": 7, "s": 1, "u": 1, "g": null, "b": 16, "c": 30}, {"n": 2, "s": 1, "u": 1, "g": null, "b": 16, "c": 33}, {"n": 1, "s": 1, "u": 0, "g": null, "b": 16, "c": 35}, {"n": 6, "s": 1, "u": 1, "g": null, "b": 16, "c": 37}, {"n": 10, "s": 1, "u": 0, "g": null, "b": 16, "c": 39}, {"n": 3, "s": 1, "u": 1, "g": null, "b": 16, "c": 41}, {"n": 1, "s": 0, "u": 0, "g": null, "b": 17, "c": 5}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 17, "c": 6}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 17, "c": 7}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 17, "c": 8}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 17, "c": 9}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 17, "c": 10}, {"n": 12, "s": 0, "u": 0, "g": null, "b": 17, "c": 12}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 17, "c": 13}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 17, "c": 14}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 17, "c": 15}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 17, "c": 16}, {"n": 6, "s": 0, "u": 0, "g": null, "b": 17, "c": 17}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 17, "c": 19}, {"n": 5, "s": 0, "u": 0, "g": null, "b": 17, "c": 20}, {"n": 12, "s": 0, "u": 0, "g": null, "b": 17, "c": 21}, {"n": 16, "s": 0, "u": 0, "g": null, "b": 17, "c": 25}, {"n": 3, "s": 1, "u": 0, "g": null, "b": 17, "c": 26}, {"n": 1, "s": 1, "u": 0, "g": null, "b": 17, "c": 27}, {"n": 1, "s": 1, "u": 0, "g": null, "b": 17, "c": 29}, {"n": 1, "s": 1, "u": 0, "g": null, "b": 17, "c": 40}, {"n": 10, "s": 1, "u": 0, "g": null, "b": 17, "c": 41}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 18, "c": 16}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 18, "c": 23}, {"n": 10, "s": 0, "u": 0, "g": null, "b": 18, "c": 25}, {"n": 25, "s": 1, "u": 0, "g": null, "b": 18, "c": 30}, {"n": 7, "s": 1, "u": 1, "g": null, "b": 18, "c": 33}, {"n": 10, "s": 1, "u": 0, "g": null, "b": 18, "c": 35}, {"n": 1, "s": 1, "u": 0, "g": null, "b": 18, "c": 38}, {"n": 25, "s": 1, "u": 0, "g": null, "b": 18, "c": 41}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 19, "c": 5}, {"n": 4, "s": 0, "u": 0, "g": null, "b": 19, "c": 6}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 19, "c": 7}, {"n": 1, "s": 0, "u": 0, "g": null, "b": 19, "c": 8}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 19, "c": 9}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 19, "c": 10}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 19, "c": 11}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 19, "c": 12}, {"n": 12, "s": 0, "u": 0, "g": null, "b": 19, "c": 13}, {"n": 3, "s": 0, "u": 0, "g": null, "b": 19, "c": 17}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 19, "c": 18}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 19, "c": 19}, {"n": 9, "s": 0, "u": 0, "g": null, "b": 19, "c": 20}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 19, "c": 21}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 19, "c": 23}, {"n": 9, "s": 0, "u": 0, "g": null, "b": 19, "c": 24}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 19, "c": 25}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 19, "c": 26}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 19, "c": 27}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 19, "c": 28}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 19, "c": 29}, {"n": 12, "s": 0, "u": 0, "g": null, "b": 19, "c": 30}, {"n": 3, "s": 1, "u": 0, "g": null, "b": 19, "c": 37}, {"n": 25, "s": 1, "u": 0, "g": null, "b": 19, "c": 39}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 20, "c": 5}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 20, "c": 13}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 20, "c": 23}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 20, "c": 25}, {"n": 8, "s": 1, "u": 1, "g": null, "b": 20, "c": 32}, {"n": 7, "s": 1, "u": 1, "g": null, "b": 20, "c": 34}, {"n": 13, "s": 1, "u": 0, "g": null, "b": 20, "c": 37}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 21, "c": 5}, {"n": 8, "s": 0, "u": 0, "g": null, "b": 21, "c": 7}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 21, "c": 8}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 21, "c": 9}, {"n": 10, "s": 0, "u": 0, "g": null, "b": 21, "c": 10}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 21, "c": 11}, {"n": 14, "s": 0, "u": 0, "g": null, "b": 21, "c": 12}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 21, "c": 14}, {"n": 12, "s": 0, "u": 0, "g": null, "b": 21, "c": 15}, {"n": 5, "s": 0, "u": 0, "g": null, "b": 21, "c": 17}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 21, "c": 18}, {"n": 6, "s": 0, "u": 0, "g": null, "b": 21, "c": 19}, {"n": 3, "s": 0, "u": 0, "g": null, "b": 21, "c": 20}, {"n": 4, "s": 0, "u": 0, "g": null, "b": 21, "c": 21}, {"n": 10, "s": 0, "u": 0, "g": null, "b": 21, "c": 22}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 21, "c": 23}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 21, "c": 24}, {"n": 6, "s": 1, "u": 1, "g": null, "b": 21, "c": 26}, {"n": 20, "s": 1, "u": 0, "g": null, "b": 21, "c": 28}, {"n": 10, "s": 1, "u": 0, "g": null, "b": 21, "c": 29}, {"n": 8, "s": 1, "u": 0, "g": null, "b": 21, "c": 31}, {"n": 4, "s": 1, "u": 0, "g": null, "b": 21, "c": 38}, {"n": 11, "s": 1, "u": 1, "g": null, "b": 21, "c": 40}, {"n": 3, "s": 1, "u": 0, "g": null, "b": 21, "c": 42}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 22, "c": 5}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 22, "c": 8}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 22, "c": 12}, {"n": 5, "s": 0, "u": 0, "g": null, "b": 22, "c": 18}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 22, "c": 20}, {"n": 8, "s": 1, "u": 0, "g": null, "b": 22, "c": 34}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 23, "c": 5}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 23, "c": 7}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 23, "c": 8}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 23, "c": 9}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 23, "c": 10}, {"n": 21, "s": 0, "u": 0, "g": null, "b": 23, "c": 11}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 23, "c": 12}, {"n": 2, "s": 0, "u": 0, "g": "N", "b": 23, "c": 14}, {"n": 15, "s": 0, "u": 0, "g": "E", "b": 23, "c": 15}, {"n": 15, "s": 0, "u": 0, "g": "E", "b": 23, "c": 16}, {"n": 9, "s": 0, "u": 0, "g": "D", "b": 23, "c": 17}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 23, "c": 20}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 23, "c": 21}, {"n": 16, "s": 0, "u": 0, "g": null, "b": 23, "c": 23}, {"n": 5, "s": 1, "u": 0, "g": null, "b": 23, "c": 27}, {"n": 5, "s": 1, "u": 0, "g": null, "b": 23, "c": 29}, {"n": 4, "s": 1, "u": 1, "g": null, "b": 23, "c": 31}, {"n": 8, "s": 1, "u": 1, "g": null, "b": 23, "c": 37}, {"n": 10, "s": 1, "u": 0, "g": null, "b": 23, "c": 39}, {"n": 7, "s": 1, "u": 1, "g": null, "b": 23, "c": 41}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 24, "c": 5}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 24, "c": 8}, {"n": 9, "s": 0, "u": 1, "g": null, "b": 24, "c": 20}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 24, "c": 21}, {"n": 19, "s": 0, "u": 0, "g": null, "b": 24, "c": 22}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 24, "c": 23}, {"n": 10, "s": 0, "u": 0, "g": null, "b": 24, "c": 24}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 24, "c": 25}, {"n": 3, "s": 0, "u": 0, "g": null, "b": 24, "c": 26}, {"n": 3, "s": 1, "u": 0, "g": null, "b": 24, "c": 30}, {"n": 8, "s": 1, "u": 0, "g": null, "b": 24, "c": 32}, {"n": 2, "s": 1, "u": 0, "g": null, "b": 24, "c": 34}, {"n": 3, "s": 1, "u": 0, "g": null, "b": 24, "c": 37}, {"n": 7, "s": 1, "u": 0, "g": null, "b": 24, "c": 39}, {"n": 2, "s": 1, "u": 0, "g": null, "b": 24, "c": 41}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 25, "c": 5}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 25, "c": 6}, {"n": 19, "s": 0, "u": 0, "g": null, "b": 25, "c": 7}, {"n": 12, "s": 0, "u": 0, "g": null, "b": 25, "c": 8}, {"n": 22, "s": 0, "u": 0, "g": null, "b": 25, "c": 9}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 25, "c": 10}, {"n": 13, "s": 0, "u": 0, "g": null, "b": 25, "c": 11}, {"n": 25, "s": 0, "u": 0, "g": null, "b": 25, "c": 12}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 25, "c": 13}, {"n": 24, "s": 0, "u": 0, "g": null, "b": 25, "c": 14}, {"n": 12, "s": 0, "u": 0, "g": null, "b": 25, "c": 15}, {"n": 23, "s": 0, "u": 0, "g": null, "b": 25, "c": 16}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 25, "c": 17}, {"n": 22, "s": 0, "u": 0, "g": null, "b": 25, "c": 18}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 25, "c": 20}, {"n": 15, "s": 0, "u": 0, "g": null, "b": 25, "c": 22}, {"n": 11, "s": 0, "u": 0, "g": null, "b": 25, "c": 24}, {"n": 10, "s": 1, "u": 1, "g": null, "b": 25, "c": 26}, {"n": 10, "s": 1, "u": 1, "g": null, "b": 25, "c": 28}, {"n": 3, "s": 1, "u": 1, "g": null, "b": 25, "c": 30}, {"n": 3, "s": 1, "u": 1, "g": null, "b": 25, "c": 33}, {"n": 2, "s": 1, "u": 1, "g": null, "b": 25, "c": 35}, {"n": 2, "s": 0, "u": 0, "g": null, "b": 26, "c": 20}, {"n": 26, "s": 0, "u": 0, "g": null, "b": 26, "c": 22}, {"n": 5, "s": 0, "u": 0, "g": null, "b": 26, "c": 24}];
const VL = [476, 567, 662, 754, 855, 939, 1036, 1130, 1223, 1317, 1410, 1503, 1597, 1691, 1785, 1879, 1971, 2065, 2158, 2253, 2346, 2440, 2532, 2627, 2722, 2816, 2908, 3002, 3094, 3187, 3283, 3376, 3469, 3563, 3659, 3750, 3842, 3937, 4031, 4124, 4217, 4308, 4407, 4503, 4592];
const HLX = [521, 616, 710, 802, 889, 984, 1083, 1170, 1268, 1357, 1456, 1545, 1638, 1732, 1825, 1918, 2010, 2101, 2203, 2290, 2387, 2476, 2574, 2662, 2763, 2848, 2945, 3042];
const KEYPOS = {"c1x": 708, "c2x": 803, "rows": {"A": 22.909, "B": 25.712, "C": 28.515, "D": 31.364, "E": 34.227, "F": 37.03, "G": 39.864, "H": 42.727, "I": 45.606, "J": 48.348, "K": 51.076, "L": 53.939, "M": 56.833, "N": 59.621, "O": 62.379, "P": 65.273, "Q": 68.167, "R": 70.985, "S": 73.788, "T": 76.621, "U": 79.47, "V": 82.318, "W": 85.136, "X": 87.939, "Y": 90.727, "Z": 93.621}};
const CIPHER_NAMES = ['conscious', 'subconscious'];
const LOCKED = { '0': { D: 9, E: 15, N: 2 }, '1': {} };
let assign = { '0': Object.assign({}, LOCKED['0']), '1': {} };
let manual = {};
let stamps = { '0': {}, '1': {} };
try { const saved = JSON.parse(localStorage.getItem('codebreak2025') || 'null');
  if (saved && saved.a) { assign['0'] = Object.assign({}, LOCKED['0'], saved.a['0'] || {}); assign['1'] = saved.a['1'] || {}; manual = saved.m || {}; stamps = saved.st || { '0': {}, '1': {} }; } } catch (e) {}
function stampOf(cp, num) { return stamps[String(cp)][num] || 0; }
function bump(cp, num) { const k = String(cp); stamps[k][num] = (stamps[k][num] || 0) + 1; }
function letterFor(cp, num) { for (const L in assign[String(cp)]) if (assign[String(cp)][L] === num) return L; return null; }
function save() { try { localStorage.setItem('codebreak2025', JSON.stringify({ a: assign, m: manual, st: stamps })); } catch (e) {} }
let warnTimer = null;
function warn(msg, kind) {
  const w = document.getElementById('warn'); w.textContent = msg; w.className = kind || 'warn'; w.style.display = 'block';
  clearTimeout(warnTimer); warnTimer = setTimeout(() => { w.className = ''; w.style.display = 'none'; }, 5000);
}
function setAssign(cp, letter, num) {
  const key = String(cp);
  const holder = letterFor(cp, num);
  if (holder && holder !== letter) { warn(num + ' is already filled in for ' + holder + ' in the ' + CIPHER_NAMES[cp] + ' key (C' + (cp + 1) + ').'); return false; }
  if (LOCKED[key][letter] && LOCKED[key][letter] !== num) { warn(letter + ' is given as ' + LOCKED[key][letter] + ' in the ' + CIPHER_NAMES[cp] + ' key, so it can’t be changed.'); return false; }
  const prev = assign[key][letter];
  assign[key][letter] = num; bump(cp, num); if (prev && prev !== num) bump(cp, prev);
  save(); render();
  if (CELLS.filter(c => c.s === cp && c.n === num).length === 0) warn('There are no ' + num + ' squares in the ' + CIPHER_NAMES[cp] + ' half.', 'info');
  return true;
}
function clearAssign(cp, letter) {
  const key = String(cp);
  if (LOCKED[key][letter]) return;
  const prev = assign[key][letter];
  delete assign[key][letter]; if (prev) bump(cp, prev);
  save(); render();
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
const art = document.getElementById('art');
const cellEls = [];
CELLS.forEach((c, i) => {
  const inp = document.createElement('input');
  inp.className = 'fld cell';
  inp.style.left = ((VL[c.c] + VL[c.c + 1]) / 2 / 5100 * 100) + '%';
  inp.style.top = ((HLX[c.b] + HLX[c.b + 1]) / 2 / 3300 * 100) + '%';
  inp.style.width = ((VL[c.c + 1] - VL[c.c]) / 5100 * 100) + '%';
  inp.style.height = ((HLX[c.b + 1] - HLX[c.b]) / 3300 * 100) + '%';
  inp.setAttribute('autocomplete', 'off'); inp.setAttribute('autocapitalize', 'characters'); inp.setAttribute('aria-label', 'Square, number ' + c.n);
  if (c.g) { inp.disabled = true; }
  inp.addEventListener('input', () => {
    const letters = inp.value.toUpperCase().replace(/[^A-Z]/g, '');
    if (letters) { manual[i] = { L: letters[letters.length - 1], st: stampOf(c.s, c.n) }; save(); }
    render();
  });
  inp.addEventListener('keydown', ev => {
    if ((ev.key === 'Backspace' || ev.key === 'Delete') && manual[i]) { delete manual[i]; save(); setTimeout(render, 0); }
  });
  inp.addEventListener('focus', () => highlight(c.s, c.n));
  inp.addEventListener('blur', () => highlight(null));
  art.appendChild(inp); cellEls.push(inp);
});
const keyInputs = { '0': {}, '1': {} };
'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('').forEach(L => {
  [0, 1].forEach(cp => {
    const inp = document.createElement('input');
    inp.className = 'fld keyfld';
    inp.style.left = ((cp === 0 ? KEYPOS.c1x : KEYPOS.c2x) / 5100 * 100) + '%';
    inp.style.top = KEYPOS.rows[L] + '%';
    inp.setAttribute('inputmode', 'numeric'); inp.setAttribute('autocomplete', 'off');
    inp.setAttribute('aria-label', 'Key number for ' + L + ' in C' + (cp + 1));
    if (LOCKED[String(cp)][L]) { inp.disabled = true; inp.style.color = 'transparent'; }
    inp.addEventListener('change', () => commitKey(cp, L, inp.value));
    inp.addEventListener('keydown', ev => { if (ev.key === 'Enter') inp.blur(); });
    inp.addEventListener('focus', () => { const n = assign[String(cp)][L]; if (n) highlight(cp, n); });
    inp.addEventListener('blur', () => highlight(null));
    art.appendChild(inp); keyInputs[String(cp)][L] = inp;
  });
});
function commitKey(cp, letter, raw) {
  const inp = keyInputs[String(cp)][letter];
  const v = String(raw).trim();
  if (v === '') { clearAssign(cp, letter); inp.value = ''; return; }
  if (!/^\d{1,2}$/.test(v) || +v < 1 || +v > 26) { warn('“' + v + '” isn’t a number from 1 to 26.'); inp.value = assign[String(cp)][letter] || ''; flashErr(inp); return; }
  if (!setAssign(cp, letter, +v)) { inp.value = assign[String(cp)][letter] || ''; flashErr(inp); }
}
function flashErr(inp) { inp.classList.add('err'); setTimeout(() => inp.classList.remove('err'), 1200); }
function highlight(s, n) {
  cellEls.forEach((el, j) => el.classList.toggle('hl', s !== null && CELLS[j].s === s && CELLS[j].n === n));
}
function render() {
  CELLS.forEach((c, i) => { const v = displayLetter(i); if (cellEls[i].value !== v) cellEls[i].value = v; });
  for (const cp of ['0', '1']) for (const L in keyInputs[cp]) { const v = assign[cp][L] || ''; if (document.activeElement !== keyInputs[cp][L]) keyInputs[cp][L].value = v; else keyInputs[cp][L].value = v; }
}
let zoom = 1;
function fitText() {
  const w = art.clientWidth; if (!w) return;
  art.style.setProperty('--chfs', Math.max(6, w * 0.0115).toFixed(1) + 'px');
  art.style.setProperty('--kfs', Math.max(6, w * 0.0100).toFixed(1) + 'px');
}
function setZoom(z) {
  zoom = Math.min(4, Math.max(1, z));
  art.style.width = (zoom * 100) + '%';
  document.getElementById('zoomLabel').textContent = Math.round(zoom * 100) + '%';
  fitText();
}
document.getElementById('btnZoomIn').addEventListener('click', () => setZoom(zoom + 0.5));
document.getElementById('btnZoomOut').addEventListener('click', () => setZoom(zoom - 0.5));
document.getElementById('btnClear').addEventListener('click', () => { assign = { '0': Object.assign({}, LOCKED['0']), '1': {} }; manual = {}; save(); render(); });
window.addEventListener('resize', fitText);
const artImg = art.querySelector('img'); if (artImg) artImg.addEventListener('load', fitText);
render(); fitText();
</script>
