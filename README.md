<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>I'm sorry, bestie 🌸</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;600;700;800&family=Quicksand:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --pink-1:#ffe4ec;
    --pink-2:#ffc2d6;
    --pink-3:#ff8fb3;
    --lav-1:#f1e8ff;
    --lav-2:#c9b3ff;
    --ink:#4a2a3a;
    --ink-soft:#7a5065;
    --cream:#fff9f5;
    --gold:#ffcf7a;
    --mint:#bdf3d4;
  }
  *{box-sizing:border-box;}
  html,body{margin:0;padding:0;}
  body{
    min-height:100vh;
    font-family:'Quicksand', sans-serif;
    background:
      radial-gradient(circle at 15% 20%, var(--pink-1) 0%, transparent 45%),
      radial-gradient(circle at 85% 15%, var(--lav-1) 0%, transparent 40%),
      radial-gradient(circle at 50% 100%, var(--pink-1) 0%, transparent 50%),
      var(--cream);
    color:var(--ink);
    overflow-x:hidden;
    position:relative;
  }

  .floaters{
    position:fixed;
    inset:0;
    pointer-events:none;
    z-index:0;
    overflow:hidden;
  }
  .floaters span{
    position:absolute;
    font-size:28px;
    opacity:0.5;
    animation: drift 14s linear infinite;
  }
  @keyframes drift{
    from{ transform:translateY(110vh) rotate(0deg); }
    to{ transform:translateY(-10vh) rotate(360deg); }
  }

  /* progress dots */
  .progress{
    position:sticky;
    top:0;
    z-index:3;
    display:flex;
    justify-content:center;
    gap:8px;
    padding:16px 0 6px;
    background:linear-gradient(var(--cream) 60%, transparent);
  }
  .dot{
    width:8px;
    height:8px;
    border-radius:999px;
    background:var(--pink-2);
    transition:all 0.3s ease;
  }
  .dot.active{
    width:22px;
    background:var(--pink-3);
  }
  .dot.done{
    background:var(--ink);
  }

  .wrap{
    position:relative;
    z-index:1;
    max-width:640px;
    margin:0 auto;
    padding:20px 24px 90px;
    text-align:center;
    min-height:70vh;
  }

  .screen{
    display:none;
    animation: fadeUp 0.5s ease both;
  }
  .screen.active{ display:block; }
  @keyframes fadeUp{
    from{ opacity:0; transform:translateY(14px); }
    to{ opacity:1; transform:translateY(0); }
  }

  .badge{
    display:inline-block;
    background:var(--pink-2);
    color:var(--ink);
    font-weight:600;
    font-size:13px;
    letter-spacing:0.3px;
    padding:7px 18px;
    border-radius:999px;
    margin-bottom:22px;
  }

  h1, h2.title{
    font-family:'Baloo 2', sans-serif;
    font-weight:800;
    line-height:1.1;
    margin:0 0 18px;
    color:var(--ink);
  }
  h1{ font-size:clamp(32px, 8vw, 52px); }
  h2.title{ font-size:clamp(26px, 6vw, 38px); }

  .heart{
    display:inline-block;
    animation: beat 1.1s ease-in-out infinite;
  }
  @keyframes beat{
    0%,100%{ transform:scale(1); }
    50%{ transform:scale(1.18); }
  }

  p.lead{
    font-size:17px;
    line-height:1.6;
    color:var(--ink-soft);
    max-width:480px;
    margin:0 auto 8px;
  }

  .card{
    background:#ffffffcc;
    backdrop-filter: blur(6px);
    border:1px solid #ffffff;
    border-radius:28px;
    padding:30px 26px;
    margin:28px 0;
    box-shadow: 0 18px 40px -20px rgba(255,143,179,0.45);
    text-align:left;
  }
  .card h3{
    font-family:'Baloo 2', sans-serif;
    font-size:20px;
    margin:0 0 14px;
    color:var(--ink);
  }
  .reasons{
    list-style:none;
    margin:0;
    padding:0;
    display:grid;
    gap:12px;
  }
  .reasons li{
    display:flex;
    gap:12px;
    align-items:flex-start;
    font-size:16px;
    line-height:1.5;
    color:var(--ink-soft);
  }
  .reasons li span.icon{
    flex:none;
    font-size:20px;
    line-height:1;
    margin-top:1px;
  }

  .meter-box{ margin:28px 0; text-align:left; }
  .meter-label{
    display:flex;
    justify-content:space-between;
    font-size:14px;
    font-weight:600;
    color:var(--ink-soft);
    margin-bottom:8px;
  }
  .meter-track{
    height:22px;
    background:#ffffff;
    border:1px solid var(--pink-2);
    border-radius:999px;
    overflow:hidden;
  }
  .meter-fill{
    height:100%;
    width:0%;
    background:linear-gradient(90deg, var(--pink-3), var(--gold));
    border-radius:999px;
    transition:width 0.5s ease;
  }

  button{
    font-family:'Quicksand', sans-serif;
    cursor:pointer;
    border:none;
  }
  .hug-btn{
    margin-top:14px;
    font-weight:700;
    font-size:15px;
    color:var(--ink);
    background:var(--mint);
    padding:10px 20px;
    border-radius:999px;
    transition:transform 0.15s ease;
  }
  .hug-btn:active{ transform:scale(0.95); }

  .btn-row{
    position:relative;
    display:flex;
    gap:18px;
    justify-content:center;
    align-items:center;
    min-height:120px;
    flex-wrap:wrap;
    margin-top:10px;
  }
  button.big{
    font-weight:700;
    font-size:17px;
    padding:16px 30px;
    border-radius:999px;
  }
  #yesBtn{
    background:var(--ink);
    color:#fff;
    box-shadow: 0 10px 24px -10px rgba(74,42,58,0.6);
    transition: transform 0.15s ease, font-size 0.3s ease, padding 0.3s ease;
  }
  #yesBtn:active{ transform:scale(0.96); }
  #noBtn{
    background:#fff;
    color:var(--ink-soft);
    border:2px solid var(--pink-2);
    position:relative;
    transition:transform 0.12s ease;
  }
  .note{
    font-size:13px;
    color:#b78a9b;
    margin-top:14px;
  }

  .next-row{
    display:flex;
    justify-content:center;
    margin-top:32px;
  }
  .next-btn{
    background:var(--ink);
    color:#fff;
    font-weight:700;
    font-size:16px;
    padding:14px 34px;
    border-radius:999px;
    box-shadow: 0 10px 24px -10px rgba(74,42,58,0.6);
    transition:transform 0.15s ease;
  }
  .next-btn:active{ transform:scale(0.96); }

  .promise-list{
    list-style:none;
    margin:0;
    padding:0;
    display:grid;
    gap:14px;
    text-align:left;
  }
  .promise-list li{
    display:flex;
    gap:12px;
    align-items:flex-start;
    background:#fff;
    border-radius:16px;
    padding:14px 16px;
    box-shadow: 0 8px 20px -14px rgba(74,42,58,0.35);
    font-size:15px;
    color:var(--ink-soft);
  }
  .promise-list input[type="checkbox"]{
    margin-top:3px;
    width:18px;
    height:18px;
    accent-color: var(--pink-3);
    flex:none;
  }

  .gift-box{
    font-size:80px;
    margin:20px 0 6px;
    cursor:pointer;
    user-select:none;
    transition:transform 0.2s ease;
    display:inline-block;
  }
  .gift-box:active{ transform:scale(0.9) rotate(-4deg); }
  .gift-reveal{
    display:none;
    margin-top:10px;
    font-family:'Baloo 2', sans-serif;
    font-size:20px;
    color:var(--ink);
  }
  .gift-reveal.show{ display:block; }

  .final-heart{
    font-size:64px;
    margin-bottom:6px;
  }

  footer{
    text-align:center;
    font-size:13px;
    color:#c79bad;
    padding-bottom:20px;
  }

  .confetti{
    position:fixed;
    top:-20px;
    z-index:5;
    border-radius:2px;
    pointer-events:none;
  }

  .restart{
    margin-top:26px;
    background:transparent;
    color:var(--ink-soft);
    text-decoration:underline;
    font-size:14px;
  }
</style>
</head>
<body>

<div class="floaters" id="floaters"></div>

<div class="progress" id="progress"></div>

<div class="wrap">

  <!-- SCREEN 1: apology + ask -->
  <section class="screen active" data-screen="1">
    <span class="badge">a very important message</span>
    <h1>I messed up<br>and I'm <span class="heart">💗</span> sorry</h1>
    <p class="lead">You're my favourite person and I hate that you're upset with me right now. So I built you this instead of just texting "sorry" like a normal person.</p>

    <div class="card">
      <h3>Here's what I know</h3>
      <ul class="reasons">
        <li><span class="icon">🙈</span> I was wrong, and I'm not going to make excuses for it.</li>
        <li><span class="icon">🫂</span> You deserve better than how things went.</li>
        <li><span class="icon">💌</span> I miss you already and it's only been this long.</li>
        <li><span class="icon">🌷</span> I'm genuinely going to do better, not just say it.</li>
      </ul>
    </div>

    <div class="meter-box">
      <div class="meter-label"><span>Sorry-meter</span><span id="meterPct">0%</span></div>
      <div class="meter-track"><div class="meter-fill" id="meterFill"></div></div>
      <button class="hug-btn" id="hugBtn">Send a virtual hug 🤗</button>
    </div>

    <h2 class="title" style="font-size:24px; margin-top:38px;">Will you forgive me?</h2>
    <div class="btn-row">
      <button class="big" id="yesBtn">Yes, okay fine 💕</button>
      <button class="big" id="noBtn">No</button>
    </div>
    <div class="note">(the "no" button is a little shy, fair warning)</div>
  </section>

  <!-- SCREEN 2: memories -->
  <section class="screen" data-screen="2">
    <span class="badge">step 2 of 6</span>
    <h2 class="title">Remember when we were actually okay?</h2>
    <p class="lead">Before I go any further, let's rewind for a second.</p>
    <div class="card">
      <ul class="reasons">
        <li><span class="icon">🌟</span> All the random voice notes that turned into hour-long calls.</li>
        <li><span class="icon">🍕</span> Every time we said "last one" and ordered food anyway.</li>
        <li><span class="icon">😂</span> The inside jokes nobody else understands, and never will.</li>
        <li><span class="icon">🫶</span> How you always show up, even when it's inconvenient for you.</li>
      </ul>
    </div>
    <p class="lead">That's the friendship I don't want to lose over this.</p>
    <div class="next-row"><button class="next-btn" data-next="3">Keep going →</button></div>
  </section>

  <!-- SCREEN 3: promises -->
  <section class="screen" data-screen="3">
    <span class="badge">step 3 of 6</span>
    <h2 class="title">Here's what I promise</h2>
    <p class="lead">Tap each one — I mean all of them.</p>
    <ul class="promise-list">
      <li><input type="checkbox"><span>I'll actually listen next time, instead of getting defensive.</span></li>
      <li><input type="checkbox"><span>I'll think before I speak, especially when I'm upset.</span></li>
      <li><input type="checkbox"><span>I'll check in on you more, not just when I need something.</span></li>
      <li><input type="checkbox"><span>I'll never let something small turn into something this big again.</span></li>
    </ul>
    <div class="next-row"><button class="next-btn" data-next="4">Next →</button></div>
  </section>

  <!-- SCREEN 4: gift -->
  <section class="screen" data-screen="4">
    <span class="badge">step 4 of 6</span>
    <h2 class="title">A little something for you</h2>
    <p class="lead">Go on, open it.</p>
    <div class="gift-box" id="giftBox">🎁</div>
    <div class="gift-reveal" id="giftReveal">A permanent, unconditional, annoyingly-persistent bestie. That's me. Forever.</div>
    <div class="next-row"><button class="next-btn" data-next="5">Almost there →</button></div>
  </section>

  <!-- SCREEN 5: final ask -->
  <section class="screen" data-screen="5">
    <span class="badge">step 5 of 6</span>
    <h2 class="title">So... are we good?</h2>
    <p class="lead">No dodging buttons this time. I just want to hear it from you.</p>
    <div class="btn-row">
      <button class="big" id="yesBtn2">Yes, we're good 💕</button>
    </div>
  </section>

  <!-- SCREEN 6: celebration -->
  <section class="screen" data-screen="6">
    <div class="final-heart">💖</div>
    <h1>Best. Day. Ever.</h1>
    <p class="lead">Thank you for forgiving me. I owe you a real hug and your favourite snack, in person, very soon.</p>
    <p class="lead" style="margin-top:14px; font-weight:600; color:var(--ink);">Love you, bestie. Always.</p>
    <button class="restart" id="restartBtn">watch that again</button>
  </section>

</div>

<footer>made with 100% real feelings, 0% AI-generated apathy</footer>

<script>
  // floating hearts background
  const floaters = document.getElementById('floaters');
  const emojis = ['💗','🌸','✨','💌','🫧'];
  for(let i=0;i<16;i++){
    const s = document.createElement('span');
    s.textContent = emojis[i % emojis.length];
    s.style.left = Math.random()*100 + 'vw';
    s.style.animationDuration = (10 + Math.random()*10) + 's';
    s.style.animationDelay = (Math.random()*14) + 's';
    s.style.fontSize = (18 + Math.random()*20) + 'px';
    floaters.appendChild(s);
  }

  // progress dots
  const TOTAL = 6;
  const progress = document.getElementById('progress');
  for(let i=1;i<=TOTAL;i++){
    const d = document.createElement('div');
    d.className = 'dot';
    d.dataset.dot = i;
    progress.appendChild(d);
  }

  function goTo(n){
    document.querySelectorAll('.screen').forEach(sc => {
      sc.classList.toggle('active', Number(sc.dataset.screen) === n);
    });
    document.querySelectorAll('.dot').forEach(d => {
      const i = Number(d.dataset.dot);
      d.classList.toggle('active', i === n);
      d.classList.toggle('done', i < n);
    });
    window.scrollTo({top:0, behavior:'smooth'});
    if(n === 6){ launchConfetti(); }
  }
  goTo(1);

  document.querySelectorAll('[data-next]').forEach(btn => {
    btn.addEventListener('click', () => goTo(Number(btn.dataset.next)));
  });

  document.getElementById('restartBtn').addEventListener('click', () => {
    hugs = 0;
    meterFill.style.width = '0%';
    meterPct.textContent = '0%';
    dodges = 0;
    noBtn.textContent = 'No';
    noBtn.style.transform = 'translate(0,0)';
    document.getElementById('giftReveal').classList.remove('show');
    document.querySelectorAll('.promise-list input').forEach(cb => cb.checked = false);
    goTo(1);
  });

  // sorry-meter (screen 1)
  let hugs = 0;
  const meterFill = document.getElementById('meterFill');
  const meterPct = document.getElementById('meterPct');
  document.getElementById('hugBtn').addEventListener('click', () => {
    hugs = Math.min(hugs + 20, 100);
    meterFill.style.width = hugs + '%';
    meterPct.textContent = hugs + '%';
  });

  // dodging "no" button (screen 1)
  const noBtn = document.getElementById('noBtn');
  const btnRow = noBtn.closest('.btn-row');
  let dodges = 0;
  const dodgeMsgs = ["nope","try again","not today","still no","nice try","keep trying"];
  noBtn.addEventListener('mouseenter', dodge);
  noBtn.addEventListener('click', (e) => { e.preventDefault(); dodge(); });
  noBtn.addEventListener('touchstart', (e) => { e.preventDefault(); dodge(); }, {passive:false});

  function dodge(){
    const rowRect = btnRow.getBoundingClientRect();
    const maxX = Math.max(rowRect.width - 110, 20);
    const maxY = Math.max(rowRect.height - 50, 10);
    const x = Math.random()*maxX - maxX/2;
    const y = Math.random()*maxY - maxY/2;
    noBtn.style.transform = `translate(${x}px, ${y}px)`;
    dodges++;
    if(dodges <= dodgeMsgs.length){
      noBtn.textContent = dodgeMsgs[dodges-1];
    }
    const yesBtn = document.getElementById('yesBtn');
    const scale = Math.min(1 + dodges*0.04, 1.4);
    yesBtn.style.fontSize = (17*scale) + 'px';
    yesBtn.style.padding = (16*scale) + 'px ' + (30*scale) + 'px';
  }

  // yes on screen 1 -> go to screen 2
  document.getElementById('yesBtn').addEventListener('click', () => goTo(2));

  // gift box on screen 4
  document.getElementById('giftBox').addEventListener('click', function(){
    this.textContent = '💝';
    document.getElementById('giftReveal').classList.add('show');
  });

  // yes on screen 5 -> go to screen 6 (celebration + confetti)
  document.getElementById('yesBtn2').addEventListener('click', () => goTo(6));

  function launchConfetti(){
    const colors = ['#ff8fb3','#ffcf7a','#c9b3ff','#bdf3d4','#ffc2d6'];
    for(let i=0;i<60;i++){
      const c = document.createElement('div');
      c.className = 'confetti';
      c.style.left = Math.random()*100 + 'vw';
      c.style.width = (6 + Math.random()*6) + 'px';
      c.style.height = (6 + Math.random()*6) + 'px';
      c.style.background = colors[Math.floor(Math.random()*colors.length)];
      const duration = 2.5 + Math.random()*2;
      const rotate = Math.random()*360;
      c.style.transform = `rotate(${rotate}deg)`;
      c.style.transition = `transform ${duration}s ease-in, top ${duration}s ease-in, opacity ${duration}s ease-in`;
      document.body.appendChild(c);
      requestAnimationFrame(() => {
        c.style.top = '110vh';
        c.style.transform = `rotate(${rotate + 360}deg)`;
        c.style.opacity = '0.9';
      });
      setTimeout(() => c.remove(), duration*1000 + 300);
    }
  }
</script>

</body>
</html>
