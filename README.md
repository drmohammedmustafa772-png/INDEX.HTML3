<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SmartContentAI</title>
  <meta name="description" content="SmartContentAI - Global AI-powered SaaS for multilingual content, SEO, automation, and cloud services.">
  <meta name="keywords" content="AI, SaaS, SEO, Automation, Multilingual, Cloud, SmartContentAI">
  <meta name="author" content="SmartContentAI">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Google Analytics -->
  <script async src="https://www.googletagmanager.com/gtag/js?id=UA-XXXXXXX-X"></script>
  <script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'UA-XXXXXXX-X');
  </script>

  <!-- Google AdSense -->
  <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
  <script>
    (adsbygoogle = window.adsbygoogle || []).push({
      google_ad_client: "ca-pub-XXXXXXXXXXXXXXXX",
      enable_page_level_ads: true
    });
  </script>

  <!-- Schema.org for SEO -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "SmartContentAI",
    "applicationCategory": "BusinessApplication",
    "operatingSystem": "Web",
    "description": "AI-powered SaaS for multilingual content, SEO, automation, and cloud services."
  }
  </script>

  <!-- PWA Manifest -->
  <link rel="manifest" href="manifest.json">
  <meta name="theme-color" content="#004080">

  <style>
    body {font-family: Arial, sans-serif; margin:0; padding:0; background:#f9f9f9; color:#333; transition:background 0.3s, color 0.3s;}
    header {background:#004080; color:#fff; text-align:center; padding:40px 20px;}
    .buttons {text-align:center; margin:20px 0;}
    .button {display:inline-block; background:#0073e6; color:#fff; padding:12px 25px; margin:10px; border-radius:6px; text-decoration:none; font-weight:bold; transition:background 0.3s;}
    .button:hover {background:#005bb5;}
    section {padding:40px 20px; background:#fff; margin:20px auto; max-width:900px; border-radius:8px; box-shadow:0 2px 6px rgba(0,0,0,0.1);}
    .features {display:flex; flex-wrap:wrap; gap:20px;}
    .card {flex:1 1 40%; background:#f0f8ff; padding:20px; border-radius:6px; box-shadow:0 1px 4px rgba(0,0,0,0.1);}
    form {background:#f5f5f5; padding:20px; border-radius:6px;}
    form input, form textarea {width:100%; padding:10px; margin:8px 0; border:1px solid #ccc; border-radius:4px;}
    form input[type="submit"] {background:#28a745; color:#fff; border:none; cursor:pointer; font-weight:bold;}
    form input[type="submit"]:hover {background:#218838;}
    footer {text-align:center; background:#004080; color:#fff; padding:15px; margin-top:30px;}
    #output {margin-top:20px; padding:15px; background:#eef; border-radius:6px;}
    .social {text-align:center; margin-top:20px;}
    .social a {margin:0 10px; text-decoration:none; color:#0073e6; font-weight:bold;}
    .dark-mode {background:#121212; color:#f1f1f1;}
    .dark-mode section {background:#1e1e1e; color:#f1f1f1;}
  </style>
</head>
<body>
  <!-- Language Selector -->
  <div style="text-align:right; padding:10px;">
    <select id="languageSwitcher" onchange="setLanguage(this.value)">
      <option value="en">English</option>
      <option value="ar">العربية</option>
      <option value="fr">Français</option>
      <option value="es">Español</option>
    </select>
  </div>

  <header>
    <h1 id="title">SmartContentAI</h1>
    <p id="subtitle">A global AI-powered SaaS platform for multilingual content creation, workflow automation, and more.</p>
    <button onclick="toggleDarkMode()" class="button">Toggle Dark Mode</button>
  </header>

  <!-- Main Buttons -->
  <div class="buttons">
    <a href="#features" class="button">View Features</a>
    <a href="#plans" class="button">Subscription Plans</a>
    <a href="#payment" class="button">Payment Methods</a>
    <a href="#ai-demo" class="button">Try the Model</a>
    <a href="#chatbot" class="button">Smart Chatbot</a>
    <a href="#faq" class="button">FAQ</a>
    <a href="#testimonials" class="button">Testimonials</a>
    <a href="#newsletter" class="button">Newsletter</a>
    <a href="#contact" class="button">Contact Us</a>
  </div>

  <!-- Features Section -->
  <section id="features">
    <h2 id="featuresTitle">🔑 Key Features</h2>
    <div class="features">
      <div class="card"><h3>🌐 Multilingual AI</h3><p>Create and optimize content in multiple languages.</p></div>
      <div class="card"><h3>📈 SEO Optimization</h3><p>Boost visibility and ranking with integrated SEO tools.</p></div>
      <div class="card"><h3>☁️ Cloud SaaS</h3><p>Secure, scalable, and accessible anywhere, anytime.</p></div>
      <div class="card"><h3>⚡ Automation</h3><p>Streamline workflows and scale productivity.</p></div>
    </div>
  </section>

  <!-- Subscription Plans -->
  <section id="plans">
    <h2>📦 Subscription Plans</h2>
    <div class="features">
      <div class="card"><h3>Basic</h3><p>$12/month – Access to AI content creation.</p></div>
      <div class="card"><h3>Pro</h3><p>$29/month – Includes SEO tools, automation, and analytics.</p></div>
      <div class="card"><h3>Enterprise</h3><p>$99/month – Full features, priority support, and custom solutions.</p></div>
    </div>
  </section>

  <!-- Payment Section -->
  <section id="payment">
    <h2 id="paymentTitle">💳 Payment Methods</h2>
    <p>Trial subscription ($6 for the first month), then $12 monthly:</p>
    <ul>
      <li><strong>IBAN:</strong> EG660022012880211112491757001</li>
      <li><strong>Branch:</strong> Al Hadiqa Al Dawlia</li>
      <li><strong>Phone:</strong> 00201126674337</li>
      <li><strong>SWIFT:</strong> ABRKEGCAXXX</li>
    </ul>
    <p>Or pay online:</p>
    <button class="button">Pay with PayPal</button>
    <button class="button">Pay with Stripe</button>
  </section>

  <!-- AI Demo Section -->
  <section id="ai-demo">
    <h2>🤖 Try the Model</h2>
    <button onclick="generateContent('Write a short article about Artificial Intelligence')">Try the Model</button>
    <div id="output"></div>
  </section>

  <!-- Smart Chatbot -->
  <section id="chatbot">
    <h2>🤖 Smart Chatbot</h2>
    <p>Ask me anything about SmartContentAI and I will answer instantly.</p>
  </section>

  <!-- Crisp Chatbot Integration -->
  <script type="text/javascript">
    window.$crisp=[];window.CRISP_WEBSITE_ID="YOUR-CRISP-ID";
    (function(){
      d=document;s=d.createElement("script");
      s.src="https://client.crisp.chat/l.js";s.async=1;
      d.getElementsByTagName("head")[0].appendChild(s);
    })();
  </script>

  <!-- FAQ Section -->
  <section id="faq">
    <h2>❓ Frequently Asked Questions</h2>
    <p><strong>How do I subscribe?</strong> Choose a plan and pay via bank transfer, PayPal, or Stripe 
