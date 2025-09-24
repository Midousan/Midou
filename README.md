# Midou
<!doctype html>

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Who's Gonna Win the Million? — Placeholder UI</title>
  <style>
    :root{
      --bg:#0f1724; /* dark slate */
      --card:#0b1220;
      --text:#e6eef8;
      --muted:#98a0b3;
      --accent:#ff7a00; /* orange */
      --glass: rgba(255,255,255,0.03);
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      background:linear-gradient(180deg,#071025 0%, #0f1724 100%);
      font-family:Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      color:var(--text);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
    }.card{
  width:min(880px,92vw);
  background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.06));
  border-radius:16px;
  padding:28px;
  box-shadow:0 10px 30px rgba(2,6,23,0.6);
  border:1px solid rgba(255,255,255,0.03);
}

.header{
  display:flex;
  align-items:center;
  gap:16px;
  margin-bottom:12px;
}
.logo{
  width:56px;height:56px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#ffb27a);display:flex;align-items:center;justify-content:center;font-weight:700;color:#111;
  box-shadow:0 6px 20px rgba(255,122,0,0.12);
}
h1{font-size:20px;margin:0}
p.sub{margin:0;color:var(--muted);font-size:13px}

.question{
  margin:18px 0 22px 0;
  font-size:22px;
  letter-spacing:0.2px;
  line-height:1.2;
}

.options{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:14px;
}

.option{
  background:var(--glass);
  border-radius:12px;
  padding:16px 18px;
  cursor:pointer;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:12px;
  border:1px solid transparent;
  transition: transform .22s cubic-bezier(.2,.9,.2,1), box-shadow .22s ease, border-color .18s ease, background .18s ease;
  user-select:none;
  position:relative;
  overflow:hidden;
}

/* Hover: rise slightly (hoovered up) */
.option:hover{
  transform: translateY(-8px) scale(1.01);
  box-shadow:0 18px 40px rgba(8,12,24,0.6);
  background: linear-gradient(180deg, rgba(255,255,255,0.018), rgba(0,0,0,0.05));
}

.option .left{
  display:flex;align-items:center;gap:12px;
}
.badge{
  width:44px;height:44px;border-radius:8px;background:rgba(255,255,255,0.03);display:flex;align-items:center;justify-content:center;font-weight:700;color:var(--text);font-size:16px;border:1px solid rgba(255,255,255,0.02);
}
.option .text{font-size:16px;color:var(--text)}
.option .sub{font-size:13px;color:var(--muted)}

/* Selected state: orange outline on the outside */
.option.selected{
  outline: 4px solid rgba(255,122,0,0.16);
  box-shadow: 0 18px 50px rgba(255,122,0,0.08), inset 0 0 0 1px rgba(255,122,0,0.06);
  border-color: rgba(255,122,0,0.18);
}

/* Strong visible outer ring (accent) */
.option.selected::after{
  content:"";position:absolute;inset:-6px;border-radius:16px;box-shadow:0 0 0 3px rgba(255,122,0,0.12);pointer-events:none;}

/* small radio on right */
.select-dot{
  width:18px;height:18px;border-radius:50%;border:2px solid rgba(255,255,255,0.06);display:flex;align-items:center;justify-content:center;flex-shrink:0;background:transparent;transition:all .18s ease;
}
.select-dot.active{background:var(--accent);border-color:var(--accent);width:20px;height:20px}

/* responsive */
@media (max-width:520px){
  .options{grid-template-columns:1fr}
  .question{font-size:18px}
}

/* subtle floating animation for decorative elements */
.floaty{animation: floaty 6s ease-in-out infinite}
@keyframes floaty{0%{transform:translateY(0)}50%{transform:translateY(-6px)}100%{transform:translateY(0)}}

.hint{margin-top:14px;color:var(--muted);font-size:13px}

  </style>
</head>
<body>
  <div class="card" role="application" aria-label="Quiz placeholder">
    <div class="header">
      <div class="logo floaty">M</div>
      <div>
        <h1>Who's Gonna Win the Million?</h1>
        <p class="sub">Question placeholder — click an answer to select (hover to lift)</p>
      </div>
    </div><div class="question">🔸 <strong>Question:</strong> Which of these discoveries most directly advanced ancient mathematical understanding?</div>

<div class="options" role="list">
  <div class="option" role="listitem" tabindex="0" data-value="A" aria-pressed="false">
    <div class="left">
      <div class="badge">A</div>
      <div>
        <div class="text">The invention of the abacus</div>
        <div class="sub">Early computational tool</div>
      </div>
    </div>
    <div class="select-dot" aria-hidden="true"></div>
  </div>

  <div class="option" role="listitem" tabindex="0" data-value="B" aria-pressed="false">
    <div class="left">
      <div class="badge">B</div>
      <div>
        <div class="text">Geometry in Greek mathematics</div>
        <div class="sub">Euclid & Pythagoras</div>
      </div>
    </div>
    <div class="select-dot" aria-hidden="true"></div>
  </div>

  <div class="option" role="listitem" tabindex="0" data-value="C" aria-pressed="false">
    <div class="left">
      <div class="badge">C</div>
      <div>
        <div class="text">Positional numeral systems</div>
        <div class="sub">Place-value arithmetic</div>
      </div>
    </div>
    <div class="select-dot" aria-hidden="true"></div>
  </div>

  <div class="option" role="listitem" tabindex="0" data-value="D" aria-pressed="false">
    <div class="left">
      <div class="badge">D</div>
      <div>
        <div class="text">Astronomical observations</div>
        <div class="sub">Calendars & cycles</div>
      </div>
    </div>
    <div class="select-dot" aria-hidden="true"></div>
  </div>
</div>

<div class="hint">Tip: Use <kbd>↑</kbd>/<kbd>↓</kbd> to navigate and <kbd>Enter</kbd> to select. Selected option gets an orange outer ring.</div>

  </div>  <script>
    (function(){
      const options = Array.from(document.querySelectorAll('.option'));
      let focusedIndex = 0;

      function selectOption(idx){
        options.forEach((el,i)=>{
          const dot = el.querySelector('.select-dot');
          if(i===idx){
            el.classList.add('selected');
            el.setAttribute('aria-pressed','true');
            dot.classList.add('active');
          } else {
            el.classList.remove('selected');
            el.setAttribute('aria-pressed','false');
            dot.classList.remove('active');
          }
        });
      }

      // click & focus handlers
      options.forEach((opt, idx)=>{
        opt.addEventListener('click', ()=>{ focusedIndex = idx; selectOption(idx); });
        opt.addEventListener('keydown', (e)=>{
          if(e.key==='Enter' || e.key===' '){ e.preventDefault(); focusedIndex = idx; selectOption(idx); }
        });

        opt.addEventListener('focus', ()=>{ focusedIndex = idx; });
      });

      // keyboard navigation
      window.addEventListener('keydown', (e)=>{
        if(e.key==='ArrowDown' || e.key==='ArrowRight'){
          e.preventDefault(); focusedIndex = (focusedIndex+1) % options.length; options[focusedIndex].focus();
        } else if(e.key==='ArrowUp' || e.key==='ArrowLeft'){
          e.preventDefault(); focusedIndex = (focusedIndex-1 + options.length) % options.length; options[focusedIndex].focus();
        } else if(e.key==='Enter'){
          // select current
          selectOption(focusedIndex);
        }
      });

      // initial focus
      options[0].focus();

    })();
  </script></body>
</html>
