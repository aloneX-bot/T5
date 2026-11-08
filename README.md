
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#ffffff">
<title>getebook.ai — Write it once. Let it earn forever.</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root{
 --orange:#f47761;
 --orange-dark:#df674f;
 --pink:#fac5bb;
 --ink:#342b28;
 --muted:#827a76;
 --cream:#faf7f3;
 --border:#eae6e1;
 --white:#fff;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{
 font-family:'DM Sans',sans-serif;
 background:white;color:var(--ink);
}
button,a{font:inherit}
button{cursor:pointer}
a{text-decoration:none;color:inherit}
.container{width:min(1160px,92%);margin:auto}

/* HEADER */
header{
 height:76px;background:#fff;
 position:sticky;top:0;z-index:50;
 border-bottom:1px solid #f1efec;
}
.nav{
 height:100%;display:flex;
 align-items:center;justify-content:space-between;
}
.logo{
 display:flex;align-items:center;gap:11px;
 font-size:28px;font-weight:800;letter-spacing:-1.2px;
}
.logo-icon{color:var(--orange);font-size:36px}
.logo .ai{color:var(--orange)}
.nav-links{display:flex;gap:28px;align-items:center;font-size:13px}
.nav-links a:hover{color:var(--orange)}
.nav-right{display:flex;gap:10px}
.btn{
 border:0;border-radius:8px;padding:13px 21px;
 font-size:13px;font-weight:700;transition:.2s;
}
.btn-primary{background:var(--orange);color:white}
.btn-primary:hover{background:var(--orange-dark);transform:translateY(-2px)}
.btn-outline{background:white;border:1px solid var(--border)}
.menu-btn{
 display:none;border:0;background:none;
 font-size:27px;color:var(--ink)
}

/* HERO */
.hero{
 padding:28px 0 65px;
 text-align:center;
 background:
 radial-gradient(ellipse at 50% 30%,#fff9f7 0%,white 70%);
}
.social-proof{
 display:inline-flex;align-items:center;gap:12px;
 border:1px solid #f1ded9;
 border-radius:40px;padding:12px 20px;
 color:#a95645;font-size:15px;font-weight:700;
 margin-bottom:40px;
}
.proof-dot{
 width:13px;height:13px;border-radius:50%;
 background:var(--orange);
 box-shadow:0 0 0 5px #fce5df;
}
.hero h1{
 font-size:clamp(44px,7vw,76px);
 font-weight:800;letter-spacing:-3px;
 line-height:1.12;color:#342a27;
 max-width:850px;margin:0 auto 45px;
}
.hero h1 span{color:var(--orange)}
.hero-description{
 max-width:730px;margin:0 auto;
 font-size:clamp(16px,2.5vw,28px);
 line-height:1.75;color:#827873;
 font-weight:400;
}

/* PROMPT BOX */
.prompt-wrap{
 max-width:850px;margin:45px auto 20px;
 position:relative;
}
.prompt-box{
 position:relative;
 min-height:260px;
 border:1.5px solid #e7e3df;
 border-radius:27px;
 background:#fff;
 box-shadow:0 15px 45px #00000008;
 text-align:left;
 transition:.2s;
}
.prompt-box:focus-within{
 border-color:#f4b4a8;
 box-shadow:0 15px 45px #f4776110;
}
.prompt-box textarea{
 display:block;width:100%;height:205px;
 padding:29px 35px 65px;
 border:0;outline:none;resize:none;
 border-radius:27px;background:transparent;
 font-size:clamp(17px,2.5vw,25px);
 color:#403632;font-family:inherit;
 line-height:1.6;
}
.prompt-box textarea::placeholder{color:#c1bfbd}
.send-btn{
 position:absolute;right:24px;bottom:20px;
 width:73px;height:73px;border-radius:50%;
 border:0;background:var(--pink);color:white;
 font-size:38px;display:grid;place-items:center;
 transition:.2s;
}
.send-btn:hover{background:var(--orange);transform:translateY(-3px)}
.send-btn:disabled{opacity:.6;cursor:wait}
.suggestions{
 display:flex;justify-content:center;
 align-items:center;gap:12px;flex-wrap:wrap;
 margin:20px auto 0;
}
.suggestion{
 padding:12px 22px;border:1px solid #e8e4df;
 border-radius:30px;background:white;
 font-size:14px;color:#706761;
 transition:.2s;
}
.suggestion:hover,.suggestion:first-child{
 border-color:#f1c6bc;color:#a95848;
 background:#fffaf8;
}
.hero-note{
 margin:60px auto 0;
 color:#aaa39e;font-size:clamp(14px,2.5vw,23px);
 line-height:1.6;
}
.see-how{
 display:inline-block;margin-top:22px;
 color:#958d87;font-size:20px;font-weight:700;
}
.see-how:hover{color:var(--orange)}

/* PLATFORMS */
.platforms{
 padding:65px 0 115px;
 text-align:center;background:white;
}
.platform-title{
 color:#aaa39f;font-size:18px;
 letter-spacing:2px;font-weight:600;
 margin-bottom:42px;
}
.platform-grid{
 max-width:900px;margin:auto;
 display:flex;justify-content:center;
 align-items:center;gap:45px;
 flex-wrap:wrap;
}
.platform{
 width:78px;height:65px;
 display:flex;justify-content:center;align-items:center;
 transition:.2s;filter:grayscale(1);opacity:.65;
}
.platform:hover{filter:none;opacity:1;transform:translateY(-4px)}
.platform img{
 max-width:65px;max-height:49px;
 width:auto;height:auto;object-fit:contain;
}
.platform-text{
 font-size:14px;font-weight:800;color:#777;
 letter-spacing:-.5px;
}

/* BOOK SHOWCASE */
.showcase{
 background:var(--cream);
 padding:100px 0;
 text-align:center;
}
.section-tag{
 display:inline-block;
 background:white;border:1px solid #f0e5df;
 border-radius:40px;padding:13px 25px;
 color:#a65b4a;font-size:15px;
 font-weight:700;letter-spacing:.3px;
 margin-bottom:34px;
}
.section-title{
 font-size:clamp(35px,5vw,58px);
 letter-spacing:-1.8px;line-height:1.2;
 font-weight:800;
 max-width:850px;margin:0 auto 25px;
}
.section-description{
 max-width:800px;margin:auto;
 font-size:clamp(16px,2.4vw,26px);
 line-height:1.8;color:#827873;
}
.books{
 display:grid;grid-template-columns:1fr 1fr;
 gap:30px;max-width:850px;margin:55px auto 0;
}
.book-card{
 background:white;padding:25px;border-radius:17px;
 border:1px solid var(--border);
}
.book-cover{
 min-height:320px;padding:35px;
 display:flex;flex-direction:column;
 justify-content:space-between;align-items:center;
 color:white;background:linear-gradient(145deg,#f47761,#9c4c43);
}
.book-cover.green{background:linear-gradient(145deg,#597d68,#203b2e)}
.book-cover small{letter-spacing:3px;font-size:10px}
.book-cover h3{
 font-size:36px;line-height:1.2;
 font-weight:800;text-align:center;
}
.book-cover .art{font-size:65px}
.book-card p{margin-top:15px;font-size:13px;color:var(--muted)}

/* FEATURES */
.features-section{padding:100px 0}
.section-head{text-align:center;margin-bottom:55px}
.section-head p{
 color:var(--muted);font-size:15px;
 margin-top:15px;line-height:1.8
}
.features{
 display:grid;grid-template-columns:repeat(3,1fr);gap:20px
}
.feature{
 padding:30px;border:1px solid var(--border);
 border-radius:14px;background:white;
 transition:.2s;
}
.feature:hover{transform:translateY(-5px);box-shadow:0 12px 30px #00000008}
.feature-icon{
 width:48px;height:48px;border-radius:13px;
 background:#fff0ec;display:grid;place-items:center;
 font-size:23px;margin-bottom:20px
}
.feature h3{font-size:19px;margin-bottom:12px}
.feature p{font-size:13px;color:var(--muted);line-height:1.8}

/* HOW IT WORKS */
.how{background:#fff8f5;padding:95px 0}
.steps{display:grid;grid-template-columns:repeat(3,1fr);gap:30px}
.step{text-align:center;padding:20px}
.step-number{
 font-size:45px;font-weight:800;color:var(--orange);
 margin-bottom:15px
}
.step h3{font-size:21px;margin-bottom:12px}
.step p{font-size:13px;line-height:1.8;color:var(--muted)}

/* PRICING */
.pricing{padding:100px 0}
.price-card{
 max-width:430px;margin:auto;padding:35px;
 border:1px solid var(--border);border-radius:17px;
 box-shadow:0 12px 35px #00000006;
}
.price-card h3{font-size:20px}
.price{font-size:55px;font-weight:800;margin:18px 0}
.price small{font-size:14px;color:var(--muted);font-weight:400}
.price-card ul{list-style:none;margin:25px 0}
.price-card li{padding:10px 0;font-size:14px;color:#625b56}
.price-card li:before{content:"✓";color:var(--orange);font-weight:bold;margin-right:12px}
.price-card button{width:100%}

/* FAQ */
.faq-section{background:var(--cream);padding:90px 0}
.faq{max-width:750px;margin:auto}
.faq-item{padding:20px 0;border-bottom:1px solid #e5ded7}
.faq-question{
 display:flex;justify-content:space-between;
 cursor:pointer;font-size:15px;font-weight:700;
}
.faq-answer{
 display:none;color:var(--muted);
 font-size:13px;line-height:1.8;padding-top:15px
}
.faq-item.active .faq-answer{display:block}
.faq-icon{color:var(--orange);font-size:20px}

/* CTA */
.cta{padding:80px 20px;text-align:center}
.cta-inner{
 max-width:950px;margin:auto;padding:65px 25px;
 background:#342b28;color:white;border-radius:20px;
}
.cta-inner h2{
 font-size:clamp(30px,5vw,48px);
 margin-bottom:18px;letter-spacing:-1px
}
.cta-inner p{color:#d9cfca;font-size:14px;margin-bottom:25px}

/* FOOTER */
footer{border-top:1px solid var(--border);padding:35px 0}
.footer{
 display:flex;justify-content:space-between;
 align-items:center;gap:20px;flex-wrap:wrap
}
.footer p,.footer-links{font-size:12px;color:var(--muted)}
.footer-links{display:flex;gap:20px}

/* GENERATOR MODAL */
.generator{
 position:fixed;inset:0;background:#201c1af5;
 z-index:100;display:none;overflow-y:auto;padding:20px;
}
.generator.open{display:block}
.generator-inner{max-width:1000px;margin:auto;color:white}
.gen-top{
 display:flex;justify-content:space-between;
 align-items:center;margin-bottom:25px
}
.gen-top button{
 border:0;background:#ffffff20;color:white;
 padding:12px 18px;border-radius:8px
}
.gen-grid{
 display:grid;grid-template-columns:350px 1fr;gap:20px
}
.gen-panel{
 background:white;color:var(--ink);
 padding:25px;border-radius:13px
}
.gen-panel h2{font-size:24px;margin-bottom:10px}
.gen-panel>p{font-size:12px;color:var(--muted);line-height:1.7;margin-bottom:20px}
.field{margin-bottom:17px}
.field label{display:block;font-size:11px;font-weight:700;margin-bottom:8px}
.field input,.field textarea,.field select{
 width:100%;padding:12px;border:1px solid var(--border);
 border-radius:7px;font:inherit;font-size:12px;
 background:#fff;outline:none
}
.field textarea{height:100px;resize:vertical}
.gen-panel .btn{width:100%}
.gen-preview{
 background:#f8f5f1;color:var(--ink);
 padding:22px;border-radius:13px;min-height:500px
}
.gen-preview-top{display:flex;justify-content:space-between;margin-bottom:18px;font-size:12px}
.result-cover{
 min-height:240px;background:linear-gradient(145deg,#f47761,#9e5148);
 color:white;display:flex;flex-direction:column;
 align-items:center;justify-content:center;
 text-align:center;padding:25px;gap:20px
}
.result-cover h2{font-size:30px}
.result-content{background:white;padding:25px}
.result-content h3{font-size:20px;margin:15px 0}
.result-content p{font-size:12px;color:var(--muted);line-height:1.8}
.chapter-nav{display:flex;flex-wrap:wrap;gap:7px;margin:15px 0}
.chapter-nav button{
 padding:8px;border:1px solid var(--border);
 background:white;border-radius:5px;font-size:10px
}
.chapter-nav button.selected{background:#342b28;color:white}
.result-content textarea{
 width:100%;height:150px;padding:12px;
 border:1px solid var(--border);font:inherit;
 font-size:12px;line-height:1.7
}
.result-actions{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}
.result-actions button{font-size:11px}
.status{font-size:11px;color:#6d9773;margin-top:12px}
.loading{animation:pulse 1s infinite alternate}
@keyframes pulse{from{opacity:.45}to{opacity:1}}

@media(max-width:800px){
 .nav-links{display:none}
 .menu-btn{display:block}
 .nav-links.mobile-open{
  display:flex;position:absolute;top:76px;left:0;right:0;
  background:white;flex-direction:column;align-items:flex-start;
  padding:25px;border-bottom:1px solid var(--border);
  gap:20px
 }
 .nav-right .btn-outline{display:none}
 .features{grid-template-columns:repeat(2,1fr)}
 .gen-grid{grid-template-columns:1fr}
}
@media(max-width:600px){
 header{height:75px}
 .logo{font-size:25px}
 .logo-icon{font-size:32px}
 .hero{padding:25px 0 45px}
 .social-proof{font-size:13px;padding:11px 15px;margin-bottom:42px}
 .hero h1{
  font-size:clamp(42px,10vw,58px);
  letter-spacing:-2px;line-height:1.17;
  max-width:500px;margin-bottom:45px
 }
 .hero-description{font-size:17px;line-height:1.8;padding:0 5px}
 .prompt-wrap{margin:45px 0 18px}
 .prompt-box{min-height:260px;border-radius:25px}
 .prompt-box textarea{
  height:205px;padding:27px 25px 65px;
  font-size:20px;border-radius:25px
 }
 .send-btn{width:72px;height:72px;right:22px;bottom:20px}
 .suggestions{flex-direction:column;gap:12px;margin-top:20px}
 .suggestion{font-size:14px;padding:12px 18px;max-width:100%}
 .hero-note{margin-top:60px;font-size:16px}
 .see-how{font-size:18px;margin-top:20px}
 .platforms{padding:55px 0 100px}
 .platform-title{font-size:15px;margin-bottom:35px}
 .platform-grid{gap:25px 20px}
 .platform{width:65px;height:55px}
 .platform img{max-width:48px;max-height:42px}
 .showcase{padding:80px 0}
 .section-tag{font-size:13px;padding:12px 17px}
 .section-title{font-size:37px;letter-spacing:-1.2px}
 .section-description{font-size:18px;line-height:1.8}
 .books{grid-template-columns:1fr}
 .features{grid-template-columns:1fr}
 .steps{grid-template-columns:1fr;gap:15px}
 .features-section,.pricing{padding:75px 0}
 .faq-section{padding:75px 0}
 .cta-inner{padding:50px 20px}
 .footer{flex-direction:column;align-items:flex-start}
 .gen-grid{grid-template-columns:1fr}
 .generator{padding:12px}
 .gen-panel,.gen-preview{padding:17px}
 .gen-preview{min-height:0}
}
</style>
</head>

<body>

<!-- HEADER -->
<header>
 <div class="container nav">
  <a href="#" class="logo">
   <span class="logo-icon">◧</span>
   <span>getebook<span class="ai">.ai</span></span>
  </a>

  <nav class="nav-links" id="navLinks">
   <a href="#showcase">Examples</a>
   <a href="#features">Features</a>
   <a href="#how">How it works</a>
   <a href="#pricing">Pricing</a>
   <a href="#faq">FAQ</a>
  </nav>

  <div class="nav-right">
   <button class="btn btn-outline" onclick="openGenerator()">Log in</button>
   <button class="btn btn-primary" onclick="openGenerator()">Start creating →</button>
  </div>

  <button class="menu-btn" onclick="toggleMenu()">☰</button>
 </div>
</header>

<!-- HERO SECTION -->
<section class="hero">
 <div class="container">

  <div class="social-proof">
   <span class="proof-dot"></span>
   Loved by 12,000+ creators publishing with AI
  </div>

  <h1>
   Write it once.<br>
   <span>Let it earn<br>forever.</span>
  </h1>

  <p class="hero-description">
   Just tell Booker what you know. Watch it write every chapter and design your cover, building your finished ebook live in front of you.
  </p>

  <!-- MAIN PROMPT BOX -->
  <div class="prompt-wrap">
   <div class="prompt-box">
    <textarea
     id="mainPrompt"
     placeholder="Tell Booker what your book is about..."
     aria-label="Describe your ebook idea"
    ></textarea>

    <button class="send-btn" id="sendBtn" onclick="startBook()" aria-label="Generate ebook">
     ↑
    </button>
   </div>

   <div class="suggestions">
    <button class="suggestion" onclick="useSuggestion(this)">
     A meal-prep guide for busy parents
    </button>

    <button class="suggestion" onclick="useSuggestion(this)">
     Side-hustle 101 for complete beginners
    </button>

    <button class="suggestion" onclick="useSuggestion(this)">
     A productivity system that actually sticks
    </button>
   </div>
  </div>

  <div class="hero-note">
   No credit card to start · cancel anytime · plans from $29/mo
  </div>

  <a href="#how" class="see-how">See how it works ↓</a>

 </div>
</section>

<!-- PUBLISHING PLATFORMS -->
<section class="platforms">
 <div class="container">
  <div class="platform-title">PUBLISH AND SELL ON</div>

  <div class="platform-grid">

   <a class="platform" href="https://kdp.amazon.com/" target="_blank" aria-label="Amazon KDP">
    <img src="https://cdn.simpleicons.org/amazonkindle/777777" alt="Amazon Kindle">
   </a>

   <a class="platform" href="https://books.apple.com/" target="_blank" aria-label="Apple Books">
    <img src="https://cdn.simpleicons.org/applebooks/777777" alt="Apple Books">
   </a>

   <a class="platform" href="https://www.etsy.com/" target="_blank" aria-label="Etsy">
    <img src="https://cdn.simpleicons.org/etsy/777777" alt="Etsy">
   </a>

   <a class="platform" href="https://gumroad.com/" target="_blank" aria-label="Gumroad">
    <img src="https://cdn.simpleicons.org/gumroad/777777" alt="Gumroad">
   </a>

   <a class="platform" href="https://www.instagram.com/" target="_blank" aria-label="Instagram">
    <img src="https://cdn.simpleicons.org/instagram/777777" alt="Instagram">
   </a>

   <a class="platform" href="https://www.tiktok.com/" target="_blank" aria-label="TikTok">
    <img src="https://cdn.simpleicons.org/tiktok/777777" alt="TikTok">
   </a>

   <a class="platform" href="https://www.facebook.com/" target="_blank" aria-label="Facebook">
    <img src="https://cdn.simpleicons.org/facebook/777777" alt="Facebook">
   </a>

   <a class="platform" href="https://www.shopify.com/" target="_blank" aria-label="Shopify">
    <img src="https://cdn.simpleicons.org/shopify/777777" alt="Shopify">
   </a>

  </div>
 </div>
</section>

<!-- BOOK SHOWCASE -->
<section class="showcase" id="showcase">
 <div class="container">

  <div class="section-tag">FLIP THROUGH A REAL BOOK</div>

  <h2 class="section-title">
   See exactly what you'll create
  </h2>

  <p class="section-description">
   These are real books made with getebook.ai. One is a polished ebook, the other a print-ready coloring book. Tap the arrows to flip through the cover and first pages.
  </p>

  <div class="books">

   <div class="book-card">
    <div class="book-cover">
     <small>YOUR GUIDE TO BETTER LIVING</small>
     <h3>Healthy<br>Everyday<br>Habits</h3>
     <div class="art">✿</div>
     <small>A PRACTICAL GUIDE</small>
    </div>
    <p>Digital ebook preview</p>
   </div>

   <div class="book-card">
    <div class="book-cover green">
     <small>CREATIVE COLLECTION</small>
     <h3>The Art of<br>Mindful<br>Living</h3>
     <div class="art">❀</div>
     <small>COLORING & ACTIVITY BOOK</small>
    </div>
    <p>Print-ready book concept</p>
   </div>

  </div>
 </div>
</section>

<!-- FEATURES -->
<section class="features-section" id="features">
 <div class="container">

  <div class="section-head">
   <div class="section-tag">YOUR COMPLETE BOOK STUDIO</div>
   <h2 class="section-title">Everything you need to create your next ebook.</h2>
   <p>One workspace. Your ideas. Your finished digital products.</p>
  </div>

  <div class="features">

   <div class="feature">
    <div class="feature-icon">✍️</div>
    <h3>AI Book Writing</h3>
    <p>Transform your ideas into organized book outlines and readable chapters.</p>
   </div>

   <div class="feature">
    <div class="feature-icon">🎨</div>
    <h3>AI Cover Design</h3>
    <p>Create attractive cover concepts that give your book a professional identity.</p>
   </div>

   <div class="feature">
    <div class="feature-icon">📚</div>
    <h3>Book Structures</h3>
    <p>Organize your ebook into sections, chapters and a logical reading experience.</p>
   </div>

   <div class="feature">
    <div class="feature-icon">📝</div>
    <h3>Chapter Editor</h3>
    <p>Edit your manuscript and customize the writing to match your ideas.</p>
   </div>

   <div class="feature">
    <div class="feature-icon">📄</div>
    <h3>Book Export</h3>
    <p>Prepare your book for digital publishing and distribution.</p>
   </div>

   <div class="feature">
    <div class="feature-icon">🚀</div>
    <h3>Publishing Workflow</h3>
    <p>Bring your book idea from the first prompt to a finished manuscript.</p>
   </div>

  </div>
 </div>
</section>

<!-- HOW IT WORKS -->
<section class="how" id="how">
 <div class="container">

  <div class="section-head">
   <div class="section-tag">HOW IT WORKS</div>
   <h2 class="section-title">Your knowledge deserves to become a book.</h2>
  </div>

  <div class="steps">
   <div class="step">
    <div class="step-number">01</div>
    <h3>Tell Booker your idea</h3>
    <p>Enter a topic, concept or knowledge area that you want to turn into a book.</p>
   </div>

   <div class="step">
    <div class="step-number">02</div>
    <h3>Create your manuscript</h3>
    <p>Develop your outline, chapters and book content in one workspace.</p>
   </div>

   <div class="step">
    <div class="step-number">03</div>
    <h3>Publish your ebook</h3>
    <p>Review your work and prepare it for your preferred publishing platform.</p>
   </div>
  </div>

 </div>
</section>

<!-- PRICING -->
<section class="pricing" id="pricing">
 <div class="container">

  <div class="section-head">
   <div class="section-tag">SIMPLE PRICING</div>
   <h2 class="section-title">Start creating today.</h2>
   <p>Example pricing for the planned subscription model.</p>
  </div>

  <div class="price-card">
   <h3>Creator Plan</h3>
   <div class="price">$29<small> / month</small></div>

   <p style="font-size:12px;color:#888">
    Example plan — payments are not connected.
   </p>

   <ul>
    <li>Book creation workspace</li>
    <li>Book outline tools</li>
    <li>Chapter editing</li>
    <li>Cover design workspace</li>
    <li>Manuscript preview</li>
    <li>Publishing preparation</li>
   </ul>

   <button class="btn btn-primary" onclick="openGenerator()">
    Start creating →
   </button>
  </div>

 </div>
</section>

<!-- FAQ -->
<section class="faq-section" id="faq">
 <div class="container">

  <div class="section-head">
   <div class="section-tag">FAQ</div>
   <h2 class="section-title">Frequently asked questions.</h2>
  </div>

  <div class="faq">

   <div class="faq-item">
    <div class="faq-question" onclick="toggleFaq(this)">
     What is Booker?
     <span class="faq-icon">+</span>
    </div>
    <div class="faq-answer">
     Booker is the AI ebook creation assistant concept. It is designed to help users turn ideas into organized books.
    </div>
   </div>

   <div class="faq-item">
    <div class="faq-question" onclick="toggleFaq(this)">
     Do I need writing experience?
     <span class="faq-icon">+</span>
    </div>
    <div class="faq-answer">
     No. The planned workflow is designed to make book creation easier for beginners as well as experienced writers.
    </div>
   </div>

   <div class="faq-item">
    <div class="faq-question" onclick="toggleFaq(this)">
     Can I edit my book?
     <span class="faq-icon">+</span>
    </div>
    <div class="faq-answer">
     Yes. The current demonstration workspace includes editable chapter text.
    </div>
   </div>

   <div class="faq-item">
    <div class="faq-question" onclick="toggleFaq(this)">
     Does it generate books using real AI?
     <span class="faq-icon">+</span>
    </div>
    <div class="faq-answer">
     This frontend version uses demonstration content. A secure AI backend must be connected for genuine AI-generated books.
    </div>
   </div>

   <div class="faq-item">
    <div class="faq-question" onclick="toggleFaq(this)">
     Can I sell my ebooks?
     <span class="faq-icon">+</span>
    </div>
    <div class="faq-answer">
     The platform is designed around ebook publishing. Actual sales depend on your publishing platform, its policies and your account.
    </div>
   </div>

  </div>
 </div>
</section>

<!-- CTA -->
<section class="cta">
 <div class="cta-inner">
  <h2>Write it once. Let it earn forever.</h2>
  <p>Your next ebook starts with a single idea.</p>
  <button class="btn btn-primary" onclick="openGenerator()">
   Create your first book →
  </button>
 </div>
</section>

<footer>
 <div class="container footer">
  <a href="#" class="logo">
   <span class="logo-icon">◧</span>
   <span>getebook<span class="ai">.ai</span></span>
  </a>

  <div class="footer-links">
   <a href="#features">Features</a>
   <a href="#pricing">Pricing</a>
   <a href="#faq">FAQ</a>
  </div>

  <p>© 2026 getebook.ai. All rights reserved.</p>
 </div>
</footer>

<!-- BOOK GENERATOR -->
<div class="generator" id="generator">
 <div class="generator-inner">

  <div class="gen-top">
   <h2>📖 Booker — Book Studio</h2>
   <button onclick="closeGenerator()">✕ Close</button>
  </div>

  <div class="gen-grid">

   <div class="gen-panel">
    <h2>Create your book</h2>
    <p>Customize your book details and create a sample preview.</p>

    <div class="field">
     <label>BOOK TOPIC</label>
     <textarea id="bookTopic" placeholder="What is your book about?"></textarea>
    </div>

    <div class="field">
     <label>TARGET AUDIENCE</label>
     <input id="bookAudience" placeholder="Example: Beginners">
    </div>

    <div class="field">
     <label>BOOK TYPE</label>
     <select id="bookType">
      <option>Educational Ebook</option>
      <option>Practical Guide</option>
      <option>Business Ebook</option>
      <option>Self Improvement</option>
      <option>Workbook</option>
      <option>Story Book</option>
     </select>
    </div>

    <div class="field">
     <label>WRITING STYLE</label>
     <select id="bookTone">
      <option>Professional</option>
      <option>Friendly</option>
      <option>Beginner Friendly</option>
      <option>Inspirational</option>
     </select>
    </div>

    <button class="btn btn-primary" onclick="generateBook()">
     Generate book preview →
    </button>

    <div class="status" id="genStatus"></div>
   </div>

   <div class="gen-preview">
    <div class="gen-preview-top">
     <b>YOUR BOOK PREVIEW</b>
     <span id="previewStatus">Waiting for your idea</span>
    </div>

    <div id="bookResult" style="background:white;min-height:400px;padding:30px;text-align:center">
     <div style="font-size:50px;margin-top:100px">📖</div>
     <h3 style="margin-top:15px">Your book starts here.</h3>
     <p style="font-size:12px;color:#999;margin-top:10px">
      Enter your idea to create a book preview.
     </p>
    </div>
   </div>

  </div>
 </div>
</div>

<script>
/* NAVIGATION */
function toggleMenu(){
 document.getElementById('navLinks').classList.toggle('mobile-open');
}

/* FAQ */
function toggleFaq(el){
 el.parentElement.classList.toggle('active');
}

/* GENERATOR OPEN/CLOSE */
function openGenerator(topic=''){
 const modal=document.getElementById('generator');
 modal.classList.add('open');
 document.body.style.overflow='hidden';

 if(topic){
  document.getElementById('bookTopic').value=topic;
 }
}

function closeGenerator(){
 document.getElementById('generator').classList.remove('open');
 document.body.style.overflow='';
}

/* HERO SUGGESTIONS */
function useSuggestion(button){
 const prompt=document.getElementById('mainPrompt');
 prompt.value=button.textContent.trim();
 prompt.focus();
}

/* MAIN ARROW */
function startBook(){
 const topic=document.getElementById('mainPrompt').value.trim();

 if(topic.length<5){
  const prompt=document.getElementById('mainPrompt');
  prompt.focus();
  prompt.placeholder='Please tell Booker what your book is about...';
  return;
 }

 openGenerator(topic);
 generateBook();
}

/* SAMPLE BOOK CREATION */
let chapters=[];
let currentChapter=0;
let bookTitle='';

function escapeHTML(text){
 return String(text).replace(/[&<>"']/g,function(c){
  return {
   '&':'&amp;',
   '<':'&lt;',
   '>':'&gt;',
   '"':'&quot;',
   "'":'&#39;'
  }[c];
 });
}

function generateBook(){
 const topic=document.getElementById('bookTopic').value.trim();
 const audience=document.getElementById('bookAudience').value.trim()||'General readers';
 const type=document.getElementById('bookType').value;
 const tone=document.getElementById('bookTone').value;

 if(topic.length<5){
  document.getElementById('genStatus').textContent='Please enter a book topic first.';
  return;
 }

 document.getElementById('genStatus').textContent='Creating your book preview...';
 document.getElementById('previewStatus').textContent='Working...';

 const result=document.getElementById('bookResult');
 result.classList.add('loading');

 setTimeout(()=>{
  bookTitle=topic.charAt(0).toUpperCase()+topic.slice(1);

  chapters=[
   {
    title:'Introduction',
    text:`Welcome to ${bookTitle}.\n\nThis book is designed for ${audience}. It introduces the topic through a structured and approachable learning experience.\n\nThis is demonstration content, intended to show the book creation interface.`
   },
   {
    title:'Understanding the Basics',
    text:`Before exploring ${bookTitle} in depth, it is important to understand its foundations.\n\nStart by identifying the central concepts, learning the terminology and understanding how the different parts connect.\n\nBuild your understanding step by step.`
   },
   {
    title:'Essential Principles',
    text:`Every subject has principles that help readers understand it more clearly.\n\nOrganize the most important concepts into manageable sections. Explain why each principle matters and how it relates to the larger topic.\n\nSupport factual statements with reliable research and sources.`
   },
   {
    title:'Practical Application',
    text:`Understanding a concept is only the beginning.\n\nIntroduce practical examples, useful exercises and simple steps. Explain common mistakes and provide ways to review progress.\n\nAdapt recommendations to the needs of your readers.`
   },
   {
    title:'Common Challenges',
    text:`Readers may encounter questions and difficulties as they explore this topic.\n\nAddress common misunderstandings, explain where additional information may be needed and provide reliable resources for further learning.`
   },
   {
    title:'Conclusion',
    text:`You have now explored the foundations of ${bookTitle}.\n\nContinue learning, reviewing and applying the ideas that are most relevant to your goals.\n\nThank you for reading.`
   }
  ];

  currentChapter=0;
  renderBook(audience,type,tone);

  document.getElementById('genStatus').textContent='✓ Your sample preview is ready.';
  document.getElementById('previewStatus').textContent='Preview ready';
  result.classList.remove('loading');

 },1200);
}

/* RENDER BOOK */
function renderBook(audience,type,tone){
 const root=document.getElementById('bookResult');

 root.innerHTML=`
  <div class="result-cover">
   <div style="font-size:10px;letter-spacing:3px">${escapeHTML(type.toUpperCase())}</div>
   <h2>${escapeHTML(bookTitle)}</h2>
   <div style="font-size:11px;letter-spacing:2px">A BOOK BY YOU</div>
   <div style="font-size:30px">✦</div>
  </div>

  <div class="result-content">
   <p><b>Audience:</b> ${escapeHTML(audience)}</p>
   <p><b>Writing style:</b> ${escapeHTML(tone)}</p>

   <h3>Table of contents</h3>
   <div class="chapter-nav" id="chapterNav"></div>

   <h3 id="chapterTitle"></h3>

   <textarea id="chapterEditor" aria-label="Edit your chapter"></textarea>

   <div class="result-actions">
    <button class="btn btn-primary" onclick="saveChapter()">Save changes</button>
    <button class="btn btn-outline" onclick="downloadBook()">Download book</button>
   </div>

   <p style="font-size:10px;margin-top:15px">
    Sample content only. Review and edit before publishing.
   </p>
  </div>
 `;

 renderChapter();
}

function renderChapter(){
 const nav=document.getElementById('chapterNav');
 const editor=document.getElementById('chapterEditor');

 if(!nav||!editor)return;

 nav.innerHTML='';

 chapters.forEach((chapter,index)=>{
  const button=document.createElement('button');

  button.textContent=(index+1)+'. '+chapter.title;
  button.className=index===currentChapter?'selected':'';

  button.onclick=()=>{
   saveChapter();
   currentChapter=index;
   renderChapter();
  };

  nav.appendChild(button);
 });

 document.getElementById('chapterTitle').textContent=
 chapters[currentChapter].title;

 editor.value=chapters[currentChapter].text;
}

function saveChapter(){
 const editor=document.getElementById('chapterEditor');

 if(editor&&chapters[currentChapter]){
  chapters[currentChapter].text=editor.value;
 }
}

/* DOWNLOAD SAMPLE BOOK */
function downloadBook(){
 saveChapter();

 let content=`
 <!DOCTYPE html>
 <html>
 <head>
 <meta charset="UTF-8">
 <title>${escapeHTML(bookTitle)}</title>
 <style>
 body{max-width:760px;margin:50px auto;padding:25px;font-family:Georgia,serif;line-height:1.9;color:#342b28}
 h1{text-align:center;margin-bottom:50px}
 h2{margin-top:45px}
 p{white-space:pre-line}
 </style>
 </head>
 <body>
 <h1>${escapeHTML(bookTitle)}</h1>
 `;

 chapters.forEach(chapter=>{
  content+=`
   <h2>${escapeHTML(chapter.title)}</h2>
   <p>${escapeHTML(chapter.text)}</p>
  `;
 });

 content+='</body></html>';

 const blob=new Blob([content],{type:'text/html;charset=utf-8'});
 const url=URL.createObjectURL(blob);

 const link=document.createElement('a');
 link.href=url;
 link.download='my-ebook.html';
 link.click();

 URL.revokeObjectURL(url);
}

/* ENTER KEY */
document.getElementById('mainPrompt').addEventListener('keydown',function(e){
 if(e.key==='Enter'&&!e.shiftKey){
  e.preventDefault();
  startBook();
 }
});
</script>

</body>
</html>
