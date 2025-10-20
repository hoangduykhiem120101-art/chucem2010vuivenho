<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Thư 20/10 gửi em Tuyết Anh • Bản ổn định</title>
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
  .sheet{position:absolute; left:50%; bottom:10px; tra
