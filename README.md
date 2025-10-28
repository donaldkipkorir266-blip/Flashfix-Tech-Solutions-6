# 🌐 FLASHFIXTECH SOLUTIONS

### 💡 Smart Digital Solutions That Sell

Welcome to the official landing page of **FlashfixTech Solutions** — your trusted partner for professional digital services designed to help your brand stand out globally.

---

## 🚀 About Us
**FlashfixTech Solutions** is a creative digital agency offering top-quality design, content, and web solutions.  
We combine technology and creativity to help brands grow online and attract more customers.

---

## 🛠️ Services
| Service | Description | Price (USD) |
|----------|--------------|-------------|
| Logo Design | Clean, professional branding | **$45** |
| Poster & Flyer Design | Catchy marketing visuals | **$30** |
| Website Design | Modern, responsive landing pages | **$180** |
| Social Media Content Pack | 5 posts + captions | **$60** |
| Voiceover & Editing | Audio for ads or promos | **$35** |
| SEO & Copywriting | Boost visibility & clarity | **$80** |

---

## 🖼️ Portfolio
Visit our live website to view samples of our past work.  
We specialize in **modern, neon-inspired visuals**, **digital marketing materials**, and **high-performing websites**.

---

## 💬 Contact Us
📞 **Phone:** +254 702 478 554  
💬 **WhatsApp:** [Chat Now](https://wa.me/254702478554)  
📧 **Email:** [donaldkipkorir266@gmail.com](mailto:donaldkipkorir266@gmail.com)  

---

## 🌍 Hosting
This website is proudly hosted on **[GitHub Pages](https://pages.github.com)**.  
To view the live version, visit:  
👉 **https://flashfixtech.github.io**

---
<!-- ⚡ Flashfix Payment Section Start -->
<section id="payments" style="padding:60px 20px; background:#050510; text-align:center; color:white;">
  <h2 style="font-size:2em; color:#00bfff; text-shadow:0 0 10px #00bfff;">Make a Payment</h2>
  <p style="opacity:0.8; font-size:1.1em;">Choose your preferred payment method below.</p>

  <!-- 🔹 M-Pesa Payment Box -->
  <div style="background:#0b0b20; border:1px solid #00bfff; box-shadow:0 0 20px #00bfff44; border-radius:15px; padding:25px; margin:30px auto; max-width:400px;">
    <h3 style="color:#00bfff;">Pay via M-Pesa</h3>
    <p>Send to <strong>07XXXXXXXX</strong> or use automatic STK push:</p>
    <input id="phone" type="text" placeholder="Enter phone number (07...)" style="width:90%; padding:10px; margin:8px 0; border-radius:8px; border:none; outline:none; text-align:center;">
    <input id="amount" type="number" placeholder="Enter amount (Ksh)" style="width:90%; padding:10px; margin:8px 0; border-radius:8px; border:none; outline:none; text-align:center;">
    <button id="payMpesa" style="background:#00bfff; color:white; border:none; border-radius:10px; padding:10px 20px; cursor:pointer; font-weight:bold; margin-top:10px; box-shadow:0 0 10px #00bfff;">Pay with M-Pesa</button>
    <p id="mpesa-status" style="margin-top:10px; font-size:0.9em; opacity:0.9;"></p>
  </div>

  <!-- 🔹 PayPal Payment Box -->
  <div style="background:#0b0b20; border:1px solid #00bfff; box-shadow:0 0 20px #00bfff44; border-radius:15px; padding:25px; margin:30px auto; max-width:400px;">
    <h3 style="color:#00bfff;">Pay via PayPal</h3>
    <div id="paypal-button-container"></div>
  </div>
</section>

<!-- 💰 PayPal + M-Pesa Script -->
<script src="https://www.paypal.com/sdk/js?client-id=YOUR_PAYPAL_CLIENT_ID"></script>

<script>
  // PayPal Button
  paypal.Buttons({
    style: { color: 'blue', shape: 'rect', label: 'pay' },
    createOrder: (data, actions) => actions.order.create({
      purchase_units: [{ amount: { value: '5.00' } }]
    }),
    onApprove: (data, actions) => actions.order.capture().then(details => {
      alert('✅ Payment completed by ' + details.payer.name.given_name);
    })
  }).render('#paypal-button-container');

  // M-Pesa Payment (requires backend)
  document.getElementById("payMpesa").addEventListener("click", async () => {
    const phone = document.getElementById("phone").value;
    const amount = document.getElementById("amount").value;
    const res = await fetch("/api/mpesa/stkpush", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({ phone, amount })
    });
    const data = await res.json();
    document.getElementById("mpesa-status").innerText = data.message || "Payment initiated.";
  });
</script>
<!-- ⚡ Flashfix Payment Section End -->
## 🧩 How to Edit or Customize
1. Clone or download this repository.  
2. Open `index.html` in a text editor.  
3. Replace text, services, or image URLs as needed.  
4. Commit and push changes — GitHub Pages will auto-update.

---

### ⚡ Powered by:
**HTML5**, **Bootstrap 5**, and **CSS3 (Neon Gradient Style)**  
Designed by **FlashfixTech Solutions**

---

© 2025 FlashfixTech Solutions — *Smart Digital Solutions That Sell.*
