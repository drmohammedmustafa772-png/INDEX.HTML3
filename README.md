<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SmartContentAI</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Crisp Chatbot Integration -->
  <script type="text/javascript">
    window.$crisp=[];
    window.CRISP_WEBSITE_ID="dd4e9e53-2015-40f2-853f-17cdb6eff82d";
    (function(){
      d=document;s=d.createElement("script");
      s.src="https://client.crisp.chat/l.js";s.async=1;
      d.getElementsByTagName("head")[0].appendChild(s);
    })();
  </script>

  <!-- Firebase SDK -->
  <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-app.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-auth.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-firestore.js"></script>
  <script>
    const firebaseConfig = {
      apiKey: "YOUR_FIREBASE_API_KEY",
      authDomain: "YOUR_FIREBASE_PROJECT.firebaseapp.com",
      projectId: "YOUR_FIREBASE_PROJECT",
      storageBucket: "YOUR_FIREBASE_PROJECT.appspot.com",
      messagingSenderId: "YOUR_SENDER_ID",
      appId: "YOUR_APP_ID"
    };
    firebase.initializeApp(firebaseConfig);
    const db = firebase.firestore();
  </script>

  <style>
    body {font-family: Arial; margin:0; padding:0; background:#f9f9f9; color:#333;}
    header {background:#004080; color:#fff; text-align:center; padding:20px;}
    section {padding:20px; margin:20px auto; max-width:900px; background:#fff; border-radius:8px;}
    .card {background:#f0f8ff; padding:15px; border-radius:6px; margin:10px;}
    button {padding:10px 20px; margin:5px; border:none; border-radius:5px; background:#0073e6; color:#fff; cursor:pointer;}
    button:hover {background:#005bb5;}
    footer {text-align:center; background:#004080; color:#fff; padding:15px;}
    .dark-mode {background:#121212; color:#f1f1f1;}
    .dark-mode section {background:#1e1e1e; color:#f1f1f1;}
  </style>
</head>
<body>
  <header>
    <h1>SmartContentAI</h1>
    <p>Global SaaS platform for multilingual content and automation</p>
    <button onclick="toggleDarkMode()">Toggle Dark Mode</button>
  </header>
<script type="text/javascript">window.$crisp=[];window.CRISP_WEBSITE_ID="dd4e9e53-2015-40f2-853f-17cdb6eff82d";(function(){d=document;s=d.createElement("script");s.src="https://client.crisp.chat/l.js";s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})();</script>
  <!-- Features -->
  <section id="features">
    <h2>🔑 Key Features</h2>
    <div class="card">🌐 Multilingual AI</div>
    <div class="card">📈 SEO Optimization</div>
    <div class="card">☁️ Cloud SaaS</div>
    <div class="card">⚡ Automation</div>
  </section>

  <!-- Subscription Plans -->
  <section id="plans">
    <h2>📦 Subscription Plans</h2>
    <div class="card">Basic – $12/month</div>
    <div class="card">Pro – $29/month</div>
    <div class="card">Enterprise – $99/month</div>
  </section>

  <!-- Payment -->
  <section id="payment">
    <h2>💳 Payment Methods</h2>
    <p>Bank Transfer: IBAN EG660022012880211112491757001</p>
    <button onclick="window.location.href='https://www.paypal.com/paypalme/drzyogo'">Pay with PayPal</button>
    <button onclick="alert('Stripe integration coming soon')">Pay with Stripe</button>
  </section>

  <!-- Try the Model -->
  <section id="ai-demo">
    <h2>🤖 Try the Model</h2>
    <button onclick="document.getElementById('output').innerText='AI generated demo content...'">Try Demo</button>
    <div id="output"></div>
  </section>

  <!-- Smart Chatbot -->
  <section id="chatbot">
    <h2>🤖 Smart Chatbot</h2>
    <p>Ask me anything about SmartContentAI and I will answer instantly.</p>
  </section>

  <!-- User Dashboard -->
  <section id="dashboard">
    <h2>👤 User Dashboard</h2>
    <form id="signupForm">
      <input type="email" id="email" placeholder="Email" required>
      <input type="password" id="password" placeholder="Password" required>
      <input type="submit" value="Sign Up">
    </form>
    <form id="loginForm">
      <input type="email" id="loginEmail" placeholder="Email" required>
      <input type="password" id="loginPassword" placeholder="Password" required>
      <input type="submit" value="Login">
    </form>
    <div id="userData"></div>
  </section>

  <script>
    function toggleDarkMode(){document.body.classList.toggle("dark-mode");}
    const signupForm=document.getElementById('signupForm');
    signupForm.addEventListener('submit',async(e)=>{
      e.preventDefault();
      const email=document.getElementById('email').value;
      const password=document.getElementById('password').value;
      try{
        const userCredential=await firebase.auth().createUserWithEmailAndPassword(email,password);
        const user=userCredential.user;
        await db.collection('users').doc(user.uid).set({email:user.email,plan:"Basic"});
        document.getElementById('userData').innerText="User registered: "+user.email;
      }catch(error){alert(error.message);}
    });
    const loginForm=document.getElementById('loginForm');
    loginForm.addEventListener('submit',async(e)=>{
      e.preventDefault();
      const email=document.getElementById('loginEmail').value;
      const password=document.getElementById('loginPassword').value;
      try{
        const userCredential=await firebase.auth().signInWithEmailAndPassword(email,password);
        const user=userCredential.user;
        document.getElementById('userData').innerText="Logged in: "+user.email;
      }catch(error){alert(error.message);}
    });
  </script>

  <!-- FAQ -->
  <section id="faq">
    <h2>❓ FAQ</h2>
    <p>How do I subscribe? Choose a plan and pay via Bank transfer, PayPal, or Stripe.</p>
    <p>Can I cancel anytime? Yes.</p>
  </section>

  <!-- Testimonials -->
  <section id="testimonials">
    <h2>💬 Testimonials</h2>
    <p>"SmartContentAI helped me grow my business internationally!"</p>
  </section>

  <!-- Newsletter -->
  <section id="newsletter">
    <h2>📧 Newsletter</h2>
    <form>
      <input type="email" placeholder="Enter your email">
      <input type="submit" value="Subscribe">
    </form>
  </section>

  <!-- Contact Us -->
  <section id="contact">
    <h2>📞 Contact Us</h2>
    <p>Email: support@smartcontentai.com</p>
    <p>Phone: +201126674337</p>
  </section>

  <footer>
    <p>© 2026 SmartContentAI</p>
  </footer>

  <!-- Service Worker -->
  <script>
    const swCode=`
      self.addEventListener('install',event=>{
        event.waitUntil(
          caches.open('smartcontent-cache').then(cache=>{
            return cache.addAll(['./index.html']);
          })
        );
      });
      self.addEventListener('fetch',event=>{
        event.respondWith(
          caches.match(event.request).then(response=>{
            return response||fetch(event.request);
          })
        );
      });
    `;
    const blob=new Blob([swCode],{type:'application/javascript'});
    const swUrl=URL.createObjectURL(blob);
    if('serviceWorker' in navigator){
      navigator.serviceWorker.register(swUrl).then(()=>console.log('Service Worker Registered'));
    }
  </script>
</body>
</html> 
