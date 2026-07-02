[love_surprise_index.html](https://github.com/user-attachments/files/29616600/love_surprise_index.html)
<!DOCTYPE html><html lang="ru"><head><meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1"><title>Доброе утро, солнышко ❤️</title>
<style>
body{margin:0;font-family:system-ui;background:linear-gradient(135deg,#6a5cff,#ff7ac8);overflow:hidden;color:#fff}
#stars{position:fixed;inset:0}
.wrap{position:relative;z-index:2;display:flex;min-height:100vh;align-items:center;justify-content:center;padding:20px}
.card{max-width:760px;background:rgba(255,255,255,.12);backdrop-filter:blur(10px);padding:30px;border-radius:24px;text-align:center;box-shadow:0 0 30px rgba(255,255,255,.2)}
button{padding:14px 28px;border:none;border-radius:30px;font-size:20px;background:#fff;color:#e91e63;cursor:pointer}
#letter,#final{display:none;white-space:pre-line;font-size:20px;line-height:1.6}
.big{font-size:64px;animation:pulse 1.2s infinite}
@keyframes pulse{50%{transform:scale(1.1)}}
.heart{position:fixed;top:-20px;animation:fall linear forwards;pointer-events:none}
@keyframes fall{to{transform:translateY(110vh);opacity:0}}
</style></head><body>
<canvas id="stars"></canvas>
<div class="wrap"><div class="card">
<h1>☀️ Доброе утро, солнышко ❤️</h1>
<div id="start">
<p>У меня есть для тебя маленький сюрприз...</p>
<button onclick="openLetter()">Открыть конверт 💌</button>
</div>
<div id="letter"></div>
<div id="next" style="display:none"><br><button onclick="finish()">Последняя страница ❤️</button></div>
<div id="final"><div class="big">❤️</div><h2>Адия, я люблю тебя.</h2><p>Спасибо за твою улыбку, заботу и тепло.
Пусть сегодняшний день будет таким же прекрасным, как и ты.

Навсегда твой. ❤️</p></div>
</div></div>
<script>
const txt=`Привет, моя любимая Адия...

Мне хотелось подарить тебе не просто сообщение.

Мне хотелось сделать маленькое место,
куда ты сможешь зайти и улыбнуться.

Спасибо тебе за каждый день рядом.
За поддержку.
За объятия.
За всё, что мы переживаем вместе.

Ты делаешь мою жизнь счастливее.

❤️ Я очень сильно тебя люблю ❤️`;
function openLetter(){start.style.display='none';letter.style.display='block';let i=0;(function t(){if(i<txt.length){letter.textContent+=txt[i++];setTimeout(t,35)}else next.style.display='block'})()}
function finish(){letter.style.display='none';next.style.display='none';final.style.display='block';for(let i=0;i<180;i++)setTimeout(h,i*30)}
function h(){let d=document.createElement('div');d.className='heart';d.textContent='❤️';d.style.left=Math.random()*100+'vw';d.style.fontSize=(18+Math.random()*32)+'px';d.style.animationDuration=(3+Math.random()*3)+'s';document.body.appendChild(d);setTimeout(()=>d.remove(),7000)}
const c=document.getElementById('stars'),x=c.getContext('2d');function rs(){c.width=innerWidth;c.height=innerHeight}rs();onresize=rs;let s=[...Array(120)].map(()=>({x:Math.random()*c.width,y:Math.random()*c.height,r:Math.random()*2}));
(function a(){x.clearRect(0,0,c.width,c.height);x.fillStyle='white';for(let p of s){x.globalAlpha=.3+Math.random()*.7;x.beginPath();x.arc(p.x,p.y,p.r,0,7);x.fill()}requestAnimationFrame(a)})();
</script></body></html>
