<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>A Little Garden of Wishes 🍀</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,500;1,9..144,400&family=Nunito:wght@400;600;800&family=Caveat:wght@500;700&display=swap" rel="stylesheet">
<style>
:root{--em:#006B52;--fo:#004C3F;--li:#C9EB69;--pk:#F5A3C7;--bb:#EC75AD;--bl:#A9D1F0;--cr:#FFF5E9;
--ink:#004C3F;--glass:rgba(255,245,233,.42);--edge:rgba(255,255,255,.7);
--bg1:#FFF5E9;--bg2:#F5A3C7;--bg3:#A9D1F0;--bg4:#C9EB69;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--ink:#FFF5E9;--glass:rgba(0,76,63,.45);--edge:rgba(201,235,105,.35);--bg1:#004C3F;--bg2:#006B52;--bg3:#1d4b5c;--bg4:#5a2d49}}
*{box-sizing:border-box;margin:0}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{min-height:100svh;color:var(--ink);font-family:Nunito,system-ui,sans-serif;overflow-x:hidden;
background:radial-gradient(60% 40% at 15% 10%,rgba(236,117,173,.45),transparent 70%),radial-gradient(50% 40% at 90% 30%,rgba(169,209,240,.8),transparent 70%),radial-gradient(60% 40% at 30% 100%,rgba(201,235,105,.6),transparent 70%),linear-gradient(165deg,var(--bg1),var(--bg2) 45%,var(--bg3) 80%,var(--bg4));background-attachment:fixed}
body::after{content:"";position:fixed;inset:0;pointer-events:none;opacity:.18;mix-blend-mode:multiply;z-index:50;
background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence baseFrequency='.9' numOctaves='2'/%3E%3C/filter%3E%3Crect width='160' height='160' filter='url(%23n)' opacity='.6'/%3E%3C/svg%3E")}
h1,h2,.serif{font-family:Fraunces,Georgia,serif;font-weight:500}
.hand{font-family:Caveat,cursive}
.stage{display:none;min-height:100svh;padding:28px 18px 60px;flex-direction:column;align-items:center;justify-content:center;text-align:center;position:relative;z-index:2}
.stage.on{display:flex;animation:in .9s ease both}
@keyframes in{from{opacity:0;transform:scale(.97) translateY(14px);filter:blur(6px)}}
.glass{background:var(--glass);border:1px solid var(--edge);backdrop-filter:blur(16px) saturate(1.4);-webkit-backdrop-filter:blur(16px) saturate(1.4);box-shadow:0 10px 40px rgba(0,76,63,.18),inset 0 1px 0 rgba(255,255,255,.7)}
.btn{font:800 1.05rem Nunito,sans-serif;color:var(--ink);padding:15px 34px;border-radius:99px;cursor:pointer;margin-top:22px;transition:transform .25s,box-shadow .25s;animation:glow 3s ease-in-out infinite}
.btn:hover{transform:translateY(-3px) scale(1.04)}
.btn:focus-visible,.knob:focus-visible,.sound:focus-visible{outline:3px solid var(--bb);outline-offset:3px}
@keyframes glow{50%{box-shadow:0 10px 40px rgba(0,76,63,.18),0 0 34px rgba(236,117,173,.65)}}
/* hero */
.hero h1{font-size:clamp(2.6rem,10vw,5.2rem);line-height:1}
.hero p{max-width:30ch;margin-top:14px;font-size:1.15rem;line-height:1.5}
.hero .sub{font-family:Caveat;font-size:1.7rem;color:var(--bb);margin-top:10px}
.clover{width:min(250px,60vw);height:auto;color:var(--em);filter:drop-shadow(0 12px 22px rgba(0,76,63,.3));animation:spin 40s linear infinite}
@keyframes spin{to{transform:rotate(360deg)}}
.sticker{position:absolute;padding:8px 14px;border-radius:18px;font-weight:800;font-size:.85rem;animation:bob 5s ease-in-out infinite}
@keyframes bob{50%{transform:translateY(-10px) rotate(var(--r,0deg))}}
/* machine */
.stage h2{font-size:clamp(1.8rem,6vw,2.8rem)}
.machine{position:relative;width:min(300px,82vw);margin:20px auto 0}
.globe{position:relative;width:min(260px,72vw);aspect-ratio:1;margin:0 auto;border-radius:50%;overflow:hidden;
background:radial-gradient(circle at 30% 25%,rgba(255,255,255,.85),rgba(255,255,255,.15) 40%,rgba(169,209,240,.35));border:3px solid var(--edge);box-shadow:inset -14px -18px 40px rgba(0,107,82,.2),0 14px 40px rgba(0,76,63,.25)}
.globe.shake{animation:shake .15s infinite}
@keyframes shake{25%{transform:translate(3px,-2px) rotate(1.5deg)}75%{transform:translate(-3px,2px) rotate(-1.5deg)}}
.ball{position:absolute;width:36px;height:36px;border-radius:50%;left:0;top:0;will-change:transform;box-shadow:inset -4px -5px 8px rgba(0,0,0,.12)}
.ball::after{content:"";position:absolute;left:22%;top:16%;width:30%;height:22%;border-radius:50%;background:rgba(255,255,255,.8);transform:rotate(-30deg)}
.base{position:relative;margin-top:-34px;padding:46px 20px 20px;border-radius:30px 30px 40px 40px;background:linear-gradient(180deg,var(--em),var(--fo));color:var(--cr);display:flex;justify-content:space-between;align-items:center;box-shadow:0 14px 30px rgba(0,76,63,.35);z-index:1}
.chute{width:76px;height:44px;border-radius:12px 12px 26px 26px;background:rgba(0,0,0,.28);box-shadow:inset 0 6px 10px rgba(0,0,0,.4)}
.knob{width:76px;height:76px;border-radius:50%;border:0;cursor:pointer;background:radial-gradient(circle at 35% 30%,#fff,var(--pk) 45%,var(--bb));font-size:1.9rem;box-shadow:0 6px 16px rgba(0,0,0,.3);transition:transform 1s cubic-bezier(.3,1.4,.5,1)}
.knob.turn{transform:rotate(360deg)}
.drop{position:absolute;left:50%;width:44px;height:44px;margin-left:-22px;border-radius:50%;z-index:3;top:40%;opacity:0;box-shadow:inset -5px -6px 10px rgba(0,0,0,.14)}
.drop.go{animation:fall 1.1s cubic-bezier(.5,0,.75,.4) forwards}
@keyframes fall{0%{opacity:1;top:60%}60%{opacity:1;top:108%}75%{top:100%}90%{top:108%}100%{opacity:1;top:108%;transform:scale(1.3)}}
.wish{min-height:112px;width:min(340px,88vw);margin-top:34px;padding:20px 22px;border-radius:28px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:6px}
.wish .serif{font-size:1.25rem;line-height:1.35;font-style:italic}
.wish.pop{animation:pop .7s cubic-bezier(.3,1.5,.5,1)}
@keyframes pop{from{transform:scale(.4) rotate(-6deg);opacity:0}}
.hint{font-family:Caveat;font-size:1.4rem}
.sound{position:fixed;top:calc(12px + env(safe-area-inset-top,0px));right:12px;z-index:60;border:0;border-radius:99px;padding:9px 14px;font:700 .85rem Nunito;color:var(--ink);cursor:pointer}
/* envelope */
.env{position:relative;width:min(300px,78vw);aspect-ratio:1;margin:26px auto 0;cursor:pointer}
.env .core{position:absolute;inset:22%;border-radius:50%;background:radial-gradient(circle,#fffbe0,var(--li) 60%,transparent 72%);opacity:0;transition:opacity 1s}
.petal{position:absolute;width:50%;height:50%;left:25%;top:25%;border-radius:50% 50% 50% 50%/60% 60% 40% 40%;background:linear-gradient(160deg,var(--cr),var(--pk));border:1px solid var(--edge);box-shadow:0 8px 20px rgba(236,117,173,.35);transform-origin:50% 100%;transition:transform 1.5s cubic-bezier(.3,1.2,.4,1),opacity 1.2s .3s}
.petal:nth-of-type(1){transform:translateY(-66%)}.petal:nth-of-type(2){transform:translateX(66%) rotate(90deg)}
.petal:nth-of-type(3){transform:translateY(66%) rotate(180deg)}.petal:nth-of-type(4){transform:translateX(-66%) rotate(270deg)}
.env.float .petal{animation:sway 4s ease-in-out infinite}
@keyframes sway{50%{filter:brightness(1.08)}}
.seal{position:absolute;left:50%;top:50%;width:84px;height:84px;margin:-42px;border-radius:50%;background:radial-gradient(circle at 35% 30%,var(--li),var(--em));display:grid;place-items:center;font-size:2.4rem;box-shadow:0 6px 18px rgba(0,76,63,.4);z-index:2;transition:transform 1s,opacity 1s}
.env.open .core{opacity:1;animation:pulse 1.6s ease-in-out infinite}
@keyframes pulse{50%{transform:scale(1.25)}}
.env.open .petal{opacity:.0}
.env.open .petal:nth-of-type(1){transform:translateY(-190%) scale(1.3) rotate(-20deg)}
.env.open .petal:nth-of-type(2){transform:translateX(190%) rotate(130deg) scale(1.3)}
.env.open .petal:nth-of-type(3){transform:translateY(190%) rotate(220deg) scale(1.3)}
.env.open .petal:nth-of-type(4){transform:translateX(-190%) rotate(230deg) scale(1.3)}
.env.open .seal{transform:scale(2.4);opacity:0}
/* letter */
.letter-wrap{width:min(680px,100%);padding:14px;border-radius:34px}
.paper{position:relative;padding:34px 26px 30px;border-radius:22px;color:#3b2a2f;text-align:left;
background:radial-gradient(circle at 0 0,rgba(245,163,199,.35),transparent 30%),radial-gradient(circle at 100% 100%,rgba(201,235,105,.4),transparent 30%),#FFF9EF;box-shadow:inset 0 0 40px rgba(180,140,100,.18);animation:unfold 1.4s cubic-bezier(.2,.9,.3,1) both;transform-origin:top}
@keyframes unfold{from{transform:scaleY(.15);opacity:0}60%{opacity:1}}
.paper h2{font-family:Caveat;font-weight:700;font-size:2.4rem;color:var(--bb);text-align:center;margin-bottom:14px}
.paper p{font-family:Fraunces,Georgia,serif;font-weight:400;font-size:1.05rem;line-height:1.75;margin-bottom:1em;max-width:62ch}
.paper .deco{position:absolute;font-size:1.4rem;opacity:.8}
.fin h2{font-size:clamp(1.8rem,6vw,3rem);max-width:16ch;margin:auto}
.fin .hand{font-size:1.9rem;margin-top:14px;color:var(--bb)}
.cake{position:relative;width:min(280px,78vw);margin:46px auto 6px;display:flex;flex-direction:column;align-items:center;filter:drop-shadow(0 14px 22px rgba(0,76,63,.25))}
.candles{display:flex;gap:24px;margin-bottom:-3px;z-index:2}
.candle{position:relative;width:12px;height:40px;border-radius:5px;background:repeating-linear-gradient(135deg,#fff 0 6px,var(--bb) 6px 12px)}
.flame{position:absolute;left:50%;top:-24px;width:14px;height:24px;margin-left:-7px;border-radius:50% 50% 50% 50%/65% 65% 35% 35%;background:radial-gradient(circle at 50% 70%,#fff6c4,#ffc94a 55%,#ff8a3d);box-shadow:0 0 18px 6px rgba(255,200,80,.6);transform-origin:50% 100%;animation:flick .5s ease-in-out infinite alternate;transition:transform .5s,opacity .5s}
@keyframes flick{from{transform:rotate(-4deg) scale(1)}to{transform:rotate(4deg) scale(.9,1.12)}}
.candle.out .flame{animation:none;transform:scale(0);opacity:0}
.tier{border-radius:18px;border:1px solid var(--edge)}
.t1{width:64%;height:60px;background:linear-gradient(180deg,var(--pk) 0 24px,var(--cr) 24px);position:relative}
.t1::after{content:"🌸";position:absolute;left:50%;bottom:6px;transform:translateX(-50%);font-size:1.3rem}
.t2{width:92%;height:82px;margin-top:-6px;background:linear-gradient(180deg,var(--li) 0 28px,var(--cr) 28px);position:relative}
.t2::after{content:"🍀 ✿ 🍀 ✿ 🍀";position:absolute;left:0;right:0;bottom:10px;text-align:center;font-size:1.05rem;letter-spacing:4px}
.plate{width:112%;height:16px;margin-top:-4px;border-radius:50%;background:var(--glass);border:1px solid var(--edge)}
#fx{position:fixed;inset:0;pointer-events:none;z-index:40;overflow:hidden}
.f{position:absolute;bottom:-40px;animation:rise linear forwards}
@keyframes rise{to{transform:translateY(-110vh) rotate(var(--rot,200deg));opacity:0}}
.sp{position:fixed;width:8px;height:8px;border-radius:50%;pointer-events:none;z-index:45;animation:burst .9s ease-out forwards}
@keyframes burst{to{transform:translate(var(--dx),var(--dy)) scale(0);opacity:0}}
.bg-float{position:fixed;inset:0;z-index:1;pointer-events:none;overflow:hidden}
.bg-float span{position:absolute;animation:drift 9s ease-in-out infinite;opacity:.7}
@keyframes drift{50%{transform:translateY(-22px) rotate(14deg)}}
@media (prefers-reduced-motion:reduce){*{animation-duration:.01s!important;animation-iteration-count:1!important;transition-duration:.01s!important}}
</style>
</head>
<body>
<svg width="0" height="0" style="position:absolute"><defs>
<symbol id="clv" viewBox="-100 -100 200 200"><g fill="currentColor">
<path id="lf" d="M0 -6C-34 -44 -52 -84 -22 -90C-8 -92 0 -80 0 -68C0 -80 8 -92 22 -90C52 -84 34 -44 0 -6Z"/>
<use href="#lf" transform="rotate(90)"/><use href="#lf" transform="rotate(180)"/><use href="#lf" transform="rotate(270)"/></g>
<g fill="#FFF5E9" opacity=".35"><circle r="16"/></g><circle r="9" fill="#EC75AD"/></symbol></defs></svg>

<button class="sound glass" id="snd" aria-pressed="false">🔇 Music off</button>
<div class="bg-float" id="bgf" aria-hidden="true"></div>
<div id="fx" aria-hidden="true"></div>

<main>
<!-- 1 -->
<section class="stage hero on" id="s1">
  <div class="sticker glass" style="top:9%;left:6%;--r:-6deg">🎤 MC queen on duty</div>
  <div class="sticker glass" style="top:16%;right:6%;--r:5deg;animation-delay:-2s">★ Semester 7, still shining</div>
  <svg class="clover" viewBox="-100 -100 200 200" aria-hidden="true"><use href="#clv"/></svg>
  <h1 style="margin-top:14px">Hey, Birthday Girl! 🌷</h1>
  <p>A little garden, a little magic, and lots of love — all made just for you.</p>
  <div class="sub">Ready to unwrap your little surprises?</div>
  <button class="btn glass" data-go="s2">Let's Bloom! ✿</button>
</section>

<!-- 2 -->
<section class="stage" id="s2">
  <h2>The Wishing Ball Machine</h2>
  <p class="hand" style="font-size:1.5rem;margin-top:4px">turn the knob, catch a little wish ✿</p>
  <div class="machine">
    <div class="globe" id="globe"></div>
    <div class="drop" id="drop"></div>
    <div class="base"><div class="chute"></div><button class="knob" id="knob" aria-label="Putar mesin">🍀</button></div>
  </div>
  <div class="wish glass" id="wish" aria-live="polite"><span class="hint">Your first wish is waiting…</span></div>
  <button class="btn glass" id="spin">Spin Again! ✨</button>
  <button class="btn glass" id="toLetter" style="margin-top:12px;font-size:.95rem;padding:11px 26px;animation:none">One last surprise 💌</button>
</section>

<!-- 3 -->
<section class="stage" id="s3">
  <h2>A Special Letter for You 💌</h2>
  <p class="hand" style="font-size:1.6rem;margin-top:6px">One last little surprise, just for you...</p>
  <div class="env float" id="env" role="button" tabindex="0" aria-label="Buka surat">
    <div class="core"></div>
    <div class="petal"></div><div class="petal"></div><div class="petal"></div><div class="petal"></div>
    <div class="seal">🍀</div>
  </div>
  <button class="btn glass" id="open">Open Your Letter ♡</button>
</section>

<!-- 4 -->
<section class="stage" id="s4">
  <div class="letter-wrap glass">
    <article class="paper">
      <span class="deco" style="top:8px;left:10px">🌸</span><span class="deco" style="top:10px;right:12px">🍀</span>
      <span class="deco" style="bottom:8px;left:12px">🍀</span><span class="deco" style="bottom:10px;right:12px">🌷</span>
      <h2>Happy Level Up Day!!!</h2>
      <p>Haloo chincann. Apa kabarr? Semoga kabar kamu baik-baik aja ya🤗. Huaaa rinduuu sekaliii. Udah lama si kembar ini tidak berjumpa dengan chincan🥺. Hari ini kamu udah berusia 22 tahun yaaa🤗 ga kerasa waktu cepet banget berlalu dan kamu udah semester 7 aja nih.</p>
      <p>Happy birthday yaaa. Semoga di usia yang baru ini kamu bisa lebih happy lagi yaa. Kami harap banyak hal-hal baik yang menghampiri kamu. Kami juga selalu berdoa semoga semua cita-cita kamu bisa terwujud. Sehat selalu yaaa dan semoga kamu selalu berada dalam lindungan Tuhan. Sesibuk-sibuknya kegiatan kamu jangan lupa untuk selalu ambil waktu istirahat yaaa, supaya bisa tetep fit🥺.</p>
      <p>Senenggg banget bisa liat kamu berproses dan kami bangga banget bisa lihat pencapaian-pencapaian yang kamu raih🥺🥺🥺. Kami yakin kamu bakal jadi orang sukses di masa depan nanti. Semoga kita bisa sama-sama menjadi apa yang kita inginkan di masa depan nanti yaaa. Kita sama-sama berproses di jalan kita masing-masing. Semoga bisa ada waktu buat ketemuan lagi yaaa. Jujur kuangennnn pollll tapi sekarang kita juga masih sama-sama sibuk 🥺 semangattt iaaaaa.</p>
      <p>Maaaciii udah selalu baik sama kamii. Maaf buat semua kesalahan yang lalu-lalu yaaa. Thank you jugaa walaupun kita udah jarang komunikasi, tapi kamu masih inget sama kami dan selalu menyempatkan waktu buat ngucapin di hari-hari spesial kami. It means a lot for us🥺. Walaupun sekarang kita udah jarang ngobrol dan belum ada kesempatan buat ketemu lagi, semoga itu ga mengubah hubungan baik kita yaaa. We will always cherish all the memories we made together.</p>
      <p>Semoga suatu saat nanti kita bisa punya waktu buat ketemu lagi, cerita banyak hal yang udah kita lewatin selama ini, dan catch up sama kehidupan masing-masing. Pasti bakal banyak banget cerita yang perlu kita bagi🥺❤️.</p>
      <p>Once again, happy birthday chincannn!! Enjoy your special day yaaa. Sending lots of love from the twins!!🤍🤍🤍</p>
    </article>
  </div>
  <button class="btn glass" data-go="scake" style="margin-top:26px">Keep reading… ✿</button>
</section>

<!-- cake -->
<section class="stage" id="scake">
  <h2>Make a wish, chincan 🎂</h2>
  <p class="hand" id="cakeHint" style="font-size:1.5rem;margin-top:4px">pejamkan mata, lalu tiup lilinnya ✿</p>
  <div class="cake" id="cake">
    <div class="candles"><div class="candle"><i class="flame"></i></div><div class="candle"><i class="flame"></i></div><div class="candle"><i class="flame"></i></div><div class="candle"><i class="flame"></i></div></div>
    <div class="tier t1"></div><div class="tier t2"></div><div class="plate"></div>
  </div>
  <button class="btn glass" id="blow">Tiup lilinnya! 💨</button>
  <button class="btn glass" id="mic" style="margin-top:12px;font-size:.95rem;padding:11px 26px;animation:none">Tiup lewat mic 🎤</button>
  <button class="btn glass" id="next" data-go="s5" hidden>One more thing ✿</button>
</section>

<!-- 5 -->
<section class="stage fin" id="s5">
  <svg class="clover" viewBox="-100 -100 200 200" style="width:min(150px,40vw);color:var(--bb)" aria-hidden="true"><use href="#clv"/></svg>
  <h2 style="margin-top:20px">Keep blooming, keep shining, and never stop being YOU! 🍀</h2>
  <div class="hand">With lots of love, from your twins ♡</div>
  <button class="btn glass" id="again">Back to the garden 🌷</button>
</section>
</main>

<script>
const $=s=>document.querySelector(s);
const WISHES=["Born to shine, bestie. Never forget that! ✨","Your energy is literally contagious!","Keep being the smartest girl in the room!","The world needs more of your sunshine.","MC queen behavior, as always! 🎤","May your dreams always find their way to you.","Don't let your sparkle dim, okay?","Semoga semua hal baik selalu menemukan jalannya ke kamu!","Tetap jadi manusia seceria dan sehebat ini yaaa!","Semoga semua impian kamu satu per satu jadi nyata!","Your future is looking as bright as your smile!","Jangan lupa istirahat di tengah sibuknya dunia, chincan!","Keep growing, keep glowing, and keep being YOU!","Semoga makin banyak kesempatan keren yang datang ke hidup kamu!","You were made to do extraordinary things!","Mic check: one, two… you're unstoppable. 🎤","Every room gets brighter when you start talking.","Semester 7, tinggal sedikit lagi. Kamu pasti bisa! 🎓","Kata-katamu punya kekuatan. Pakai terus buat bersinar!","A four-leaf clover found you today. Lucky you, lucky us. 🍀","Be proud of how far you've come, chincan!","Semoga tahun ke-22 ini isinya senyum, tawa, dan kabar baik 🌷","Confidence looks so good on you.","Panggung apa pun yang kamu pilih, kamu pasti bersinar di sana!","Soft heart, big dreams, loud laugh. Never change.","Semoga langkahmu selalu ringan dan hatimu selalu hangat 🤍","The spotlight was literally made for you. ⭐","Istirahat itu bagian dari proses juga, ya. Take care!","Today the whole garden blooms for you. 🌸","Kami bangga banget sama kamu, chincan! 🥺"];
const COLS=["#F5A3C7","#C9EB69","#A9D1F0","#FFF5E9","#EC75AD"];
let last=-1,spinning=false,sound=false,ac;
function blip(f=660,d=.12){if(!sound)return;try{ac=ac||new(window.AudioContext||window.webkitAudioContext)();const o=ac.createOscillator(),g=ac.createGain();o.type="sine";o.frequency.value=f;g.gain.setValueAtTime(.08,ac.currentTime);g.gain.exponentialRampToValueAtTime(.001,ac.currentTime+d);o.connect(g);g.connect(ac.destination);o.start();o.stop(ac.currentTime+d)}catch(e){}}
let started=false,mTimer,master;
const N={C4:261.63,D4:293.66,E4:329.63,F4:349.23,G4:392,A4:440,B4:493.88,C5:523.25,D5:587.33,E5:659.25,F5:698.46,G5:783.99};
const MEL=[["G4",.75],["G4",.25],["A4",1],["G4",1],["C5",1],["B4",2],["G4",.75],["G4",.25],["A4",1],["G4",1],["D5",1],["C5",2],["G4",.75],["G4",.25],["G5",1],["E5",1],["C5",1],["B4",1],["A4",1],["F5",.75],["F5",.25],["E5",1],["C5",1],["D5",1],["C5",2]];
const BASS=[[130.81,0],[98,6],[130.81,12],[87.31,18]];
function note(f,t,d,type="triangle",v=.5){const o=ac.createOscillator(),g=ac.createGain();o.type=type;o.frequency.value=f;g.gain.setValueAtTime(0,t);g.gain.linearRampToValueAtTime(v,t+.02);g.gain.exponentialRampToValueAtTime(.001,t+d);o.connect(g);g.connect(master);o.start(t);o.stop(t+d+.05)}
function loop(){if(!sound||!master)return;const B=.62,t0=ac.currentTime+.1;let t=t0;MEL.forEach(([n,b])=>{note(N[n],t,b*B*1.8);note(N[n]*2,t,b*B,"sine",.14);t+=b*B});BASS.forEach(([f,s])=>note(f,t0+s*B,3.4,"sine",.3));mTimer=setTimeout(loop,(t-t0+3)*1000)}
function setSound(on){sound=on;const b=$("#snd");b.textContent=on?"🎵 Music on":"🔇 Music off";b.setAttribute("aria-pressed",on);clearTimeout(mTimer);if(master){master.disconnect();master=null}if(on){try{ac=ac||new(window.AudioContext||window.webkitAudioContext)();if(ac.state==="suspended")ac.resume();master=ac.createGain();master.gain.value=.09;master.connect(ac.destination);loop()}catch(e){}}}
$("#snd").onclick=()=>setSound(!sound);
function burst(x,y,n=16){for(let i=0;i<n;i++){const s=document.createElement("i");s.className="sp";const a=Math.random()*6.28,r=40+Math.random()*80;s.style.cssText=`left:${x}px;top:${y}px;--dx:${Math.cos(a)*r}px;--dy:${Math.sin(a)*r}px;background:${COLS[i%5]};box-shadow:0 0 8px ${COLS[i%5]}`;document.body.appendChild(s);setTimeout(()=>s.remove(),900)}}
function floaters(list,n=18){const fx=$("#fx");for(let i=0;i<n;i++){const s=document.createElement("span");s.className="f";s.textContent=list[i%list.length];const d=3+Math.random()*3;s.style.cssText=`left:${Math.random()*100}%;font-size:${16+Math.random()*22}px;animation-duration:${d}s;animation-delay:${Math.random()*1.2}s;--rot:${(Math.random()-.5)*500}deg`;fx.appendChild(s);setTimeout(()=>s.remove(),(d+1.5)*1000)}}
function go(id,e){const t=e?{x:e.clientX,y:e.clientY}:{x:innerWidth/2,y:innerHeight/2};burst(t.x,t.y,22);blip(740);document.querySelectorAll(".stage").forEach(s=>s.classList.toggle("on",s.id===id));scrollTo(0,0);if(id==="s2"){initBalls();if(!started){started=true;setSound(true)}}if(id==="s5")floaters(["🍀","🌸","✨","🌷"],24)}
document.querySelectorAll("[data-go]").forEach(b=>b.onclick=e=>go(b.dataset.go,e));
$("#toLetter").onclick=e=>go("s3",e);
/* ambient */
(()=>{const f=$("#bgf");["🍀","🌸","✨","🦋","🌷","⭐","🍀","✨","🌼"].forEach((c,i)=>{const s=document.createElement("span");s.textContent=c;s.style.cssText=`left:${(i*13+6)%95}%;top:${(i*29+8)%90}%;font-size:${18+(i%4)*8}px;animation-delay:${-i*1.3}s;animation-duration:${7+i%4*2}s`;f.appendChild(s)})})();
/* balls */
const globe=$("#globe");let balls=[],R=0,raf,kick=0;
function initBalls(){if(balls.length)return;R=globe.clientWidth/2;for(let i=0;i<14;i++){const el=document.createElement("div");el.className="ball";el.style.background=`radial-gradient(circle at 35% 30%,#fff,${COLS[i%5]} 60%)`;globe.appendChild(el);const a=Math.random()*6.28,r=Math.random()*(R-70);balls.push({x:R+Math.cos(a)*r*.5,y:R+R*.3+Math.random()*R*.4,vx:(Math.random()-.5)*3,vy:0,r:18,el})}cancelAnimationFrame(raf);tick()}
function tick(){R=globe.clientWidth/2;for(const b of balls){if(kick>0){b.vx+=(Math.random()-.5)*3.2;b.vy-=Math.random()*1.6}b.vy+=.32;b.x+=b.vx;b.y+=b.vy;const dx=b.x-R,dy=b.y-R,d=Math.hypot(dx,dy)||1;if(d>R-b.r){const nx=dx/d,ny=dy/d,dot=b.vx*nx+b.vy*ny;if(dot>0){b.vx-=1.75*dot*nx;b.vy-=1.75*dot*ny}b.x=R+nx*(R-b.r);b.y=R+ny*(R-b.r)}b.vx*=.995;b.vy*=.995;b.el.style.transform=`translate(${b.x-b.r}px,${b.y-b.r}px)`}
if(kick>0)kick--;raf=requestAnimationFrame(tick)}
/* spin */
function spin(e){if(spinning)return;spinning=true;const w=$("#wish");w.classList.remove("pop");w.innerHTML='<span class="hint">Shaking the garden…</span>';
$("#knob").classList.add("turn");globe.classList.add("shake");kick=90;blip(520,.3);setTimeout(()=>blip(620,.2),400);setTimeout(()=>blip(760,.2),800);
let i;do{i=Math.floor(Math.random()*WISHES.length)}while(i===last);last=i;
const c=COLS[Math.floor(Math.random()*5)],d=$("#drop");d.style.background=`radial-gradient(circle at 35% 30%,#fff,${c} 62%)`;
setTimeout(()=>{globe.classList.remove("shake");d.classList.remove("go");void d.offsetWidth;d.classList.add("go");blip(300,.25)},1500);
setTimeout(()=>{const r=d.getBoundingClientRect();burst(r.left+22,r.top+22,18);d.classList.remove("go");d.style.opacity=0;$("#knob").classList.remove("turn");
w.innerHTML=`<span style="font-size:1.6rem">🍀</span><span class="serif">${WISHES[i]}</span>`;void w.offsetWidth;w.classList.add("pop");blip(990,.25);spinning=false},2650)}
$("#spin").onclick=spin;$("#knob").onclick=spin;
/* envelope */
let blown=false;const HINT="pejamkan mata, lalu tiup lilinnya ✿";
function blow(){if(blown)return;blown=true;document.querySelectorAll(".candle").forEach((c,i)=>setTimeout(()=>c.classList.add("out"),i*200));blip(300,.3);setTimeout(()=>{const r=$("#cake").getBoundingClientRect();burst(r.left+r.width/2,r.top,40);floaters(["🎉","✨","🎂","🌸","🍀","💗"],30);$("#cakeHint").textContent="Semoga semua wish kamu jadi nyata, chincan! 🎉";$("#blow").hidden=true;$("#mic").hidden=true;$("#next").hidden=false;blip(880,.4);setTimeout(()=>blip(1100,.4),200)},1100)}
function resetCake(){blown=false;document.querySelectorAll(".candle").forEach(c=>c.classList.remove("out"));$("#cakeHint").textContent=HINT;$("#blow").hidden=false;$("#mic").hidden=false;$("#next").hidden=true}
async function micBlow(){const h=$("#cakeHint");try{const st=await navigator.mediaDevices.getUserMedia({audio:true});ac=ac||new(window.AudioContext||window.webkitAudioContext)();if(ac.state==="suspended")ac.resume();const src=ac.createMediaStreamSource(st),an=ac.createAnalyser();an.fftSize=512;src.connect(an);const buf=new Uint8Array(an.fftSize);h.textContent="tiup ke arah mic sekarang… 🌬️";let n=0;const chk=()=>{if(blown){st.getTracks().forEach(t=>t.stop());return}an.getByteTimeDomainData(buf);let s=0;for(const v of buf)s+=(v-128)*(v-128);n=Math.sqrt(s/buf.length)>22?n+1:0;if(n>6){st.getTracks().forEach(t=>t.stop());blow()}else requestAnimationFrame(chk)};chk()}catch(e){h.textContent="Mic tidak bisa diakses, tap tombol tiup aja ya 💨"}}
$("#blow").onclick=blow;$("#cake").onclick=blow;$("#mic").onclick=micBlow;
let opened=false;
function openEnv(e){if(opened)return;opened=true;const env=$("#env");env.classList.add("open");env.classList.remove("float");const r=env.getBoundingClientRect();burst(r.left+r.width/2,r.top+r.height/2,36);floaters(["🍀","✨","🍀","💗","🌸"],26);blip(660,.4);setTimeout(()=>blip(880,.4),300);$("#open").style.visibility="hidden";setTimeout(()=>go("s4"),2300)}
$("#open").onclick=openEnv;$("#env").onclick=openEnv;$("#env").onkeydown=e=>{if(e.key==="Enter"||e.key===" ")openEnv(e)};
$("#again").onclick=e=>{resetCake();opened=false;$("#env").classList.remove("open");$("#env").classList.add("float");$("#open").style.visibility="visible";go("s1",e)};
</script>
</body>
</html>
