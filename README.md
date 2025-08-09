<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>ClariSubs — Family-first subscription management</title>
  <meta name="description" content="ClariSubs helps families track, split and cancel subscriptions — together. Save money, protect your family budget." />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#f5f9ff;
      --card:#ffffff;
      --text:#0f1724;
      --muted:#6b7280;
      --primary:#0b6eff; /* blue */
      --accent:#14b8a6;  /* teal/green */
      --glass: rgba(255,255,255,0.6);
      --maxw:1100px;
      --radius:14px;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family:Inter,system-ui,Arial,"Noto Sans",sans-serif;
      background:linear-gradient(180deg,var(--bg),#ffffff);
      color:var(--text);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }
    .wrap{max-width:var(--maxw);margin:28px auto;padding:20px}
    header{display:flex;justify-content:space-between;align-items:center;gap:16px}
    .logo{display:flex;align-items:center;gap:12px}
    .logo .mark{width:44px;height:44px;border-radius:9px;background:linear-gradient(135deg,var(--primary),var(--accent));display:flex;align-items:center;justify-content:center;color:white;font-weight:700}
    .nav{display:flex;gap:12px;align-items:center}
    .btn{background:var(--primary);color:white;padding:10px 14px;border-radius:10px;border:0;cursor:pointer;font-weight:600}
    .btn.secondary{background:transparent;color:var(--primary);border:1px solid rgba(11,110,255,0.12)}
    /* Hero */
    .hero{display:flex;flex-direction:column-reverse;gap:20px;margin-top:18px}
    .hero-inner{display:flex;flex-direction:column;gap:18px;flex:1}
    h1{font-size:28px;margin:0;line-height:1.05}
    p.lead{margin:0;color:var(--muted)}
    .hero-cta{display:flex;gap:12px;flex-wrap:wrap}
    .visual{display:flex;justify-content:center;align-items:center;background:linear-gradient(180deg, rgba(11,110,255,0.06), rgba(20,184,166,0.03));border-radius:16px;padding:18px}
    .visual svg{max-width:340px;width:100%;height:auto}
    /* features */
    .cards{display:grid;grid-template-columns:1fr;gap:12px;margin-top:20px}
    .card{background:var(--card);padding:16px;border-radius:12px;box-shadow:0 6px 18px rgba(8,15,35,0.04);display:flex;gap:12px;align-items:flex-start}
    .icon{width:48px;height:48px;border-radius:10px;background:linear-gradient(135deg,var(--primary),var(--accent));display:flex;align-items:center;justify-content:center;color:white;font-weight:700}
    .card h4{margin:0;font-size:16px}
    .muted{color:var(--muted);font-size:14px}
    /* grid for features on larger screens */
    @media(min-width:800px){
      .hero{flex-direction:row;align-items:center}
      h1{font-size:40px}
      .cards{grid-template-columns:repeat(3,1fr)}
    }
    /* calculator */
    .calc{background:linear-gradient(180deg,#fff, #f7fffe);padding:16px;border-radius:12px}
    .calc input[type=range]{width:100%}
    .metrics{display:flex;gap:12px;flex-wrap:wrap;margin-top:12px}
    .metric{flex:1;min-width:140px;background:var(--card);padding:12px;border-radius:10px;text-align:center}
    .metric .num{font-size:20px;font-weight:700}
    /* comparison */
    .compare{margin-top:18px;background:linear-gradient(180deg,#fff,#f7fafc);padding:12px;border-radius:12px}
    .compare table{width:100%;border-collapse:collapse}
    .compare th{ text-align:left;padding:10px 8px;font-weight:600}
    .compare td{padding:10px 8px;border-top:1px solid rgba(11,110,255,0.06)}
    .tick{color:var(--accent);font-weight:700}
    /* testimonials */
    .testimonials{display:grid;grid-template-columns:1fr;gap:12px;margin-top:18px}
    .testi{background:var(--card);padding:14px;border-radius:12px;box-shadow:0 6px 16px rgba(8,15,35,0.03)}
    @media(min-width:900px){ .testimonials{grid-template-columns:repeat(3,1fr)} }
    footer{margin-top:30px;padding:20px 12px;color:var(--muted);font-size:14px;text-align:center}
    /* small helpers */
    .small{font-size:13px;color:var(--muted)}
    .pill{display:inline-block;padding:6px 10px;border-radius:999px;background:rgba(20,184,166,0.08);color:var(--accent);font-weight:600}
    form input, form button{font-family:inherit}
    .form-row{display:flex;gap:8px;flex-wrap:wrap}
    .form-row input[type="email"]{flex:1;padding:12px;border-radius:10px;border:1px solid rgba(12,35,63,0.06)}
    .success{background:linear-gradient(90deg,#ecfdf5,#ffffff);padding:12px;border-radius:10px;color:var(--accent);display:none}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="logo">
        <div class="mark">CS</div>
        <div>
          <div style="font-weight:700">ClariSubs</div>
          <div class="small">Family-first subscription control</div>
        </div>
      </div>
      <nav class="nav">
        <a class="small" href="#features">Features</a>
        <a class="small" href="#compare">Why Family</a>
        <button class="btn" onclick="scrollToForm()">Get early access</button>
      </nav>
    </header>

    <section class="hero" id="top">
      <div class="hero-inner">
        <div>
          <h1>ClariSubs — manage your family's subscriptions. Save together.</h1>
          <p class="lead">All family subscriptions in one dashboard. Split bills, cancel unused plans, and stop surprising charges — built specifically for households.</p>
        </div>

        <div class="hero-cta">
          <button class="btn" onclick="scrollToForm()">Start free</button>
          <button class="btn secondary" onclick="document.getElementById('demo').scrollIntoView({behavior:'smooth'})">See demo calculator</button>
        </div>

        <div style="margin-top:10px">
          <form name="signup" method="POST" data-netlify="true" netlify-honeypot="bot-field" id="signupForm">
            <input type="hidden" name="form-name" value="signup">
            <div class="form-row">
              <input type="email" name="email" placeholder="Your email — get early access" required>
              <button class="btn" type="submit">Join waitlist</button>
            </div>
            <div class="small" style="margin-top:8px">No spam. We launch closed beta for families soon.</div>
            <div class="success" id="successMsg">Thanks — you're on the waitlist. We'll email you next steps.</div>
          </form>
        </div>
      </div>

      <div class="visual" aria-hidden="true">
        <!-- simple family SVG illustration -->
        <svg viewBox="0 0 600 400" xmlns="http://www.w3.org/2000/svg">
          <defs><linearGradient id="g" x1="0" x2="1"><stop offset="0" stop-color="#0b6eff"/><stop offset="1" stop-color="#14b8a6"/></linearGradient></defs>
          <rect x="0" y="0" width="600" height="400" rx="16" fill="url(#g)" opacity="0.07"/>
          <g transform="translate(90,40)">
            <circle cx="110" cy="90" r="46" fill="#fff"/>
            <circle cx="160" cy="70" r="36" fill="#fff"/>
            <rect x="50" y="150" width="220" height="110" rx="16" fill="#fff" opacity="0.98"/>
            <text x="100" y="210" font-family="Inter" font-size="22" fill="#0b6eff" font-weight="700">Family Dashboard</text>
            <text x="60" y="240" font-family="Inter" font-size="14" fill="#667085">Shared subscriptions, one view</text>
          </g>
        </svg>
      </div>
    </section>

    <!-- Features -->
    <section id="features" style="margin-top:24px">
      <div style="display:flex;justify-content:space-between;align-items:center">
        <h2 style="margin:0">What ClariSubs does for families</h2>
        <div class="pill">Family-first MVP</div>
      </div>

      <div class="cards" style="margin-top:12px">
        <div class="card">
          <div class="icon">F</div>
          <div>
            <h4>Shared Family Dashboard</h4>
            <div class="muted">See every subscription across family members in one clean view.</div>
          </div>
        </div>

        <div class="card">
          <div class="icon">S</div>
          <div>
            <h4>Split & assign bills</h4>
            <div class="muted">Automatically split recurring costs and charge family wallets or cards.</div>
          </div>
        </div>

        <div class="card">
          <div class="icon">C</div>
          <div>
            <h4>One-click cancel & pause</h4>
            <div class="muted">Cancel unused plans or pause subscriptions without hunting through sites.</div>
          </div>
        </div>

        <div class="card">
          <div class="icon">P</div>
          <div>
            <h4>Parental controls</h4>
            <div class="muted">Approve kids’ new subscriptions, set spending limits for sub-accounts.</div>
          </div>
        </div>

        <div class="card">
          <div class="icon">A</div>
          <div>
            <h4>Shared savings plans</h4>
            <div class="muted">Plan collective cancellations to maximize family savings.</div>
          </div>
        </div>

        <div class="card">
          <div class="icon">🔒</div>
          <div>
            <h4>Bank-level security</h4>
            <div class="muted">Encrypted connections, secure tokens, and privacy-first defaults.</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Calculator demo -->
    <section id="demo" style="margin-top:22px">
      <div style="display:flex;justify-content:space-between;align-items:center">
        <h2 style="margin:0">Estimate family spending & potential savings</h2>
        <div class="small">Quick demo — tweak numbers to see impact</div>
      </div>

      <div style="margin-top:12px" class="calc">
        <label class="small">Family members: <span id="membersLabel">4</span></label>
        <input id="members" type="range" min="1" max="8" value="4" oninput="updateCalc()">

        <label class="small" style="margin-top:8px">Avg subscriptions per person: <span id="subsLabel">3</span></label>
        <input id="subs" type="range" min="0" max="10" value="3" oninput="updateCalc()">

        <label class="small" style="margin-top:8px">Avg monthly cost per subscription ($): <span id="costLabel">12</span></label>
        <input id="cost" type="range" min="1" max="50" value="12" oninput="updateCalc()">

        <div class="metrics">
          <div class="metric">
            <div class="small">Total monthly spend</div>
            <div class="num" id="totalSpend">$0</div>
          </div>
          <div class="metric">
            <div class="small">Estimated savings*</div>
            <div class="num" id="savings">$0</div>
          </div>
          <div class="metric">
            <div class="small">Per person monthly</div>
            <div class="num" id="perPerson">$0</div>
          </div>
        </div>
        <div class="small" style="margin-top:8px">*Savings estimate based on average cancellation & optimization — real results vary.</div>
      </div>
    </section>

    <!-- Compare -->
    <section id="compare" style="margin-top:20px">
      <h2 style="margin-bottom:8px">Why ClariSubs for families — short comparison</h2>
      <div class="compare">
        <table>
          <thead>
            <tr>
              <th>Feature</th><th>ClariSubs (Family)</th><th>Standard subscription apps</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Family dashboard</td><td class="tick">Yes</td><td>No / Individual</td>
            </tr>
            <tr>
              <td>Split payments</td><td class="tick">Yes</td><td>Partial or none</td>
            </tr>
            <tr>
              <td>Parental controls</td><td class="tick">Yes</td><td>No</td>
            </tr>
            <tr>
              <td>Shared savings plans</td><td class="tick">Yes</td><td>No</td>
            </tr>
            <tr>
              <td>Fast setup (family)</td><td class="tick">1–2 minutes</td><td>Usually per-person</td>
            </tr>
          </tbody>
        </table>
      </div>
    </section>

    <!-- Testimonials -->
    <section style="margin-top:20px">
      <h2>Families testing the beta</h2>
      <div class="testimonials">
        <div class="testi">
          <div style="font-weight:700">Sarah, Mom of 3</div>
          <div class="small">"We found 2 duplicate subscriptions and saved $36/month. Setting spending limits for my teens changed everything."</div>
        </div>
        <div class="testi">
          <div style="font-weight:700">James & Ana</div>
          <div class="small">"One dashboard for both of us — no more surprise charges. The split feature is simple and fair."</div>
        </div>
        <div class="testi">
          <div style="font-weight:700">Beta Family</div>
          <div class="small">"Easy to use on phones. We signed up the whole household in minutes."</div>
        </div>
      </div>
    </section>

    <footer>
      <div style="display:flex;gap:12px;flex-wrap:wrap;justify-content:center;align-items:center">
        <div class="small">© ClariSubs — Built for families</div>
        <div class="small">Privacy • Security • Terms</div>
      </div>
    </footer>
  </div>

  <script>
    // Simple calculator logic + animation
    const members = document.getElementById('members');
    const subs = document.getElementById('subs');
    const cost = document.getElementById('cost');
    const membersLabel = document.getElementById('membersLabel');
    const subsLabel = document.getElementById('subsLabel');
    const costLabel = document.getElementById('costLabel');
    const totalSpendEl = document.getElementById('totalSpend');
    const savingsEl = document.getElementById('savings');
    const perPersonEl = document.getElementById('perPerson');

    function format(n){ return '$' + Math.round(n).toLocaleString(); }

    function updateCalc(){
      membersLabel.textContent = members.value;
      subsLabel.textContent = subs.value;
      costLabel.textContent = cost.value;
      const total = members.value * subs.value * cost.value;
      // estimated savings: conservative 18% by default (demo)
      const savings = total * 0.18;
      const perPerson = total / Math.max(1,members.value);
      animateNumber(totalSpendEl, total);
      animateNumber(savingsEl, savings);
      animateNumber(perPersonEl, perPerson);
    }

    function animateNumber(el, to){
      const start = parseInt(el.getAttribute('data-val')) || 0;
      const duration = 600;
      const startTime = performance.now();
      function step(t){
        const p = Math.min(1,(t - startTime) / duration);
        const value = Math.round(start + (to - start) * easeOutCubic(p));
        el.textContent = format(value);
        el.setAttribute('data-val', value);
        if(p < 1) requestAnimationFrame(step);
      }
      requestAnimationFrame(step);
    }
    function easeOutCubic(t){ return 1 - Math.pow(1 - t, 3); }

    // initial
    updateCalc();

    // Form handling (Netlify will do server-side but show UI feedback)
    const form = document.getElementById('signupForm');
    const successMsg = document.getElementById('successMsg');
    form.addEventListener('submit', function(e){
      // Let Netlify handle POST — show success UI
      setTimeout(()=>{ successMsg.style.display = 'block'; form.querySelector('input[type="email"]').value=''; }, 600);
    });

    function scrollToForm(){ document.getElementById('signupForm').scrollIntoView({behavior:'smooth'}); }
  </script>
</body>
</html>
