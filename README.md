<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SmartContentAI</title>
  <meta name="description" content="SmartContentAI - Global AI-powered SaaS for multilingual content, SEO, automation, and cloud services.">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Google Analytics -->
  <script async src="https://www.googletagmanager.com/gtag/js?id=UA-XXXXXXX-X"></script>
  <script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'UA-XXXXXXX-X');
  </script>

  <!-- Crisp Chatbot Integration -->
  <script type="text/javascript">
    window.$crisp=[];
    window.CRISP_WEBSITE_ID="dd4e9e53-2015-40f2-853f-17cdb6eff82d";
    (function(){
      d=document;
      s=d.createElement("script");
      s.src="https://client.crisp.chat/l.js";
      s.async=1;
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
    body {font-family: Arial, sans-serif; margin:0; padding:0; background:#f9f9f9; color:#333;}
    header {background:#004080; color:#fff; text-align:center; padding:40px 20px;}
    section {padding:40px 20px; background:#fff; margin:20px auto; max-width:900px; border-radius:8px;}
    .card {background:#f0f8ff; padding:20px; border-radius:6px; margin:10px;}
    footer {text-align:center; background:#004080; color:#fff; padding:15px; margin-top:30px;}
  </style>
</head>
<body>
  <header>
    <h1>SmartContentAI</h1>
    <p>Global SaaS platform for multilingual content and automation</p>
  </header>

  <!-- Features -->
  <section id="features">
    <h2>🔑 Features</h2>
    <div class="card">🌐 Multilingual AI</div>
    <div class="card">📈 SEO Optimization</div>
    <div class="card">☁️ Cloud SaaS</div>
    <div class="card">⚡ Automation</div>
  </section>

  <!-- Subscription Plans -->
  <section id="plans">
    <h2>📦 Plans</h2>
    <div class="card">Basic – $12/month</div>
    <div class="card">Pro – $29/month</div>
    <div class="card">Enterprise – $99/month</div>
  </section>

  <!-- Payment -->
  <section id="payment">
    <h2>💳 Payment</h2>
    <p>IBAN: EG660022012880211112491757001</p>
    <button>PayPal</button>
    <button>Stripe</button>
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
    // Sign Up with Free Trial
    const signupForm = document.getElementById('signupForm');
    signupForm.addEventListener('submit', async (e) => {
      e.preventDefault();
      const email = document.getElementById('email').value;
      const password = document.getElementById('password').value;
      try {
        const userCredential = await firebase.auth().createUserWithEmailAndPassword(email, password);
        const user = userCredential.user;
        const startDate = new Date();
        const endDate = new Date();
        endDate.setDate(startDate.getDate() + 7); // أسبوع مجاني

        await db.collection('users').doc(user.uid).set({
          email: user.email,
          plan: "Trial",
          trialStart: startDate.toISOString(),
          trialEnd: endDate.toISOString()
        });

        document.getElementById('userData').innerText = "Free Trial started for: " + user.email;
      } catch (error) {
        alert(error.message);
      }
    });

    // Login and check trial
    const loginForm = document.getElementById('loginForm');
    loginForm.addEventListener('submit', async (e) => {
      e.preventDefault();
      const email = document.getElementById('loginEmail').value;
      const password = document.getElementById('loginPassword').value;
      try {
        const userCredential = await firebase.auth().signInWithEmailAndPassword(email, password);
        const user = userCredential.user;
        const doc = await db.collection('users').doc(user.uid).get();
        const data = doc.data();

        const now = new Date();
        if (data.plan === "Trial" && new Date(data.trialEnd) < now) {
          await db.collection('users').doc(user.uid).update({ plan: "Basic" });
          document.getElementById('userData').innerText = "Trial ended. Upgraded to Basic plan.";
        } else {
          document.getElementById('userData').innerText = "Logged in: " + user.email + " | Plan: " + data.plan;
        }
      } catch (error) {
        alert(error.message);
      }
    });
  </script>

  <!-- FAQ -->
  <section id="faq">
    <h2>❓ FAQ</h2>
    <p>How do I subscribe? Choose a plan and pay online.</p>
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

  <footer>
    <p>© 2026 SmartContentAI</p>
  </footer>

  <!-- Service Worker -->
  <script>
    const swCode = `
      self.addEventListener('install', event => {
        event.waitUntil(
          caches.open('smartcontent-cache').then(cache => {
            return cache.addAll(['./index.html']);
          })
        );
      });
      self.addEventListener('fetch', event => {
        event.respondWith(
          caches.match(event.request).then(response => {
            return response || fetch(event.request);
          })
        );
      });
    `;
    const blob = new Blob([swCode], {type: 'application/javascript'});
    const swUrl = URL.createObjectURL(blob);
    if ('serviceWorker' in navigator) {
      navigator.serviceWorker.register(swUrl).then(() => console.log('Service Worker Registered'));
    }
  </script>
</body>
</html> 
