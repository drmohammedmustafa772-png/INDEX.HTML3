<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SmartContentAI</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Firebase SDK -->
  <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-app.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-auth.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-firestore.js"></script>
  <script>
    const firebaseConfig = {
      apiKey: "AIzaSyC-YourRealKey",
      authDomain: "smart-content-ai.firebaseapp.com",
      projectId: "smart-content-ai",
      storageBucket: "smart-content-ai.appspot.com",
      messagingSenderId: "1234567890",
      appId: "1:1234567890:web:abcdef123456"
    };
    firebase.initializeApp(firebaseConfig);
    const db = firebase.firestore();
  </script>

  <style>
    body {font-family: Arial, sans-serif; margin:0; padding:0;}
    section {padding:40px; border-bottom:1px solid #ddd;}
    .dark-mode {background:#222; color:#fff;}
    button {padding:10px 20px; margin:5px;}
    iframe {width:100%; height:400px; border:none;}
  </style>
</head>
<body>

  <!-- Features -->
  <section id="features">
    <h2>Key Features</h2>
    <p>🌐 Multilingual AI, 📈 SEO Optimization, ☁️ SaaS Cloud, ⚡ Automation</p>
  </section>

  <!-- Plans -->
  <section id="plans">
    <h2>Subscription Plans</h2>
    <p>Basic: €17/month</p>
  </section>

  <!-- Payment Methods -->
  <section id="payment">
    <h2>Payment Methods</h2>
    <a href="https://paypal.me/drzyogo" target="_blank"><button>Pay with PayPal</button></a>
    <button onclick="alert('Stripe: mustangteam.com@gmail.com')">Pay with Stripe</button>
  </section>

  <!-- Bank Transfer -->
  <section id="bank">
    <h2>Bank Transfer</h2>
    <h3>EGP Account</h3>
    <p>IBAN: EG660022012880211112491757001<br>SWIFT: ABRKEGCAXXX<br>Branch: Al Hadiqa Al dawlia</p>
    <h3>USD Account</h3>
    <p>IBAN: EG310022012880211102491757001<br>SWIFT: ABRKEGCAXXX<br>Branch: Al Hadiqa Al dawlia</p>
  </section>

  <!-- Amazon Affiliate -->
  <section id="amazon">
    <h2>Amazon Products</h2>
    <iframe src="https://www.amazon.com/affiliate-link-example"></iframe>
  </section>

  <!-- Google AdSense -->
  <section id="adsense">
    <h2>Sponsored Ads</h2>
    <ins class="adsbygoogle"
         style="display:block"
         data-ad-client="ca-pub-XXXXXXXXXX"
         data-ad-slot="1234567890"
         data-ad-format="auto"></ins>
    <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
  </section>

  <!-- FAQ -->
  <section id="faq">
    <h2>FAQ</h2>
    <p>All services are free except optional premium upgrades.</p>
  </section>

  <!-- Testimonials -->
  <section id="testimonials">
    <h2>Testimonials</h2>
    <p>"SmartContentAI changed my workflow!"</p>
  </section>

  <!-- Newsletter -->
  <section id="newsletter">
    <h2>Newsletter</h2>
    <input type="email" placeholder="Enter your email">
    <button>Subscribe</button>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact</h2>
    <p>Email: support@smartcontentai.com</p>
  </section>

  <!-- Dashboard -->
  <section id="dashboard">
    <h2>Dashboard</h2>
    <input type="email" id="email" placeholder="Email">
    <input type="password" id="password" placeholder="Password">
    <button onclick="signup()">Sign Up</button>
    <button onclick="login()">Login</button>
    <script>
      function signup(){
        const email = document.getElementById('email').value;
        const password = document.getElementById('password').value;
        firebase.auth().createUserWithEmailAndPassword(email, password)
          .then(user => alert('Signed up: ' + user.user.email))
          .catch(err => alert(err.message));
      }
      function login(){
        const email = document.getElementById('email').value;
        const password = document.getElementById('password').value;
        firebase.auth().signInWithEmailAndPassword(email, password)
          .then(user => alert('Logged in: ' + user.user.email))
          .catch(err => alert(err.message));
      }
    </script>
  </section>

  <!-- Try the Model -->
  <section id="model">
    <h2>Try the Model</h2>
    <input type="text" id="userInput" placeholder="اكتب نص للتجربة">
    <button onclick="runModel()">Run Demo</button>
    <pre id="output"></pre>
  </section>

  <script>
    async function runModel(){
      const userText = document.getElementById("userInput").value;
      const response = await fetch("https://api-inference.huggingface.co/models/gpt2", {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
          "Authorization": "Bearer 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"
        },
        body: JSON.stringify({ inputs: userText })
      });
      const data = await response.json();
      document.getElementById("output").textContent = data[0].generated_text;
    }
  </script>

  <!-- Dark Mode -->
  <section id="darkmode">
    <h2>Dark Mode</h2>
    <button onclick="document.body.classList.toggle('dark-mode')">Toggle Dark Mode</button>
  </section>

  <!-- Crisp Chatbot -->
  <script type="text/javascript">
    window.$crisp=[];
    window.CRISP_WEBSITE_ID="dde9e35f-2015-40f2-b353-17cd0eef1828";
    (function(){
      d=document;s=d.createElement("script");
      s.src="https://client.crisp.chat/l.js";s.async=1;
      d.getElementsByTagName("head")[0].appendChild(s);
    })();
  </script>

  <!-- Google Analytics -->
  <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
  <script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'G-XXXXXXXXXX');
  </script>

</body>
</html> 
