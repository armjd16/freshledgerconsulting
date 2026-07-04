<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fresh Ledger Consulting — Debt Negotiation for Filipino Families</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500;600&display=swap');

  :root{
    --ink:#1B2A41;
    --ink-soft:#2E4058;
    --paper:#EEF1EE;
    --paper-line:#D8DED9;
    --brass:#A9814B;
    --brass-dark:#8A6B3D;
    --forest:#204F3B;
    --forest-soft:#e4ece7;
    --rule-red:#A5423A;
    --charcoal:#22262B;
    --white:#FBFBF9;
    --max:1080px;
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--paper);
    color:var(--charcoal);
    font-family:'IBM Plex Sans', sans-serif;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3{
    font-family:'Fraunces', serif;
    color:var(--ink);
    margin:0 0 0.4em 0;
    letter-spacing:-0.01em;
  }
  .mono{font-family:'IBM Plex Mono', monospace;}
  a{color:inherit;}
  :focus-visible{outline:3px solid var(--brass); outline-offset:3px;}

  .wrap{max-width:var(--max); margin:0 auto; padding:0 28px;}

  /* ---------- NAV ---------- */
  header.site{
    position:sticky; top:0; z-index:50;
    background:rgba(238,241,238,0.92);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--paper-line);
  }
  nav{
    display:flex; align-items:center; justify-content:space-between;
    padding:16px 28px; max-width:var(--max); margin:0 auto;
  }
  .brand{
    display:flex; align-items:baseline; gap:8px;
    font-family:'Fraunces', serif; font-weight:600; font-size:1.15rem; color:var(--ink);
    text-decoration:none;
  }
  .brand .mark{color:var(--brass-dark); font-family:'IBM Plex Mono', monospace; font-size:1rem;}
  nav .links{display:flex; gap:28px; font-size:0.92rem;}
  nav .links a{text-decoration:none; color:var(--ink-soft); font-weight:500;}
  nav .links a:hover{color:var(--brass-dark);}
  .cta-btn{
    background:var(--ink); color:var(--white); padding:10px 18px;
    border-radius:3px; text-decoration:none; font-weight:600; font-size:0.9rem;
    border:1px solid var(--ink);
    transition:background 0.15s ease, color 0.15s ease;
    white-space:nowrap;
  }
  .cta-btn:hover{background:var(--brass-dark); border-color:var(--brass-dark);}
  .cta-btn.outline{background:transparent; color:var(--ink);}
  .cta-btn.outline:hover{background:var(--ink); color:var(--white);}

  @media (max-width:720px){
    nav .links{display:none;}
  }

  /* ---------- HERO ---------- */
  .hero{
    padding:64px 0 40px;
  }
  .hero-grid{
    display:grid; grid-template-columns:1.1fr 0.9fr; gap:48px; align-items:center;
  }
  @media (max-width:900px){ .hero-grid{grid-template-columns:1fr;} }

  .eyebrow{
    font-family:'IBM Plex Mono', monospace; font-size:0.78rem; letter-spacing:0.08em;
    text-transform:uppercase; color:var(--forest); font-weight:600;
    display:flex; align-items:center; gap:8px; margin-bottom:18px;
  }
  .eyebrow::before{content:''; width:22px; height:1px; background:var(--forest);}

  .hero h1{
    font-size:clamp(2.1rem, 4vw, 3.1rem);
    font-weight:600;
    line-height:1.08;
  }
  .hero h1 em{font-style:italic; color:var(--forest); font-weight:500;}
  .hero p.lead{
    font-size:1.08rem; color:var(--ink-soft); max-width:46ch; margin:18px 0 28px;
  }
  .hero .actions{display:flex; gap:14px; flex-wrap:wrap;}

  /* ---------- LEDGER CARD (signature element) ---------- */
  .ledger-card{
    background:var(--white);
    border:1px solid var(--paper-line);
    border-radius:6px;
    box-shadow:0 24px 48px -20px rgba(27,42,65,0.25);
    position:relative;
    overflow:hidden;
    padding:28px 24px 24px 44px;
  }
  .ledger-card::before{
    content:'';
    position:absolute; left:26px; top:0; bottom:0;
    width:1px; background:var(--rule-red); opacity:0.55;
  }
  .ledger-card .ledger-head{
    display:flex; justify-content:space-between; align-items:baseline;
    font-family:'IBM Plex Mono', monospace; font-size:0.72rem; letter-spacing:0.05em;
    color:var(--ink-soft); text-transform:uppercase; margin-bottom:14px;
    padding-bottom:10px; border-bottom:1px dashed var(--paper-line);
  }
  .ledger-row{
    display:grid; grid-template-columns:1fr auto; gap:8px;
    padding:11px 0; border-bottom:1px dotted var(--paper-line);
    font-family:'IBM Plex Mono', monospace; font-size:0.86rem;
    color:var(--ink);
  }
  .ledger-row .label{color:var(--ink-soft); font-family:'IBM Plex Sans', sans-serif; font-size:0.88rem;}
  .ledger-row .amt{font-weight:500;}
  .ledger-row.before .amt{color:var(--rule-red);}
  .ledger-row.after .amt{color:var(--forest);}

  .stamp{
    margin-top:18px;
    display:inline-flex; align-items:center; gap:10px;
    border:2px solid var(--brass-dark); color:var(--brass-dark);
    padding:8px 16px; border-radius:4px;
    font-family:'IBM Plex Mono', monospace; font-weight:600; font-size:0.82rem;
    letter-spacing:0.08em; text-transform:uppercase;
    transform:rotate(-2.5deg);
    opacity:0;
    animation:stampIn 0.5s ease-out 0.4s forwards;
  }
  @keyframes stampIn{
    0%{opacity:0; transform:rotate(-2.5deg) scale(1.4);}
    70%{opacity:1;}
    100%{opacity:1; transform:rotate(-2.5deg) scale(1);}
  }
  @media (prefers-reduced-motion:reduce){
    .stamp{animation:none; opacity:1;}
  }
  .ledger-foot{
    margin-top:16px; font-size:0.78rem; color:var(--ink-soft); font-style:italic;
  }

  /* ---------- SECTIONS ---------- */
  section{padding:76px 0;}
  .section-head{max-width:640px; margin-bottom:44px;}
  .section-head .eyebrow{margin-bottom:14px;}
  .section-head h2{font-size:clamp(1.6rem, 3vw, 2.2rem);}
  .section-head p{color:var(--ink-soft); font-size:1.02rem;}

  .band-forest{background:var(--forest); color:var(--white);}
  .band-forest h2, .band-forest .eyebrow{color:var(--white);}
  .band-forest .eyebrow::before{background:var(--white);}
  .band-forest p{color:#D6E4DB;}

  /* services */
  .services-grid{
    display:grid; grid-template-columns:repeat(2, 1fr); gap:1px;
    background:var(--paper-line); border:1px solid var(--paper-line);
    border-radius:8px; overflow:hidden;
  }
  @media (max-width:720px){.services-grid{grid-template-columns:1fr;}}
  .service{background:var(--white); padding:30px 28px;}
  .service .num{font-family:'IBM Plex Mono', monospace; color:var(--brass-dark); font-size:0.8rem; font-weight:600;}
  .service h3{font-size:1.15rem; margin:10px 0 8px;}
  .service p{color:var(--ink-soft); font-size:0.94rem; margin:0;}

  /* process */
  .process{
    display:grid; grid-template-columns:repeat(4,1fr); gap:0;
    border-top:1px solid rgba(255,255,255,0.18);
  }
  @media (max-width:900px){.process{grid-template-columns:1fr; }}
  .step{
    padding:26px 22px; border-right:1px solid var(--paper-line); border-bottom:1px solid var(--paper-line);
  }
  .process .step:last-child{border-right:none;}
  @media (max-width:900px){ .step{border-right:none;} }
  .step{border-right-color:rgba(255,255,255,0.18); border-bottom-color:rgba(255,255,255,0.18);}
  .step .step-no{
    font-family:'IBM Plex Mono', monospace; color:var(--brass); font-weight:600; font-size:0.85rem;
    display:block; margin-bottom:10px;
  }
  .step h3{font-size:1.02rem; margin-bottom:6px; color:var(--white);}
  .step p{color:#D6E4DB; font-size:0.9rem; margin:0;}

  /* about / credibility */
  .about-grid{display:grid; grid-template-columns:1fr 1fr; gap:48px; align-items:start;}
  @media (max-width:820px){.about-grid{grid-template-columns:1fr;}}
  .stat-row{display:flex; gap:36px; margin-top:26px; flex-wrap:wrap;}
  .stat{}
  .stat .n{font-family:'Fraunces', serif; font-size:2rem; font-weight:600; color:var(--forest);}
  .stat .l{font-size:0.82rem; color:var(--ink-soft); text-transform:uppercase; letter-spacing:0.04em;}

  .principles{list-style:none; padding:0; margin:0; display:flex; flex-direction:column; gap:16px;}
  .principles li{
    display:flex; gap:14px; align-items:flex-start; font-size:0.96rem; color:var(--ink-soft);
    padding-bottom:16px; border-bottom:1px solid var(--paper-line);
  }
  .principles li:last-child{border-bottom:none;}
  .principles .tick{
    flex:0 0 auto; width:22px; height:22px; border-radius:50%; border:1.5px solid var(--brass-dark);
    display:flex; align-items:center; justify-content:center; color:var(--brass-dark); font-size:0.72rem;
    margin-top:2px; font-family:'IBM Plex Mono', monospace;
  }

  /* disclaimer */
  .disclaimer{
    background:var(--white); border:1px solid var(--paper-line); border-left:4px solid var(--brass-dark);
    border-radius:6px; padding:22px 24px; font-size:0.86rem; color:var(--ink-soft);
  }
  .disclaimer strong{color:var(--ink);}

  /* contact */
  .contact-panel{
    background:var(--ink); color:var(--white); border-radius:10px;
    padding:48px; display:grid; grid-template-columns:1.1fr 0.9fr; gap:40px;
  }
  @media (max-width:820px){.contact-panel{grid-template-columns:1fr; padding:34px 24px;}}
  .contact-panel h2{color:var(--white);}
  .contact-panel p{color:#C7D0DB;}
  .contact-list{list-style:none; padding:0; margin:24px 0 0; display:flex; flex-direction:column; gap:16px;}
  .contact-list a{
    display:flex; align-items:center; gap:12px; text-decoration:none; color:var(--white);
    font-weight:500; font-size:1.02rem;
    padding:14px 16px; border:1px solid rgba(255,255,255,0.18); border-radius:6px;
    transition:border-color 0.15s ease, background 0.15s ease;
  }
  .contact-list a:hover{border-color:var(--brass); background:rgba(255,255,255,0.06);}
  .contact-list .ic{
    font-family:'IBM Plex Mono', monospace; font-size:0.75rem; color:var(--brass);
    width:20px;
  }
  .contact-note{font-size:0.8rem; color:#9FB0C2; margin-top:20px;}

  .service-area{
    background:rgba(255,255,255,0.06); border-radius:8px; padding:22px;
    font-size:0.9rem;
  }
  .service-area .eyebrow{color:var(--brass); }
  .service-area .eyebrow::before{background:var(--brass);}

  footer{
    padding:32px 0; text-align:center; font-size:0.82rem; color:var(--ink-soft);
    border-top:1px solid var(--paper-line);
  }
</style>
</head>
<body>

<header class="site">
  <nav>
    <a href="#top" class="brand"><span class="mark">FL</span> Fresh Ledger Consulting</a>
    <div class="links">
      <a href="#services">Services</a>
      <a href="#process">Process</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </div>
    <a href="#contact" class="cta-btn">Book a Consultation</a>
  </nav>
</header>

<main id="top">

  <!-- HERO -->
  <section class="hero">
    <div class="wrap hero-grid">
      <div>
        <div class="eyebrow">Debt Negotiation Consulting · Philippines</div>
        <h1>Twelve years inside collections, <em>now working for you.</em></h1>
        <p class="lead">Fresh Ledger Consulting helps individuals in the Philippines understand their debt, talk to creditors with confidence, and negotiate terms they can actually keep — from someone who has sat on the other side of that call.</p>
        <div class="actions">
          <a href="#contact" class="cta-btn">Book a Free Initial Call</a>
          <a href="#services" class="cta-btn outline">See how it works</a>
        </div>
      </div>

      <div class="ledger-card">
        <div class="ledger-head">
          <span>Case File · Sample</span>
          <span>Status</span>
        </div>
        <div class="ledger-row before">
          <span class="label">Outstanding balance, 3 accounts</span>
          <span class="amt">₱ 248,000</span>
        </div>
        <div class="ledger-row">
          <span class="label">Monthly demand before negotiation</span>
          <span class="amt">₱ 21,500</span>
        </div>
        <div class="ledger-row after">
          <span class="label">Restructured monthly commitment</span>
          <span class="amt">₱ 6,800</span>
        </div>
        <div class="stamp">✓ Terms Restructured</div>
        <p class="ledger-foot">Illustrative example. Every case and creditor response is different — see disclosure below.</p>
      </div>
    </div>
  </section>

  <!-- SERVICES -->
  <section id="services">
    <div class="wrap">
      <div class="section-head">
        <div class="eyebrow">What I help with</div>
        <h2>Practical support at the exact point debt gets overwhelming</h2>
        <p>Each service draws directly on years of handling accounts from the collector's side — I know how the calls are scripted, what banks will actually agree to, and where the room to negotiate really is.</p>
      </div>

      <div class="services-grid">
        <div class="service">
          <span class="num">01</span>
          <h3>Debt Assessment &amp; Strategy</h3>
          <p>A clear-eyed review of every account, lender, and notice you've received, sorted by urgency, with a realistic plan for what to tackle first.</p>
        </div>
        <div class="service">
          <span class="num">02</span>
          <h3>Creditor Negotiation Support</h3>
          <p>Guidance on settlement offers, restructured payment terms, and how to respond to collection calls or demand letters without agreeing to something you can't sustain.</p>
        </div>
        <div class="service">
          <span class="num">03</span>
          <h3>Repayment Roadmap</h3>
          <p>A monthly plan built around your actual income, so commitments are realistic instead of another broken promise to a creditor.</p>
        </div>
        <div class="service">
          <span class="num">04</span>
          <h3>Know-Your-Rights Coaching</h3>
          <p>What collectors can and can't legally do in the Philippines, so you can respond from a position of information rather than fear.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- PROCESS -->
  <section id="process" class="band-forest">
    <div class="wrap">
      <div class="section-head">
        <div class="eyebrow">How an engagement runs</div>
        <h2>Four steps, start to finish</h2>
        <p>No jargon, no long retainer — a straightforward sequence from first conversation to a plan you can act on.</p>
      </div>
    </div>
    <div class="wrap">
      <div class="process">
        <div class="step">
          <span class="step-no">Step 1</span>
          <h3>Free initial call</h3>
          <p>15–20 minutes to understand your situation and confirm I can actually help before any commitment.</p>
        </div>
        <div class="step">
          <span class="step-no">Step 2</span>
          <h3>Full account review</h3>
          <p>You share your statements and notices; I map every balance, rate, and creditor deadline.</p>
        </div>
        <div class="step">
          <span class="step-no">Step 3</span>
          <h3>Negotiation plan</h3>
          <p>We agree on target terms and talking points for each creditor, in the order that protects you most.</p>
        </div>
        <div class="step">
          <span class="step-no">Step 4</span>
          <h3>Ongoing support</h3>
          <p>I stay available while you execute — reviewing offers, prepping responses, adjusting as creditors reply.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="wrap about-grid">
      <div>
        <div class="eyebrow">Why work with me</div>
        <h2>Insider experience, used on your behalf</h2>
        <p style="color:var(--ink-soft); max-width:52ch;">I spent over a decade in the collections industry — the calls, the escalation paths, the settlement authority most agents never mention. Fresh Ledger Consulting exists to put that knowledge to work for the person on the receiving end of the call, not the creditor.</p>

        <div class="stat-row">
          <div class="stat">
            <div class="n">12+</div>
            <div class="l">Years in collections</div>
          </div>
          <div class="stat">
            <div class="n">1:1</div>
            <div class="l">Private engagements</div>
          </div>
          <div class="stat">
            <div class="n">PH</div>
            <div class="l">Philippines-wide, remote</div>
          </div>
        </div>
      </div>

      <ul class="principles">
        <li><span class="tick">✓</span> Every conversation is confidential — your situation is never shared or discussed with your creditors without your say-so.</li>
        <li><span class="tick">✓</span> No pressure tactics. If consulting won't meaningfully help your case, I'll tell you directly.</li>
        <li><span class="tick">✓</span> Plans are built around what you can actually pay — not a number that sounds good on a call.</li>
        <li><span class="tick">✓</span> All sessions held remotely by phone or video, on your schedule.</li>
      </ul>
    </div>
  </section>

  <!-- DISCLAIMER -->
  <section style="padding-top:0;">
    <div class="wrap">
      <div class="disclaimer">
        <strong>A note on what this service is:</strong> Fresh Ledger Consulting provides debt negotiation consulting based on industry experience. This is not a law firm, and consulting here is not legal, tax, or licensed financial advice. Outcomes depend on your creditors, your accounts, and your circumstances, and no specific settlement amount, interest reduction, or approval can be guaranteed. For matters involving active legal proceedings, garnishment, or formal disputes, you should also consult a licensed attorney.
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="wrap">
      <div class="contact-panel">
        <div>
          <div class="eyebrow" style="color:var(--brass);">Get in touch</div>
          <h2>Start with a free, confidential call</h2>
          <p>Reach out directly — no forms, no gatekeeping. I respond personally to every message.</p>

          <ul class="contact-list">
            <li>
              <a href="mailto:armjdarmjd16@gmail.com">
                <span class="ic">MAIL</span> armjdarmjd16@gmail.com
              </a>
            </li>
            <li>
              <a href="tel:+639274186327">
                <span class="ic">TEL</span> 0927 418 6327
              </a>
            </li>
          </ul>
          <p class="contact-note">Available for calls and messages on Philippine business hours. Weekend slots by request.</p>
        </div>

        <div class="service-area">
          <div class="eyebrow">Service area</div>
          <h3 style="color:var(--white); font-size:1.05rem;">Philippines, nationwide</h3>
          <p style="color:#C7D0DB; margin-top:8px;">All consultations are conducted remotely by phone or video call, so location anywhere in the Philippines is not a barrier.</p>
        </div>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="wrap">
    Fresh Ledger Consulting · Independent debt negotiation consulting · Philippines · Not a law firm
  </div>
</footer>

</body>
</html>
