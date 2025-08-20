# 247-max-courier
Legit Courier website!
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>24/7 Max Courier</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; }
    header { background: #222; color: #fff; padding: 20px; text-align: center; }
    nav a { color: #fff; margin: 0 15px; text-decoration: none; font-weight: bold; }
    nav a:hover { text-decoration: underline; }
    section { padding: 40px 20px; max-width: 900px; margin: auto; }
    .hero { background: url('https://images.unsplash.com/photo-1600488994928-88f6f8b1d9b6?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') center/cover; color: white; padding: 100px 20px; text-align: center; }
    .hero h1 { font-size: 3em; }
    .services { display: flex; gap: 20px; flex-wrap: wrap; }
    .service { flex: 1; background: #f4f4f4; padding: 20px; border-radius: 8px; min-width: 250px; }
    footer { background: #222; color: white; text-align: center; padding: 15px; margin-top: 30px; }
    form input, form textarea { width: 100%; padding: 10px; margin: 10px 0; }
    form button { background: #222; color: white; padding: 10px 20px; border: none; cursor: pointer; }
    form button:hover { background: #444; }
    #chat-box { border: 1px solid #ccc; height: 200px; overflow-y: auto; padding: 10px; background: #fafafa; margin-bottom: 10px; }
    #chat-input { display: flex; }
    #chat-input input { flex: 1; padding: 10px; }
    #chat-input button { padding: 10px; background: #222; color: #fff; border: none; cursor: pointer; }
    #chat-input button:hover { background: #444; }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <h1>Welcome to 24/7 Max Courier</h1>
    <h2>Your trusted partner in nationwide delivery services</h2>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#track">Track</a>
      <a href="#chat">Chat</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- Hero Section -->
  <section class="hero" id="home">
    <h1>Fast. Reliable. 24/7.</h1>
    <p>Courier solutions that keep your business and life moving.</p>
  </section>

  <!-- About Section -->
  <section id="about">
    <h2>About Us</h2>
    <p>
      At <b>24/7 Max Courier</b>, we provide fast, secure, and reliable delivery services.
      Whether it’s food, parcels, or urgent same-day deliveries, our mission is to get it done — anytime, anywhere.
    </p>
  </section>

  <!-- Services Section -->
  <section id="services">
    <h2>Our Services</h2>
    <div class="services">
      <div class="service">
        <h3>Express Delivery</h3>
        <p>Same-day and urgent deliveries with real-time tracking.</p>
      </div>
      <div class="service">
        <h3>Food & Grocery</h3>
        <p>Fast delivery from restaurants, supermarkets, and stores.</p>
      </div>
      <div class="service">
        <h3>Parcel Delivery</h3>
        <p>Safe and secure parcel delivery to your destination.</p>
      </div>
    </div>
  </section>

  <!-- Tracking Section -->
  <section id="track">
    <h2>Track Your Package</h2>
    <form onsubmit="fakeTracking(event)">
      <input type="text" id="trackingNumber" placeholder="Enter Tracking Number" required>
      <button type="submit">Track</button>
    </form>
    <p id="trackingResult"></p>
  </section>

  <!-- Chat Section -->
  <section id="chat">
    <h2>Customer Chat Support (Demo)</h2>
    <div id="chat-box"></div>
    <div id="chat-input">
      <input type="text" id="chatMessage" placeholder="Type your message...">
      <button onclick="sendMessage()">Send</button>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact">
    <h2>Contact Us</h2>
    <p>Email: info@247maxcourier.com | Phone: +234 800 247 0000</p>
    <form>
      <input type="text" placeholder="Your Name" required>
      <input type="email" placeholder="Your Email" required>
      <textarea placeholder="Your Message" rows="5"></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 24/7 Max Courier. All rights reserved.</p>
  </footer>

  <!-- JavaScript for Demo Functions -->
  <script>
    // Fake Tracking
    function fakeTracking(event) {
      event.preventDefault();
      const number = document.getElementById("trackingNumber").value;
      document.getElementById("trackingResult").innerText =
        "Tracking Number " + number + " is currently IN TRANSIT (Demo Only)";
    }

    // Fake Chat
    function sendMessage() {
      const input = document.getElementById("chatMessage");
      const chatBox = document.getElementById("chat-box");
      if (input.value.trim() !== "") {
        const userMessage = document.createElement("p");
        userMessage.textContent = "You: " + input.value;
        chatBox.appendChild(userMessage);

        // Auto fake reply
        const botMessage = document.createElement("p");
        botMessage.textContent = "Agent: Thanks for contacting us! (Demo Only)";
        chatBox.appendChild(botMessage);

        input.value = "";
        chatBox.scrollTop = chatBox.scrollHeight;
      }
    }
  </script>

</body>
</html>
