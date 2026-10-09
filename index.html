<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Lightsaber Forge</title>
<style>
  *{box-sizing:border-box}
  html,body{height:100%;margin:0}
  body{
    background:#05070c;color:#dbe3f0;overflow:hidden;
    font-family:ui-sans-serif,system-ui,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;
    -webkit-font-smoothing:antialiased;
  }
  .app{display:flex;height:100vh;height:100dvh}

  .panel{
    width:350px;flex:0 0 350px;overflow-y:auto;padding:16px 14px 60px;
    background:linear-gradient(180deg,#0b1018,#070a10);
    border-right:1px solid #16202e;
    scrollbar-width:thin;scrollbar-color:#22303f transparent;
  }
  .panel::-webkit-scrollbar{width:8px}
  .panel::-webkit-scrollbar-thumb{background:#22303f;border-radius:8px}
  h1{
    font-size:17px;letter-spacing:.22em;text-transform:uppercase;
    margin:2px 0 18px;font-weight:700;
    background:linear-gradient(90deg,#69b6ff,#c9a227,#ff5a5a);
    -webkit-background-clip:text;background-clip:text;color:transparent;
  }
  h2{
    font-size:10.5px;letter-spacing:.2em;text-transform:uppercase;
    color:#6d8199;margin:0 0 10px;font-weight:700;
  }
  .group{margin-bottom:22px}
  .row{
    display:flex;align-items:center;justify-content:space-between;gap:10px;
    margin-bottom:9px;font-size:12.5px;color:#9fb2c7;
  }
  .row > span{flex:0 0 auto}
  .row input[type=color]{
    width:52px;height:26px;padding:0;border:1px solid #23303f;border-radius:6px;
    background:#0c121b;cursor:pointer;
  }
  .row input[type=range]{
    flex:1;min-width:0;accent-color:#4aa8ff;height:20px;cursor:pointer;
  }
  .row select{
    flex:1;min-width:0;background:#0d141d;color:#cfe0f2;border:1px solid #23303f;
    border-radius:6px;padding:5px 6px;font-size:12px;cursor:pointer;outline:none;
  }
  .row.check{justify-content:flex-start;gap:8px}
  .row.check input{accent-color:#4aa8ff;width:15px;height:15px;cursor:pointer}

  .search{
    width:100%;background:#0d141d;border:1px solid #23303f;border-radius:7px;
    color:#cfe0f2;padding:7px 10px;font-size:12px;margin-bottom:10px;outline:none;
  }
  .search:focus{border-color:#2f6fa8}
  .chars{display:flex;flex-wrap:wrap;gap:6px;max-height:290px;overflow-y:auto;padding-right:4px}
  .chars::-webkit-scrollbar{width:7px}
  .chars::-webkit-scrollbar-thumb{background:#22303f;border-radius:8px}
  .char{
    display:flex;align-items:center;gap:6px;
    background:#0d141d;border:1px solid #1e2a38;color:#b9cade;
    padding:5px 9px;border-radius:20px;font-size:11px;cursor:pointer;
    transition:.15s;white-space:nowrap;
  }
  .char:hover{background:#141f2c;border-color:#33506e;color:#fff}
  .char.active{background:#16324d;border-color:#4aa8ff;color:#fff;box-shadow:0 0 12px rgba(74,168,255,.35)}
  .dot{width:9px;height:9px;border-radius:50%;flex:0 0 auto;box-shadow:0 0 7px currentColor}

  .stage{flex:1;position:relative;min-width:0;min-height:0;background:#04060a}
  canvas{display:block;position:absolute;inset:0}
  .toolbar{
    position:absolute;left:50%;bottom:18px;transform:translateX(-50%);
    display:flex;gap:8px;flex-wrap:wrap;justify-content:center;
    background:rgba(8,12,18,.82);border:1px solid #1c2836;border-radius:14px;
    padding:8px;backdrop-filter:blur(10px);z-index:5;max-width:calc(100% - 24px);
  }
  .btn{
    background:#101a26;border:1px solid #22303f;color:#c3d5e8;
    padding:8px 13px;border-radius:9px;font-size:12px;cursor:pointer;
    transition:.15s;letter-spacing:.04em;white-space:nowrap;
  }
  .btn:hover{background:#17263a;border-color:#3a6a9c;color:#fff}
  .btn:active{transform:scale(.96)}
  .btn.primary{background:#12395c;border-color:#3f8fd6;color:#eaf5ff}
  .btn.primary:hover{background:#17496f}
  .btn.on{background:#3a1f22;border-color:#d94b4b;color:#ffdcdc;box-shadow:0 0 12px rgba(217,75,75,.35)}

  @media (max-width:820px){
    .app{flex-direction:column-reverse}
    .panel{width:100%;flex:0 0 48%;border-right:none;border-top:1px solid #16202e;padding-bottom:24px}
    .stage{flex:1 1 52%}
    .chars{max-height:150px}
    .toolbar{bottom:10px;padding:6px}
    .btn{padding:7px 10px;font-size:11px}
  }
</style>
</head>
<body>
<div class="app">

  <aside class="panel">
    <h1>Lightsaber Forge</h1>

    <div class="group">
      <h2>Characters</h2>
      <input class="search" id="search" placeholder="Search a character…" autocomplete="off">
      <div class="chars" id="chars"></div>
    </div>

    <div class="group">
      <h2>Blade</h2>
      <div class="row"><span>Colour</span><input type="color" id="blade" value="#3ff06a"></div>
      <div class="row">
        <span>Type</span>
        <select id="type">
          <option value="single">Single blade</option>
          <option value="double">Double blade (staff)</option>
          <option value="crossguard">Crossguard</option>
          <option value="darksaber">Darksaber</option>
        </select>
      </div>
      <div class="row"><span>Length</span><input type="range" id="bladeLen" min="140" max="470" value="340"></div>
      <div class="row"><span>Width</span><input type="range" id="bladeW" min="8" max="26" value="16"></div>
      <div class="row"><span>Glow</span><input type="range" id="glow" min="0.3" max="1.7" step="0.05" value="1"></div>
      <div class="row check"><input type="checkbox" id="unstable"><span>Unstable blade (crackling)</span></div>
    </div>

    <div class="group">
      <h2>Hilt — Optional Parts</h2>
      <div class="row"><span>Finish</span><input type="color" id="hilt" value="#8f979f"></div>
      <div class="row"><span>Accent</span><input type="color" id="accent" value="#1a1f26"></div>
      <div class="row">
        <span>Emitter</span>
        <select id="emitter">
          <option value="standard">Standard</option>
          <option value="vented">Vented</option>
          <option value="rounded">Rounded</option>
          <option value="claw">Clawed</option>
          <option value="angled">Angled</option>
        </select>
      </div>
      <div class="row">
        <span>Grip</span>
        <select id="grip">
          <option value="ribbed">Ribbed</option>
          <option value="smooth">Smooth</option>
          <option value="wrapped">Leather wrap</option>
          <option value="segmented">Segmented</option>
          <option value="panel">Control panel</option>
        </select>
      </div>
      <div class="row">
        <span>Pommel</span>
        <select id="pommel">
          <option value="flat">Flat</option>
          <option value="rounded">Rounded</option>
          <option value="ring">Ring</option>
          <option value="cone">Cone</option>
        </select>
      </div>
    </div>
  </aside>

  <main class="stage" id="stage">
    <canvas id="c"></canvas>
    <div class="toolbar">
      <button class="btn primary" id="ignite">⚡ Ignite</button>
      <button class="btn" id="random">🎲 Random</button>
      <button class="btn" id="hum">🔊 Hum: Off</button>
      <button class="btn" id="bg">🌌 Transparent BG</button>
      <button class="btn" id="save">💾 Save PNG</button>
    </div>
  </main>
</div>

<script>
/* =====================================================================
   LIGHTSABER FORGE
   ===================================================================== */

const BASE = {
  blade:'#3fa9ff', type:'single', bladeLen:340, bladeW:16,
  hilt:'#c9ced6', accent:'#1b2027',
  emitter:'standard', grip:'ribbed', pommel:'flat', unstable:false
};

const PRESETS = [
  {name:'Luke Skywalker (ANH)', blade:'#3fa9ff', hilt:'#c9ced6', accent:'#20262e', emitter:'standard', grip:'ribbed',  pommel:'flat'},
  {name:'Luke Skywalker (ROTJ)',blade:'#3ff06a', hilt:'#8f979f', accent:'#1a1f26', emitter:'standard', grip:'ribbed',  pommel:'rounded'},
  {name:'Anakin Skywalker',     blade:'#3fa9ff', hilt:'#c2c8d0', accent:'#2a3038', emitter:'standard', grip:'panel',   pommel:'flat'},
  {name:'Obi-Wan Kenobi',       blade:'#3fa9ff', hilt:'#a8aeb6', accent:'#20252c', emitter:'rounded',  grip:'smooth',  pommel:'rounded'},
  {name:'Darth Vader',          blade:'#ff2b2b', hilt:'#2a2d33', accent:'#0d0f13', emitter:'vented',   grip:'ribbed',  pommel:'flat'},
  {name:'Emperor Palpatine',    blade:'#ff2b2b', hilt:'#3a3128', accent:'#c9a227', emitter:'angled',   grip:'smooth',  pommel:'cone'},
  {name:'Count Dooku',          blade:'#ff2b2b', hilt:'#4a4640', accent:'#c9a227', emitter:'angled',   grip:'wrapped', pommel:'cone'},
  {name:'Yoda',                 blade:'#3ff06a', bladeLen:190, bladeW:12, hilt:'#8f979f', accent:'#1a1f26', emitter:'rounded', grip:'ribbed', pommel:'rounded'},
  {name:'Mace Windu',           blade:'#b06bff', hilt:'#c9ced6', accent:'#3a2b12', emitter:'standard', grip:'panel',   pommel:'flat'},
  {name:'Qui-Gon Jinn',         blade:'#3ff06a', hilt:'#b6bcc4', accent:'#232830', emitter:'standard', grip:'smooth',  pommel:'flat'},
  {name:'Darth Maul',           blade:'#ff2b2b', type:'double', hilt:'#33373d', accent:'#0e1013', emitter:'vented', grip:'ribbed', pommel:'flat'},
  {name:'Asajj Ventress',       blade:'#ff2b2b', type:'double', hilt:'#4a4640', accent:'#1a1a1a', emitter:'angled', grip:'smooth', pommel:'cone'},
  {name:'Ahsoka Tano',          blade:'#3ff06a', bladeLen:250, bladeW:13, hilt:'#b6bcc4', accent:'#2a3038', emitter:'rounded', grip:'smooth', pommel:'rounded'},
  {name:'Rey Skywalker',        blade:'#ffd23f', hilt:'#c9ced6', accent:'#2a3038', emitter:'standard', grip:'wrapped', pommel:'ring'},
  {name:'Kylo Ren',             blade:'#ff2b2b', type:'crossguard', unstable:true, hilt:'#2a2d33', accent:'#0d0f13', emitter:'vented', grip:'segmented', pommel:'flat'},
  {name:'Ben Solo',             blade:'#3fa9ff', hilt:'#c9ced6', accent:'#20262e', emitter:'standard', grip:'smooth',  pommel:'flat'},
  {name:'Darth Revan',          blade:'#b06bff', hilt:'#3a3f46', accent:'#c9a227', emitter:'vented',   grip:'segmented', pommel:'flat'},
  {name:'Bastila Shan',         blade:'#ffd23f', type:'double', hilt:'#c9a227', accent:'#2a2216', emitter:'standard', grip:'smooth', pommel:'flat'},
  {name:'Starkiller',           blade:'#ff2b2b', hilt:'#4a4f56', accent:'#0d0f13', emitter:'claw',     grip:'segmented', pommel:'flat'},
  {name:'Ezra Bridger',         blade:'#3ff06a', hilt:'#b6bcc4', accent:'#2a3038', emitter:'standard', grip:'panel',   pommel:'flat'},
  {name:'Kanan Jarrus',         blade:'#3fa9ff', hilt:'#a8aeb6', accent:'#20252c', emitter:'standard', grip:'panel',   pommel:'flat'},
  {name:'Cal Kestis',           blade:'#3fa9ff', hilt:'#c9ced6', accent:'#3a2b12', emitter:'standard', grip:'wrapped', pommel:'ring'},
  {name:'Cere Junda',           blade:'#3fa9ff', hilt:'#8f979f', accent:'#1a1f26', emitter:'rounded',  grip:'ribbed',  pommel:'flat'},
  {name:'The Grand Inquisitor', blade:'#ff2b2b', type:'double', hilt:'#33373d', accent:'#0d0f13', emitter:'vented', grip:'segmented', pommel:'flat'},
  {name:'Second Sister',        blade:'#ff2b2b', type:'double', hilt:'#2f333a', accent:'#0d0f13', emitter:'vented', grip:'ribbed', pommel:'flat'},
  {name:'Pre Vizsla',           blade:'#ffffff', type:'darksaber', bladeLen:310, bladeW:22, hilt:'#3a3f46', accent:'#0d0f13', emitter:'angled', grip:'segmented', pommel:'cone'},
  {name:'Moff Gideon',          blade:'#ffffff', type:'darksaber', bladeLen:310, bladeW:22, hilt:'#2a2d33', accent:'#c9a227', emitter:'angled', grip:'segmented', pommel:'cone'},
  {name:'Leia Organa',          blade:'#3fa9ff', hilt:'#c9ced6', accent:'#20262e', emitter:'standard', grip:'smooth',  pommel:'rounded'},
  {name:'Mara Jade',            blade:'#b06bff', hilt:'#8f979f', accent:'#1a1f26', emitter:'standard', grip:'ribbed',  pommel:'flat'},
  {name:'Plo Koon',             blade:'#3fa9ff', hilt:'#a8aeb6', accent:'#20252c', emitter:'standard', grip:'ribbed',  pommel:'flat'},
  {name:'Kit Fisto',            blade:'#3ff06a', hilt:'#8f979f', accent:'#1a1f26', emitter:'standard', grip:'smooth',  pommel:'flat'},
  {name:'Aayla Secura',         blade:'#3fa9ff', hilt:'#c9ced6', accent:'#20262e', emitter:'standard', grip:'smooth',  pommel:'flat'},
  {name:'Shaak Ti',             blade:'#3fa9ff', hilt:'#c9ced6', accent:'#3a2b12', emitter:'standard', grip:'ribbed',  pommel:'flat'},
  {name:'Luminara Unduli',      blade:'#3ff06a', hilt:'#8f979f', accent:'#1a1f26', emitter:'standard', grip:'ribbed',  pommel:'flat'},
  {name:'Savage Opress',        blade:'#ff2b2b', type:'double', hilt:'#3a3f46', accent:'#0d0f13', emitter:'vented', grip:'segmented', pommel:'flat'},
  {name:'Darth Bane',           blade:'#ff2b2b', hilt:'#4a4640', accent:'#c9a227', emitter:'angled',   grip:'wrapped', pommel:'cone'},
  {name:'Darth Nihilus',        blade:'#ff2b2b', hilt:'#2a2d33', accent:'#0d0f13', emitter:'vented',   grip:'smooth',  pommel:'flat'},
  {name:'Darth Plagueis',       blade:'#ff2b2b', hilt:'#3a3128', accent:'#c9a227', emitter:'standard', grip:'smooth',  pommel:'rounded'},
  {name:'Shin Hati',            blade:'#ff8a1f', hilt:'#c9ced6', accent:'#20262e', emitter:'standard', grip:'wrapped', pommel:'flat'},
  {name:'Baylan Skoll',         blade:'#ff8a1f', hilt:'#3a3f46', accent:'#c9a227', emitter:'standard', grip:'ribbed',  pommel:'flat'},
  {name:'Sabine Wren',          blade:'#3ff06a', hilt:'#b6bcc4', accent:'#2a3038', emitter:'standard', grip:'panel',   pommel:'flat'},
  {name:'Kyle Katarn',          blade:'#3fa9ff', hilt:'#8f979f', accent:'#1a1f26', emitter:'standard', grip:'ribbed',  pommel:'flat'},
  {name:'Corran Horn',          blade:'#cfe8ff', hilt:'#c9ced6', accent:'#20262e', emitter:'standard', grip:'smooth',  pommel:'flat'},
  {name:'Tenel Ka',             blade:'#4ff0ff', hilt:'#c9ced6', accent:'#20262e', emitter:'rounded',  grip:'smooth',  pommel:'rounded'},
  {name:'Exar Kun',             blade:'#3fa9ff', type:'double', hilt:'#3a3f46', accent:'#c9a227', emitter:'claw', grip:'segmented', pommel:'flat'},
  {name:'Satele Shan',          blade:'#3fa9ff', type:'double', hilt:'#c9ced6', accent:'#20262e', emitter:'standard', grip:'smooth', pommel:'flat'},
  {name:'General Grievous',     blade:'#3fa9ff', hilt:'#8f979f', accent:'#20262e', emitter:'standard', grip:'segmented', pommel:'flat'},
  {name:'Tera Sinube',          blade:'#8fd6ff', bladeLen:210, bladeW:13, hilt:'#c9ced6', accent:'#20262e', emitter:'rounded', grip:'wrapped', pommel:'rounded'},
  {name:'Depa Billaba',         blade:'#3ff06a', hilt:'#c9ced6', accent:'#3a2b12', emitter:'standard', grip:'ribbed',  pommel:'flat'}
];

const state = Object.assign({}, BASE, {
  preset: 'Luke Skywalker (ROTJ)',
  glow: 1,
  transparent: false
});

const stage  = document.getElementById('stage');
const canvas = document.getElementById('c');
const ctx    = canvas.getContext('2d');
let W = 0, H = 0, DPR = 1, stars = [];

function resize(){
  const r = stage.getBoundingClientRect();
  DPR = Math.min(window.devicePixelRatio || 1, 2);
  W = Math.max(1, r.width);
  H = Math.max(1, r.height);
  canvas.width  = Math.round(W * DPR);
  canvas.height = Math.round(H * DPR);
  canvas.style.width  = W + 'px';
  canvas.style.height = H + 'px';

  stars = [];
  const n = Math.round((W * H) / 12000);
  for (let i = 0; i < n; i++){
    stars.push({
      x: Math.random() * W,
      y: Math.random() * H,
      r: Math.random() * 1.3 + 0.2,
      a: Math.random() * 0.55 + 0.1,
      p: Math.random() * Math.PI * 2
    });
  }
}
new ResizeObserver(resize).observe(stage);
resize();

function hexToRgb(h){
  h = String(h).replace('#','');
  if (h.length === 3) h = h.split('').map(c => c + c).join('');
  const n = parseInt(h, 16);
  return { r:(n >> 16) & 255, g:(n >> 8) & 255, b:n & 255 };
}
function shade(hex, amt){
  const { r, g, b } = hexToRgb(hex);
  const f = v => amt >= 0
    ? Math.round(v + (255 - v) * amt)
    : Math.round(v * (1 + amt));
  return `rgb(${f(r)},${f(g)},${f(b)})`;
}
function rgba(hex, a){
  const { r, g, b } = hexToRgb(hex);
  return `rgba(${r},${g},${b},${a})`;
}
function rr(c, x, y, w, h, r){
  r = Math.min(r, Math.abs(w) / 2, Math.abs(h) / 2);
  c.beginPath();
  c.moveTo(x + r, y);
  c.arcTo(x + w, y,     x + w, y + h, r);
  c.arcTo(x + w, y + h, x,     y + h, r);
  c.arcTo(x,     y + h, x,     y,     r);
  c.arcTo(x,     y,     x + w, y,     r);
  c.closePath();
}
function metalGrad(x0, x1, color){
  const g = ctx.createLinearGradient(x0, 0, x1, 0);
  g.addColorStop(0.00, shade(color, -0.58));
  g.addColorStop(0.14, shade(color, -0.12));
  g.addColorStop(0.38, shade(color,  0.50));
  g.addColorStop(0.55, shade(color,  0.10));
  g.addColorStop(0.80, shade(color, -0.34));
  g.addColorStop(1.00, shade(color, -0.64));
  return g;
}
function cyl(c, cx, y, w, h, r, color){
  const x = cx - w / 2;
  rr(c, x, y, w, h, r);
  c.fillStyle = metalGrad(x, x + w, color);
  c.fill();
  c.strokeStyle = 'rgba(0,0,0,.55)';
  c.lineWidth = 1;
  c.stroke();
}
const clamp = (v, a, b) => Math.min(b, Math.max(a, v));

function bladePath(c, ax, ay, bx, by, jit, t, seed){
  c.beginPath();
  c.moveTo(ax, ay);
  const N = jit > 0 ? 12 : 1;
  for (let i = 1; i <= N; i++){
    const f = i / N;
    let off = 0;
    if (jit > 0){
      off = (Math.sin(t * 31 + i * 2.3 + seed) * 0.6 +
             Math.sin(t * 57 + i * 5.1 + seed * 3) * 0.4) * jit;
    }
    c.lineTo(ax + (bx - ax) * f + off, ay + (by - ay) * f);
  }
}

function drawBlade(c, ax, ay, bx, by, w, color, core, intensity, unstable, t, seed){
  if (intensity <= 0.004) return;
  const jit = unstable ? w * 0.32 : 0;

  c.save();
  c.globalCompositeOperation = 'lighter';
  c.lineCap = 'round';
  c.shadowColor = color;

  const layers = [
    { m: 4.0,  a: 0.10, blur: 46 },
    { m: 2.2,  a: 0.20, blur: 30 },
    { m: 1.25, a: 0.45, blur: 16 }
  ];
  for (const L of layers){
    c.globalAlpha = clamp(L.a * intensity, 0, 1);
    c.lineWidth   = w * L.m;
    c.strokeStyle = color;
    c.shadowBlur  = L.blur;
    bladePath(c, ax, ay, bx, by, jit, t, seed);
    c.stroke();
  }

  c.globalAlpha = clamp(0.98 * intensity, 0, 1);
  c.lineWidth   = w * 0.5;
  c.strokeStyle = core;
  c.shadowColor = core;
  c.shadowBlur  = 12;
  bladePath(c, ax, ay, bx, by, jit, t, seed);
  c.stroke();

  c.restore();
}

function drawDarksaber(c, ax, ay, bx, by, w, t, e){
  if (e <= 0.004) return;
  const dx = bx - ax, dy = by - ay;
  const len = Math.hypot(dx, dy) || 1;
  const ux = dx / len, uy = dy / len;
  const px = -uy, py = ux;

  const wn = w / 2;
  const wt = w * 0.19;

  const poly = (scale) => {
    c.beginPath();
    c.moveTo(ax + px * wn * scale, ay + py * wn * scale);
    c.lineTo(bx + px * wt * scale, by + py * wt * scale);
    c.lineTo(bx - px * wt * scale, by - py * wt * scale);
    c.lineTo(ax - px * wn * scale, ay - py * wn * scale);
    c.closePath();
  };

  c.save();
  c.globalCompositeOperation = 'lighter';
  c.shadowColor = '#d8ecff';
  c.shadowBlur = 34;
  poly(1.0);
  c.fillStyle = `rgba(200,225,255,${0.16 * e})`;
  c.fill();
  c.lineWidth = 11;
  c.strokeStyle = `rgba(200,225,255,${0.16 * e})`;
  c.stroke();
  c.restore();

  poly(1.0);
  c.fillStyle = '#05070a';
  c.fill();
  c.lineWidth = 2;
  c.strokeStyle = `rgba(225,242,255,${0.92 * e})`;
  c.stroke();

  c.save();
  poly(0.94);
  c.clip();
  c.strokeStyle = `rgba(230,245,255,${0.75 * e})`;
  c.lineWidth = 1.1;
  const steps = 9;
  for (let i = 0; i < steps; i++){
    const f = (i + 0.5) / steps;
    const cx = ax + dx * f, cy = ay + dy * f;
    const s = Math.sin(t * 19 + i * 4.7) * wn * 0.55;
    c.beginPath();
    c.moveTo(cx + px * s, cy + py * s);
    c.lineTo(cx - px * s * 0.8, cy - py * s * 0.8);
    c.stroke();
  }
  c.restore();

  c.beginPath();
  c.moveTo(ax, ay);
  c.lineTo(bx, by);
  c.strokeStyle = `rgba(255,255,255,${0.25 * e})`;
  c.lineWidth = 1;
  c.stroke();
}

function drawEmitter(c, x, y, w, h, s){
  const type = s.emitter;
  const r = type === 'rounded' ? h * 0.45 : 4;

  if (type === 'angled'){
    c.beginPath();
    c.moveTo(x + w * 0.12, y);
    c.lineTo(x + w, y + h * 0.30);
    c.lineTo(x + w, y + h);
    c.lineTo(x, y + h);
    c.lineTo(x, y + h * 0.12);
    c.closePath();
  } else {
    rr(c, x, y, w, h, r);
  }
  c.fillStyle = metalGrad(x, x + w, s.hilt);
  c.fill();
  c.strokeStyle = 'rgba(0,0,0,.6)';
  c.lineWidth = 1.2;
  c.stroke();

  if (type === 'vented'){
    for (let i = 0; i < 4; i++){
      const sx = x + w * (0.16 + i * 0.2);
      rr(c, sx, y + h * 0.2, w * 0.09, h * 0.6, 2);
      c.fillStyle = 'rgba(0,0,0,.85)';
      c.fill();
    }
  }

  if (type === 'claw'){
    c.fillStyle = metalGrad(x, x + w, s.hilt);
    for (const sgn of [-1, 1]){
      const bx = sgn < 0 ? x : x + w;
      c.beginPath();
      c.moveTo(bx, y + h * 0.62);
      c.lineTo(bx + sgn * w * 0.05, y - h * 0.62);
      c.lineTo(bx - sgn * w * 0.18, y - h * 0.42);
      c.lineTo(bx - sgn * w * 0.2,  y + h * 0.66);
      c.closePath();
      c.fill();
      c.strokeStyle = 'rgba(0,0,0,.5)';
      c.lineWidth = 1;
      c.stroke();
    }
  }

  if (type === 'rounded'){
    c.beginPath();
    c.moveTo(x, y + h * 0.66);
    c.lineTo(x + w, y + h * 0.66);
    c.strokeStyle = 'rgba(0,0,0,.35)';
    c.lineWidth = 2;
    c.stroke();
  }

  const aw = w * 0.66;
  rr(c, -aw / 2, y + h * 0.05, aw, h * 0.17, 3);
  c.fillStyle = '#05070a';
  c.fill();

  c.beginPath();
  c.moveTo(x + w * 0.2, y + h * 0.12);
  c.lineTo(x + w * 0.2, y + h * 0.9);
  c.strokeStyle = 'rgba(255,255,255,.10)';
  c.lineWidth = 2;
  c.stroke();
}

function drawGrip(c, x, y, w, h, s, t){
  rr(c, x, y, w, h, 4);
  c.fillStyle = metalGrad(x, x + w, s.hilt);
  c.fill();
  c.strokeStyle = 'rgba(0,0,0,.55)';
  c.lineWidth = 1;
  c.stroke();

  c.save();
  rr(c, x, y, w, h, 4);
  c.clip();

  const g = s.grip;

  if (g === 'ribbed'){
    const n = 9;
    for (let i = 0; i < n; i++){
      const yy = y + h * (i + 0.5) / n;
      c.fillStyle = 'rgba(0,0,0,.45)';
      c.fillRect(x, yy, w, h * 0.035);
      c.fillStyle = 'rgba(255,255,255,.09)';
      c.fillRect(x, yy + h * 0.035, w, h * 0.012);
    }
  } else if (g === 'smooth'){
    c.fillStyle = 'rgba(0,0,0,.25)';
    c.fillRect(x, y + h * 0.08, w, h * 0.03);
    c.fillRect(x, y + h * 0.88, w, h * 0.03);
  } else if (g === 'wrapped'){
    c.fillStyle = rgba(s.accent, 0.78);
    c.fillRect(x, y + h * 0.06, w, h * 0.88);
    c.strokeStyle = 'rgba(0,0,0,.35)';
    c.lineWidth = 1.5;
    for (let i = -8; i < 20; i++){
      c.beginPath();
      c.moveTo(x, y + i * h * 0.09);
      c.lineTo(x + w, y + i * h * 0.09 + h * 0.05);
      c.stroke();
    }
  } else if (g === 'segmented'){
    const n = 5;
    for (let i = 0; i < n; i++){
      const yy = y + h * 0.08 + i * (h * 0.84 / n);
      const hh = (h * 0.84 / n) * 0.68;
      rr(c, x + w * 0.05, yy, w * 0.9, hh, 3);
      c.fillStyle = i % 2 ? rgba(s.accent, 0.92) : 'rgba(255,255,255,.07)';
      c.fill();
    }
  } else if (g === 'panel'){
    rr(c, x + w * 0.1, y + h * 0.28, w * 0.8, h * 0.36, 3);
    c.fillStyle = 'rgba(0,0,0,.62)';
    c.fill();
    c.strokeStyle = 'rgba(255,255,255,.12)';
    c.lineWidth = 1;
    c.stroke();

    c.fillStyle = s.blade;
    c.beginPath();
    c.arc(x + w * 0.3, y + h * 0.4, w * 0.065, 0, Math.PI * 2);
    c.fill();

    c.fillStyle = '#ff4444';
    c.beginPath();
    c.arc(x + w * 0.3, y + h * 0.55, w * 0.05, 0, Math.PI * 2);
    c.fill();

    c.fillStyle = 'rgba(255,255,255,.16)';
    c.fillRect(x + w * 0.5, y + h * 0.36, w * 0.3, h * 0.05);
  }

  c.fillStyle = 'rgba(255,255,255,.10)';
  c.fillRect(x + w * 0.14, y, w * 0.08, h);
  c.fillStyle = 'rgba(0,0,0,.25)';
  c.fillRect(x + w * 0.78, y, w * 0.22, h);

  c.restore();
}

function drawPommel(c, x, y, w, h, s){
  const type = s.pommel;

  if (type === 'cone'){
    c.beginPath();
    c.moveTo(x, y);
    c.lineTo(x + w, y);
    c.lineTo(x + w * 0.62, y + h);
    c.lineTo(x + w * 0.38, y + h);
    c.closePath();
    c.fillStyle = metalGrad(x, x + w, s.hilt);
    c.fill();
    c.strokeStyle = 'rgba(0,0,0,.55)';
    c.lineWidth = 1;
    c.stroke();
  } else {
    const r = type === 'rounded' ? h * 0.5 : 4;
    rr(c, x, y, w, h, r);
    c.fillStyle = metalGrad(x, x + w, s.hilt);
    c.fill();
    c.strokeStyle = 'rgba(0,0,0,.55)';
    c.lineWidth = 1;
    c.stroke();

    if (type === 'ring'){
      c.beginPath();
      c.ellipse(x + w / 2, y + h * 0.52, w * 0.16, h * 0.26, 0, 0, Math.PI * 2);
      c.fillStyle = '#05070a';
      c.fill();
      c.strokeStyle = 'rgba(255,255,255,.12)';
      c.lineWidth = 1;
      c.stroke();
    }
  }

  c.fillStyle = rgba(s.accent, 0.85);
  c.fillRect(x, y, w, h * 0.13);
}

function drawHilt(c, top, bottom, w, s, t){
  const L = bottom - top;
  const emH   = L * 0.18;
  const neckH = L * 0.07;
  const pomH  = L * 0.15;
  const gripH = L - emH - neckH - pomH;

  const y0 = top;
  const y1 = top + emH;
  const y2 = y1 + neckH;
  const y3 = y2 + gripH;

  c.save();
  c.lineJoin = 'round';

  const ew = w * 1.15;
  drawEmitter(c, -ew / 2, y0, ew, emH, s);
  cyl(c, 0, y1, w * 0.6, neckH, 3, s.accent);
  drawGrip(c, -w / 2, y2, w, gripH, s, t);
  drawPommel(c, -w / 2, y3, w, pomH, s);

  c.restore();
}

let igniteT = 1;
let igniting = true;
let last = performance.now();

function update(dt){
  if (igniting) igniteT = Math.min(1, igniteT + dt / 0.40);
  else          igniteT = Math.max(0, igniteT - dt / 0.28);
}
const easeOutCubic = x => 1 - Math.pow(1 - x, 3);

function render(t){
  ctx.setTransform(DPR, 0, 0, DPR, 0, 0);
  ctx.clearRect(0, 0, W, H);

  const s = state;

  if (!s.transparent){
    const bg = ctx.createRadialGradient(W / 2, H * 0.42, 0, W / 2, H * 0.5, Math.max(W, H) * 0.8);
    bg.addColorStop(0, '#0e1723');
    bg.addColorStop(0.55, '#070b12');
    bg.addColorStop(1, '#03050a');
    ctx.fillStyle = bg;
    ctx.fillRect(0, 0, W, H);

    for (const st of stars){
      const tw = 0.6 + 0.4 * Math.sin(t * 1.6 + st.p);
      ctx.fillStyle = `rgba(200,220,255,${st.a * tw})`;
      ctx.beginPath();
      ctx.arc(st.x, st.y, st.r, 0, Math.PI * 2);
      ctx.fill();
    }
  }

  const hiltLen  = 150;
  const hiltW    = 30;
  const bladeLen = s.bladeLen;
  const bladeW   = s.bladeW;

  const total = s.type === 'double' ? hiltLen + 2 * bladeLen : hiltLen + bladeLen;

  let scale = (H - 90) / total;
  scale = Math.min(scale, 1.75);
  scale = Math.max(scale, 0.15);

  ctx.save();
  ctx.translate(W / 2, H / 2);
  ctx.scale(scale, scale);

  const e = easeOutCubic(igniteT);
  const flick = 1 + Math.sin(t * 37) * 0.018 + Math.sin(t * 13.3) * 0.016;
  const intensity = e * flick * s.glow;

  const core = '#ffffff';

  if (s.type === 'darksaber'){
    const hiltTop = -total / 2 + bladeLen;
    const hiltBot = hiltTop + hiltLen;
    const tipY    = hiltTop - bladeLen * e;

    drawDarksaber(ctx, 0, hiltTop, 0, tipY, bladeW, t, e);
    drawHilt(ctx, hiltTop, hiltBot, hiltW, s, t);

    ctx.save();
    ctx.globalCompositeOperation = 'lighter';
    const fg = ctx.createRadialGradient(0, hiltTop, 0, 0, hiltTop, bladeW * 3);
    fg.addColorStop(0, `rgba(220,240,255,${0.4 * e})`);
    fg.addColorStop(1, 'rgba(220,240,255,0)');
    ctx.fillStyle = fg;
    ctx.beginPath();
    ctx.arc(0, hiltTop, bladeW * 3, 0, Math.PI * 2);
    ctx.fill();
    ctx.restore();

  } else if (s.type === 'double'){
    const topY = -hiltLen / 2;
    const botY =  hiltLen / 2;

    drawBlade(ctx, 0, topY, 0, topY - bladeLen * e, bladeW, s.blade, core, intensity, s.unstable, t, 0);
    drawBlade(ctx, 0, botY, 0, botY + bladeLen * e, bladeW, s.blade, core, intensity, s.unstable, t, 3.3);

    drawHilt(ctx, topY, botY, hiltW, s, t);

    ctx.save();
    ctx.globalCompositeOperation = 'lighter';
    for (const yy of [topY, botY]){
      const fg = ctx.createRadialGradient(0, yy, 0, 0, yy, bladeW * 3);
      fg.addColorStop(0, rgba(s.blade, 0.5 * e));
      fg.addColorStop(1, rgba(s.blade, 0));
      ctx.fillStyle = fg;
      ctx.beginPath();
      ctx.arc(0, yy, bladeW * 3, 0, Math.PI * 2);
      ctx.fill();
    }
    ctx.restore();

  } else {
    const hiltTop = -total / 2 + bladeLen;
    const hiltBot = hiltTop + hiltLen;
    const tipY    = hiltTop - bladeLen * e;

    drawBlade(ctx, 0, hiltTop, 0, tipY, bladeW, s.blade, core, intensity, s.unstable, t, 0);

    if (s.type === 'crossguard'){
      const emY  = hiltTop + 22;
      const qLen = Math.max(30, bladeLen * 0.13) * e;
      const ang  = 1.15;
      for (const sgn of [-1, 1]){
        const ox = sgn * hiltW * 0.35;
        const bx = ox + sgn * Math.sin(ang) * qLen;
        const by = emY - Math.cos(ang) * qLen;
        drawBlade(ctx, ox, emY, bx, by, bladeW * 0.85, s.blade, core, intensity, true, t, sgn * 5.1);
      }
    }

    drawHilt(ctx, hiltTop, hiltBot, hiltW, s, t);

    ctx.save();
    ctx.globalCompositeOperation = 'lighter';
    const fg = ctx.createRadialGradient(0, hiltTop, 0, 0, hiltTop, bladeW * 3);
    fg.addColorStop(0, rgba(s.blade, 0.55 * e));
    fg.addColorStop(1, rgba(s.blade, 0));
    ctx.fillStyle = fg;
    ctx.beginPath();
    ctx.arc(0, hiltTop, bladeW * 3, 0, Math.PI * 2);
    ctx.fill();
    ctx.restore();
  }

  ctx.restore();
}

function frame(now){
  const dt = Math.min(0.05, (now - last) / 1000);
  last = now;
  update(dt);
  render(now / 1000);
  requestAnimationFrame(frame);
}
requestAnimationFrame(frame);

/* ========== AUDIO ========== */
let actx = null, humNodes = null, humOn = false;

function initAudio(){
  if (actx) return;
  const AC = window.AudioContext || window.webkitAudioContext;
  if (AC) actx = new AC();
}

function startHum(){
  initAudio();
  if (!actx || humNodes) return;
  if (actx.state === 'suspended') actx.resume();

  const out = actx.createGain();
  out.gain.value = 0;
  out.connect(actx.destination);

  const filt = actx.createBiquadFilter();
  filt.type = 'lowpass';
  filt.frequency.value = 330;
  filt.Q.value = 7;
  filt.connect(out);

  const o1 = actx.createOscillator(); o1.type = 'sawtooth'; o1.frequency.value = 55;
  const o2 = actx.createOscillator(); o2.type = 'sawtooth'; o2.frequency.value = 82.6;
  const o3 = actx.createOscillator(); o3.type = 'square';   o3.frequency.value = 27.5;

  const g3 = actx.createGain(); g3.gain.value = 0.28;
  o1.connect(filt);
  o2.connect(filt);
  o3.connect(g3); g3.connect(filt);

  const lfo = actx.createOscillator(); lfo.type = 'sine'; lfo.frequency.value = 0.65;
  const lfoGain = actx.createGain(); lfoGain.gain.value = 95;
  lfo.connect(lfoGain); lfoGain.connect(filt.frequency);

  const lfo2 = actx.createOscillator(); lfo2.type = 'sine'; lfo2.frequency.value = 5.3;
  const lfo2Gain = actx.createGain(); lfo2Gain.gain.value = 3.5;
  lfo2.connect(lfo2Gain); lfo2Gain.connect(o2.detune);

  o1.start(); o2.start(); o3.start(); lfo.start(); lfo2.start();

  out.gain.linearRampToValueAtTime(0.055, actx.currentTime + 0.35);
  humNodes = { out, o1, o2, o3, lfo, lfo2 };
}

function stopHum(){
  if (!actx || !humNodes) return;
  const n = humNodes;
  humNodes = null;
  const now = actx.currentTime;
  n.out.gain.cancelScheduledValues(now);
  n.out.gain.setValueAtTime(n.out.gain.value, now);
  n.out.gain.linearRampToValueAtTime(0.0001, now + 0.25);
  setTimeout(() => {
    try {
      n.o1.stop(); n.o2.stop(); n.o3.stop(); n.lfo.stop(); n.lfo2.stop();
    } catch (e) {}
  }, 400);
}

function whoosh(up){
  initAudio();
  if (!actx) return;
  if (actx.state === 'suspended') actx.resume();

  const o = actx.createOscillator();
  o.type = 'sawtooth';
  const f = actx.createBiquadFilter();
  f.type = 'lowpass';
  f.frequency.value = 1400;
  const g = actx.createGain();

  o.connect(f); f.connect(g); g.connect(actx.destination);

  const now = actx.currentTime;
  if (up){
    o.frequency.setValueAtTime(90, now);
    o.frequency.exponentialRampToValueAtTime(430, now + 0.18);
  } else {
    o.frequency.setValueAtTime(420, now);
    o.frequency.exponentialRampToValueAtTime(80, now + 0.22);
  }
  g.gain.setValueAtTime(0.0001, now);
  g.gain.exponentialRampToValueAtTime(0.13, now + 0.04);
  g.gain.exponentialRampToValueAtTime(0.0001, now + 0.36);

  o.start(now);
  o.stop(now + 0.42);
}

/* ========== UI ========== */
const $ = id => document.getElementById(id);

const charsEl = $('chars');
function buildChars(filter = ''){
  charsEl.innerHTML = '';
  const f = filter.trim().toLowerCase();
  PRESETS.forEach(p => {
    if (f && !p.name.toLowerCase().includes(f)) return;
    const b = document.createElement('button');
    b.className = 'char' + (p.name === state.preset ? ' active' : '');
    b.innerHTML = `<span class="dot" style="background:${p.blade};color:${p.blade}"></span><span>${p.name}</span>`;
    b.onclick = () => applyPreset(p);
    charsEl.appendChild(b);
  });
}
buildChars();

$('search').addEventListener('input', e => buildChars(e.target.value));

function applyPreset(p){
  const keepTransparent = state.transparent;
  Object.assign(state, BASE, p);
  state.preset = p.name;
  state.transparent = keepTransparent;
  syncUI();
  buildChars($('search').value);
  ignite(true);
}

function syncUI(){
  $('blade').value    = toHex(state.blade);
  $('hilt').value     = toHex(state.hilt);
  $('accent').value   = toHex(state.accent);
  $('type').value     = state.type;
  $('bladeLen').value = state.bladeLen;
  $('bladeW').value   = state.bladeW;
  $('glow').value     = state.glow;
  $('emitter').value  = state.emitter;
  $('grip').value     = state.grip;
  $('pommel').value   = state.pommel;
  $('unstable').checked = !!state.unstable;
}

function toHex(c){
  if (/^#[0-9a-f]{6}$/i.test(c)) return c;
  const { r, g, b } = hexToRgb(c);
  return '#' + [r, g, b].map(v => v.toString(16).padStart(2, '0')).join('');
}

$('blade').addEventListener('input', e => { state.blade = e.target.value; });
$('hilt').addEventListener('input',  e => { state.hilt  = e.target.value; });
$('accent').addEventListener('input',e => { state.accent = e.target.value; });
$('type').addEventListener('change', e => { state.type = e.target.value; ignite(true); });
$('bladeLen').addEventListener('input', e => { state.bladeLen = +e.target.value; });
$('bladeW').addEventListener('input',   e => { state.bladeW   = +e.target.value; });
$('glow').addEventListener('input',     e => { state.glow     = +e.target.value; });
$('emitter').addEventListener('change', e => { state.emitter  = e.target.value; });
$('grip').addEventListener('change',    e => { state.grip     = e.target.value; });
$('pommel').addEventListener('change',  e => { state.pommel   = e.target.value; });
$('unstable').addEventListener('change',e => { state.unstable = e.target.checked; });

function ignite(on){
  igniting = on;
  if (humOn) whoosh(on);
}

$('ignite').addEventListener('click', () => {
  igniting = !igniting;
  if (humOn) whoosh(igniting);
  $('ignite').textContent = igniting ? '⚡ Ignite' : '⭘ Extinguish';
});

const pick = a => a[Math.floor(Math.random() * a.length)];
const rnd  = (a, b) => a + Math.random() * (b - a);
function randomColor(){
  return pick(['#3fa9ff','#3ff06a','#ff2b2b','#b06bff','#ffd23f','#ff8a1f','#4ff0ff','#ffffff']);
}
function randomMetal(){
  const v = Math.round(rnd(40, 210));
  return '#' + [v, v, Math.min(255, v + 8)].map(x => x.toString(16).padStart(2,'0')).join('');
}

$('random').addEventListener('click', () => {
  Object.assign(state, BASE, {
    blade:    randomColor(),
    type:     pick(['single','single','double','crossguard','darksaber']),
    bladeLen: Math.round(rnd(180, 440)),
    bladeW:   Math.round(rnd(10, 24)),
    glow:     +rnd(0.6, 1.6).toFixed(2),
    hilt:     randomMetal(),
    accent:   randomMetal(),
    emitter:  pick(['standard','vented','rounded','claw','angled']),
    grip:     pick(['ribbed','smooth','wrapped','segmented','panel']),
    pommel:   pick(['flat','rounded','ring','cone']),
    unstable: Math.random() < 0.25
  });
  state.preset = 'Custom Build';
  syncUI();
  buildChars($('search').value);
  ignite(true);
});

$('hum').addEventListener('click', () => {
  humOn = !humOn;
  if (humOn){
    startHum();
    $('hum').textContent = '🔊 Hum: On';
    $('hum').classList.add('on');
  } else {
    stopHum();
    $('hum').textContent = '🔊 Hum: Off';
    $('hum').classList.remove('on');
  }
});

$('bg').addEventListener('click', () => {
  state.transparent = !state.transparent;
  $('bg').textContent = state.transparent ? '🌌 Dark BG' : '🌌 Transparent BG';
  $('bg').classList.toggle('on', state.transparent);
});

$('save').addEventListener('click', () => {
  const prev = state.transparent;
  state.transparent = true;
  render(performance.now() / 1000);
  const a = document.createElement('a');
  a.href = canvas.toDataURL('image/png');
  a.download = 'lightsaber-' + state.preset.replace(/[^a-z0-9]+/gi, '-').toLowerCase() + '.png';
  a.click();
  state.transparent = prev;
});

const initPreset = PRESETS.find(p => p.name === state.preset) || PRESETS[0];
Object.assign(state, BASE, initPreset);
syncUI();
buildChars();
ignite(true);
</script>
</body>
</html>