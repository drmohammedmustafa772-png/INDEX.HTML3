<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>SmartContentAI</title>
    <style>
        body {font-family: "Tahoma", Arial, sans-serif; margin:0; padding:0; background:#f9f9f9; color:#333;}
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
    </style>

    <!-- Google AdSense -->
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
    <script>
      (adsbygoogle = window.adsbygoogle || []).push({
        google_ad_client: "ca-pub-XXXXXXXXXXXXXXXX", // ضع رقم حسابك هنا
        enable_page_level_ads: true
      });
    </script>
</head>
<body>
    <header>
        <h1>SmartContentAI</h1>
        <p>A global AI-powered SaaS platform for multilingual content creation, workflow automation, and more.</p>
    </header>

    <!-- أزرار رئيسية -->
    <div class="buttons">
        <a href="#features" class="button">عرض المميزات</a>
        <a href="#payment" class="button">طرق الدفع</a>
        <a href="#ai-demo" class="button">جرّب النموذج</a>
    </div>

    <!-- قسم المميزات -->
    <section id="features">
        <h2>🔑 Key Features</h2>
        <div class="features">
            <div class="card"><h3>🌐 Multilingual AI</h3><p>Create and optimize content in English, Arabic, French, Spanish, and more.</p></div>
            <div class="card"><h3>📈 SEO Optimization</h3><p>Boost visibility and ranking with integrated SEO tools.</p></div>
            <div class="card"><h3>☁️ Cloud SaaS</h3><p>Secure, scalable, and accessible anywhere, anytime.</p></div>
            <div class="card"><h3>⚡ Automation</h3><p>Streamline workflows and scale productivity.</p></div>
        </div>
    </section>

    <!-- قسم الدفع البنكي -->
    <section id="payment">
        <h2>💳 طرق الدفع البنكي</h2>
        <p>للاشتراك التجريبي (6 دولار للشهر الأول) ثم 12 دولار شهريًا:</p>
        <ul>
            <li><strong>IBAN:</strong> EG660022012880211112491757001</li>
            <li><strong>الفرع:</strong> Al Hadiqa Al Dawlia</li>
            <li><strong>الهاتف:</strong> 2</li>
            <li><strong>SWIFT:</strong> ABRKEGCAXXX</li>
        </ul>
        <form action="mailto:yourname@example.com" method="post" enctype="text/plain">
            <label for="name">الاسم الكامل:</label><br>
            <input type="text" id="name" name="name" required><br><br>
            <label for="email">البريد الإلكتروني:</label><br>
            <input type="email" id="email" name="email" required><br><br>
            <label for="message">ملاحظات أو تفاصيل التحويل:</label><br>
            <textarea id="message" name="message" rows="4" required></textarea><br><br>
            <input type="submit" value="إرسال">
        </form>
    </section>

    <!-- قسم تجربة النموذج -->
    <section id="ai-demo">
        <h2>🤖 تجربة النموذج</h2>
        <button onclick="generateContent('اكتب مقال قصير عن الذكاء الاصطناعي')">جرّب النموذج</button>
        <div id="output"></div>
    </section>

    <!-- Amazon Affiliate Example -->
    <section id="amazon">
        <h2>🛒 منتجات أمازون</h2>
        <iframe style="width:120px;height:240px;" marginwidth="0" marginheight="0" scrolling="no" frameborder="0"
        src="https://www.amazon.com/dp/B08N5WRWNW?tag=YOURAFFILIATEID-20"></iframe>
    </section>

    <footer>
        <p>©2026 SmartContentAI | Powered by AIPro</p>
    </footer>

    <!-- OpenAI API Integration -->
    <script>
    async function generateContent(prompt) {
        const response = await fetch("https://api.openai.com/v1/chat/completions", {
            method: "POST",
            headers: {
                "Content-Type": "application/json",
                "Authorization": "Bearer YOUR_API_KEY" // ضع مفتاحك هنا
            },
            body: JSON.stringify({
                model: "gpt-5",
                messages: [{role: "user", content: prompt}]
            })
        });
        const data = await response.json();
        document.getElementById("output").innerText = data.choices[0].message.content;
    }
    </script>

    <!-- ========================= -->
    <!-- Issue Templates (توثيق) -->
    <!-- ========================= -->

    <!-- bug_report.yml -->
    <!--
    name: "Bug report"
    description: "استخدم هذا النموذج للإبلاغ عن مشكلة تقنية في SmartContentAI."
    title: "[Bug] - اكتب عنوان المشكلة هنا"
    labels: ["bug"]
    -->

    <!-- feature_request.yml -->
    <!--
    name: "Feature request"
    description: "استخدم هذا النموذج لاقتراح ميزة جديدة لمشروع SmartContentAI."
    title: "[Feature] - اكتب عنوان الاقتراح هنا"
    labels: ["enhancement"]
    -->

    <!-- custom_template.yml -->
    <!--
    name: "SmartContentAI Custom Issue"
    description: "نموذج مخصص لتوثيق مشاكل الدفع أو تكامل API."
    title: "[Custom] - اكتب عنوانًا واضحًا هنا"
    labels: ["payment", "api"]
    assignees: ["drmohammedmustafa772-png"]
    -->
</body>
</html> 
