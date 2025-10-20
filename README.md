<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Thư 20/10 gửi em Tuyết Anh</title>
<style>
  :root{ --paper:#fffaf5; --ink:#43253f; --accent:#e91e63; --bg1:#fce4ec; --bg2:#fff0f7; }
  *{box-sizing:border-box}
  html,body{height:100%;margin:0}
  body{
    background:linear-gradient(to top,var(--bg1) 0%,var(--bg2) 60%);
    font-family:system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
    color:var(--ink); overflow:hidden;
    display:flex; align-items:center; justify-content:center;
  }

  /* --- ENVELOPE (mở thư) --- */
  .stage{text-align:center; z-index:10; position:relative}
  .btn{margin-top:12px; border:none; padding:10px 16px; border-radius:999px;
       background:#ffffffc8; box-shadow:0 10px 22px rgba(0,0,0,.12);
       backdrop-filter:blur(6px); color:#7a2e4d; font-weight:700; cursor:pointer}
  .btn:hover{transform:translateY(-1px)}
  .envelope{width:min(360px,88vw); height:230px; margin:0 auto; perspective:1200px;
            filter:drop-shadow(0 18px 30px rgba(0,0,0,.16))}
  .env-body{width:100%; height:100%; position:relative; overflow:hidden;
            background:linear-gradient(180deg,#ffe9ef,#ffdbe7); border-radius:12px; border:1px solid #ffd1e1}
  .flap{position:absolute; left:0; right:0; top:0; height:60%; transform-origin:50% 0%;
        background:linear-gradient(180deg,#ffc1d6,#ffb0cd); clip-path:polygon(0 0,100% 0,50% 100%);
        border-top-left-radius:12px; border-top-right-radius:12px; box-shadow:inset 0 -6px 10px rgba(0,0,0,.08)}
  .seal{position:absolute; left:50%; top:44%; transform:translate(-50%,-50%);
        width:64px; height:64px; border-radius:50%; background:radial-gradient(circle at 30% 30%,#ff8fb3,#e91e63 70%);
        border:6px solid #ffd1e1; color:#fff; display:flex; align-items:center; justify-content:center; font-size:28px}
  .sheet{position:absolute; left:50%; bottom:10px; transform:translateX(-50%);
         width:86%; height:78%; background:#fffaf5; border-radius:10px; box-shadow:0 6px 18px rgba(0,0,0,.1)}
  .open .flap{animation:flip 1.2s ease forwards}
  @keyframes flip{0%{transform:rotateX(0)}60%{transform:rotateX(-170deg)}100%{transform:rotateX(-180deg)}}
  .open .seal{animation:pop .5s ease forwards}
  @keyframes pop{0%{transform:translate(-50%,-50%) scale(1)}100%{transform:translate(-50%,-200%) scale(0)}}
  .open .sheet{animation:slideUp 1.25s .45s ease forwards}
  @keyframes slideUp{0%{transform:translate(-50%,0);opacity:1}70%{transform:translate(-50%,-140%);opacity:1}100%{transform:translate(-50%,-150%);opacity:0}}

  /* --- LETTER (nội dung) --- */
  .wrap{position:absolute; inset:0; display:flex; align-items:center; justify-content:center;
        padding:18px; opacity:0; pointer-events:none; z-index:12; transition:opacity .6s ease .6s}
  .wrap.show{opacity:1; pointer-events:auto}
  .letter{width:min(820px,92vw); background:var(--paper); border-radius:20px;
          box-shadow:0 14px 40px rgba(0,0,0,.12); padding:clamp(18px,3.5vw,34px);
          border:1px solid rgba(0,0,0,.05);
          background-image:linear-gradient(180deg,rgba(255,255,255,.85),rgba(255,255,255,.85)),
                           repeating-linear-gradient(180deg,rgba(255,192,203,.12) 0 1px,transparent 1px 48px)}
  h1{margin:6px 0 8px; text-align:center; color:var(--accent); font-size:clamp(24px,5.5vw,44px)}
  .hand{font-size:clamp(18px,3.3vw,28px); line-height:1.55}
  .hand p{margin:.35em 0}
  .closing{text-align:right; margin-top:10px; font-size:clamp(20px,3.5vw,30px); color:#b31359}

  /* --- PETALS (cánh hoa bay) --- */
  canvas{position:fixed; bottom:0; left:0; width:100vw; height:58vh; z-index:0}
</style>
</head>
<body>
  <!-- Phong bì -->
  <div class="stage" id="stage">
    <div class="envelope" id="envelope">
      <div class="env-body">
        <div class="flap"></div>
        <div class="seal">💮</div>
        <div class="sheet"></div>
      </div>
    </div>
    <button class="btn" id="openBtn">Mở thư của em 💌</button>
  </div>

  <!-- Bức thư -->
  <div class="wrap" id="letterWrap" aria-hidden="true">
    <div class="letter">
      <h1>💐 Chúc Mừng Tuyết Anh Ngày 20/10 💐</h1>

      <div class="hand">
        <p>
          Nhân dịp Ngày Phụ Nữ Việt Nam 20/10, chúc <b>Tuyết Anh</b> một ngày thật vui vẻ,
          ý nghĩa và đong đầy những điều tốt đẹp.
        </p>

        <p>
          Chúc em luôn giữ được nụ cười rạng rỡ, sự tự tin và năng lượng tích cực vốn có.
          Hãy luôn mạnh mẽ, xinh đẹp và là nguồn cảm hứng cho những người xung quanh nhé.
        </p>

        <p>
          Anh chúc em sẽ luôn thành công trên con đường mình chọn, gặt hái được nhiều thành tựu
          xứng đáng với sự nỗ lực của bản thân. Điều quan trọng là em phải luôn yêu thương bản thân
          và tận hưởng mọi khoảnh khắc tuyệt vời của cuộc sống.
        </p>

        <p><b>Mọi điều tốt đẹp nhất sẽ đến với em!</b> 💖</p>
      </div>

      <div class="closing">— Gửi em 💞</div>
    </div>
  </div>

  <!-- Cánh hoa bay -->
  <canvas id="petals"></canvas>

  <!-- Nhạc (phát khi bấm mở thư để tránh chặn autoplay) -->
  <audio id="bgm" preload="auto" loop>
    <source src="https://cdn.pixabay.com/audio/2022/11/16/audio_37fa3e3f79.mp3" type="audio/mpeg">
  </audio>

<script>
  // Mở thư
  const openBtn = document.getElementById('openBtn');
  const envelope = document.getElementById('envelope');
  const stage = document.getElementById('stage');
  const letterWrap = document.getElementById('letterWrap');
  const bgm = document.getElementById('bgm');

  openBtn.addEventListener('click', async () => {
    envelope.classList.add('open');
    try { await bgm.play(); } catch(e) {}
    setTimeout(() => {
      stage.style.display = 'none';
      letterWrap.classList.add('show');
    }, 1600);
  });

  // Hoa rơi (emoji nhẹ, chạy mọi trình duyệt)
  const cvs = document.getElementById('petals');
  const ctx = cvs.getContext('2d');
  function resize(){ cvs.width = innerWidth; cvs.height = Math.max(260, innerHeight*0.58); }
  resize(); addEventListener('resize', resize);

  const PETALS = Array.from({length: 24}).map(() => ({
    x: Math.random()*innerWidth,
    y: Math.random()*cvs.height,
    e: ['🌸','💗','🌷'][Math.floor(Math.random()*3)],
    v: 0.5 + Math.random(),
    d: 0.2 + Math.random()*0.6
  }));

  (function loop(){
    ctx.clearRect(0,0,cvs.width,cvs.height);
    ctx.font = '20px serif';
    PETALS.forEach(p=>{
      ctx.fillText(p.e, p.x, p.y);
      p.y += p.v;
      p.x += Math.sin(p.y*0.02)*p.d;
      if(p.y > cvs.height){ p.y = -20; p.x = Math.random()*innerWidth; }
    });
    requestAnimationFrame(loop);
  })();
</script>
</body>
</html>
