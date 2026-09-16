<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Presido Collections | Online Store</title>
  <style>
    :root {
      --primary-blue: #0A2540;
      --accent-blue: #1A4971;
      --cream-bg: #FDFBF7;
      --cream-card: #F5EFEB;
      --text-dark: #2C3E50;
      --white: #FFFFFF;
      --whatsapp-green: #25D366;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: var(--cream-bg);
      color: var(--text-dark);
    }

    /* Header & Navigation */
    header {
      background-color: var(--primary-blue);
      padding: 20px 5%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    .logo {
      font-size: 26px;
      font-weight: 800;
      color: var(--cream-bg);
      letter-spacing: 1px;
    }

    .logo span {
      color: #90CAF9;
      font-weight: 300;
    }

    .contact-btn {
      background-color: var(--whatsapp-green);
      color: var(--white);
      padding: 10px 18px;
      border-radius: 20px;
      text-decoration: none;
      font-weight: 600;
      font-size: 14px;
    }

    /* Hero Section */
    .hero {
      background-color: var(--cream-card);
      padding: 60px 5%;
      text-align: center;
      border-bottom: 1px solid rgba(10, 37, 64, 0.08);
    }

    .hero h1 {
      color: var(--primary-blue);
      font-size: 36px;
      margin-bottom: 15px;
    }

    .hero p {
      font-size: 18px;
      max-width: 600px;
      margin: 0 auto 25px;
      color: var(--text-dark);
    }

    /* About Section */
    .about-section {
      padding: 40px 5%;
      background-color: var(--white);
      text-align: center;
    }

    .about-section h2 {
      color: var(--primary-blue);
      margin-bottom: 15px;
    }

    .about-section p {
      max-width: 700px;
      margin: 0 auto;
      line-height: 1.6;
    }

    /* Products Grid */
    .products-container {
      padding: 50px 5%;
    }

    .section-title {
      text-align: center;
      color: var(--primary-blue);
      font-size: 28px;
      margin-bottom: 30px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
    }

    .card {
      background-color: var(--cream-card);
      border-radius: 12px;
      padding: 20px;
      text-align: center;
      border: 1px solid rgba(10, 37, 64, 0.08);
      box-shadow: 0 4px 12px rgba(10, 37, 64, 0.05);
      transition: transform 0.2s;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card-icon {
      font-size: 40px;
      margin-bottom: 15px;
    }

    .card h3 {
      color: var(--primary-blue);
      margin-bottom: 10px;
    }

    .card p {
      font-size: 14px;
      margin-bottom: 20px;
      color: #555;
    }

    .order-btn {
      display: inline-block;
      width: 100%;
      padding: 12px;
      background-color: var(--primary-blue);
      color: var(--cream-bg);
      text-decoration: none;
      border-radius: 6px;
      font-weight: 600;
      transition: background-color 0.2s;
    }

    .order-btn:hover {
      background-color: var(--accent-blue);
    }

    /* Footer */
    footer {
      background-color: var(--primary-blue);
      color: var(--cream-bg);
      text-align: center;
      padding: 30px 5%;
      margin-top: 40px;
    }

    footer p {
      margin-bottom: 10px;
    }

    .whatsapp-link {
      color: #90CAF9;
      text-decoration: none;
      font-weight: 600;
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="logo">PRESIDO <span>STORE</span></div>
    <a href="https://wa.me/2348125255158" target="_blank" class="contact-btn">WhatsApp Us</a>
  </header>

  <!-- Hero Banner -->
  <section class="hero">
    <h1>Your One-Stop Shop for Everything Style & Gifts</h1>
    <p>Quality fashion items, custom birthday frames, footwear, and general merchandise delivered to your doorstep.</p>
    <a href="https://wa.me/2348125255158?text=Hello,%20I%20want%20to%20make%20an%20inquiry" target="_blank" class="order-btn" style="width: auto; padding: 12px 30px;">Chat on WhatsApp</a>
  </section>

  <!-- About Section -->
  <section class="about-section">
    <h2>About Us</h2>
    <p>We deal in all kinds of general merchandise! From trendy clothing and comfortable shoes to customized birthday frames and special gifts. We bring quality directly to you at affordable prices.</p>
  </section>

  <!-- Products Section -->
  <section class="products-container">
    <h2 class="section-title">Our Categories</h2>
    <div class="grid">
      
      <!-- Clothing -->
      <div class="card">
        <div class="card-icon">👗</div>
        <h3>Quality Clothing</h3>
        <p>Trendy outfits, corporate wear, casual clothes, and stylish fashion items for all occasions.</p>
        <a href="https://wa.me/2348125255158?text=Hello,%20I%20want%20to%20buy%20Clothes" target="_blank" class="order-btn">Order via WhatsApp</a>
      </div>

      <!-- Shoes -->
      <div class="card">
        <div class="card-icon">👟</div>
        <h3>Shoes & Footwear</h3>
        <p>Sneakers, heels, sandals, and formal shoes built for comfort and durability.</p>
        <a href="https://wa.me/2348125255158?text=Hello,%20I%20want%20to%20buy%20Shoes" target="_blank" class="order-btn">Order via WhatsApp</a>
      </div>

      <!-- Birthday Frames -->
      <div class="card">
        <div class="card-icon">🖼️</div>
        <h3>Birthday & Photo Frames</h3>
        <p>Customized picture frames, birthday design frames, and memorable photo gifts.</p>
        <a href="https://wa.me/2348125255158?text=Hello,%20I%20want%20to%20order%20a%20Birthday%20Frame" target="_blank" class="order-btn">Order via WhatsApp</a>
      </div>

      <!-- General Items -->
      <div class="card">
        <div class="card-icon">🛍️</div>
        <h3>General Merchandise</h3>
        <p>Looking for something specific? Contact us directly to place custom orders.</p>
        <a href="https://wa.me/2348125255158?text=Hello,%20I%20want%20to%20inquire%20about%20your%20products" target="_blank" class="order-btn">Order via WhatsApp</a>
      </div>

    </div>
  </section>

  <!-- Footer -->
  <footer>
    <p><strong>Presido Store</strong> — Quality & Reliability Guaranteed</p>
    <p>Phone / WhatsApp: <a href="https://wa.me/2348125255158" class="whatsapp-link">08125255158</a></p>
  </footer>

</body>
</html>
