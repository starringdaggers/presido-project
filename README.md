<!doctype.html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Presido Store | Fashion, Frames & More</title>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary-blue: #0A2540;
      --accent-blue: #1E4F7C;
      --light-blue: #E8F1F5;
      --cream-bg: #FAF7F2;
      --cream-card: #FFFFFF;
      --text-dark: #1A202C;
      --text-muted: #4A5568;
      --whatsapp-green: #25D366;
      --whatsapp-hover: #20bd5a;
      --shadow-sm: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
      --shadow-lg: 0 10px 25px -5px rgba(10, 37, 64, 0.1);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Plus Jakarta Sans', sans-serif;
    }

    body {
      background-color: var(--cream-bg);
      color: var(--text-dark);
      line-height: 1.6;
    }

    /* Navigation */
    header {
      background-color: var(--primary-blue);
      padding: 18px 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 4px 20px rgba(0,0,0,0.15);
    }

    .logo {
      font-size: 24px;
      font-weight: 800;
      color: var(--cream-bg);
      letter-spacing: 0.5px;
    }

    .logo span {
      color: #93C5FD;
      font-weight: 400;
    }

    .header-wa-btn {
      background-color: var(--whatsapp-green);
      color: #FFFFFF;
      padding: 10px 20px;
      border-radius: 30px;
      text-decoration: none;
      font-weight: 600;
      font-size: 14px;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: all 0.2s ease;
    }

    .header-wa-btn:hover {
      background-color: var(--whatsapp-hover);
      transform: translateY(-1px);
    }

    /* Hero Section */
    .hero {
      background: linear-gradient(135deg, var(--primary-blue) 0%, var(--accent-blue) 100%);
      color: #FFFFFF;
      padding: 80px 8% 100px;
      text-align: center;
      position: relative;
    }

    .hero h1 {
      font-size: 42px;
      font-weight: 800;
      margin-bottom: 18px;
      line-height: 1.2;
    }

    .hero p {
      font-size: 18px;
      max-width: 650px;
      margin: 0 auto 30px;
      color: #E2E8F0;
      font-weight: 400;
    }

    .hero-btn {
      display: inline-block;
      background-color: var(--cream-bg);
      color: var(--primary-blue);
      padding: 14px 32px;
      border-radius: 30px;
      font-weight: 700;
      text-decoration: none;
      transition: all 0.2s ease;
      box-shadow: var(--shadow-lg);
    }

    .hero-btn:hover {
      background-color: #FFFFFF;
      transform: translateY(-2px);
    }

    /* Main Container */
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 5%;
    }

    /* About Section */
    .about-card {
      background: var(--cream-card);
      margin-top: -50px;
      padding: 40px;
      border-radius: 16px;
      box-shadow: var(--shadow-lg);
      text-align: center;
      position: relative;
      z-index: 10;
      border: 1px solid rgba(10, 37, 64, 0.05);
    }

    .about-card h2 {
      color: var(--primary-blue);
      font-size: 26px;
      font-weight: 700;
      margin-bottom: 12px;
    }

    .about-card p {
      color: var(--text-muted);
      max-width: 750px;
      margin: 0 auto;
      font-size: 16px;
    }

    /* Products Section */
    .products-section {
      padding: 70px 0;
    }

    .section-title {
      text-align: center;
      color: var(--primary-blue);
      font-size: 32px;
      font-weight: 800;
      margin-bottom: 40px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 30px;
    }

    .card {
      background-color: var(--cream-card);
      border-radius: 16px;
      overflow: hidden;
      box-shadow: var(--shadow-sm);
      border: 1px solid rgba(10, 37, 64, 0.06);
      transition: all 0.3s ease;
      display: flex;
      flex-direction: column;
    }

    .card:hover {
      transform: translateY(-8px);
      box-shadow: var(--shadow-lg);
    }

    .card-img-wrapper {
      width: 100%;
      height: 220px;
      overflow: hidden;
      position: relative;
    }

    .card-img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.4s ease;
    }

    .card:hover .card-img {
      transform: scale(1.06);
    }

    .card-body {
      padding: 24px;
      display: flex;
      flex-direction: column;
      flex-grow: 1;
    }

    .card-title {
      color: var(--primary-blue);
      font-size: 20px;
      font-weight: 700;
      margin-bottom: 10px;
    }

    .card-desc {
      color: var(--text-muted);
      font-size: 14px;
      margin-bottom: 24px;
      flex-grow: 1;
    }

    .order-btn {
      display: block;
      width: 100%;
      text-align: center;
      padding: 12px;
      background-color: var(--primary-blue);
      color: #FFFFFF;
      text-decoration: none;
      border-radius: 8px;
      font-weight: 600;
      font-size: 14px;
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
      padding: 40px 5%;
      margin-top: 40px;
    }

    footer p {
      margin-bottom: 8px;
      font-size: 15px;
    }

    .wa-link {
      color: #93C5FD;
      text-decoration: none;
      font-weight: 700;
    }

    .wa-link:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="logo">PRESIDO <span>STORE</span></div>
    <a href="https://wa.me/2348125255158" target="_blank" class="header-wa-btn">
      💬 Chat on WhatsApp
    </a>
  </header>

  <!-- Hero Section -->
  <section class="hero">
    <h1>Quality Fashion & Unique Gifts</h1>
    <p>Discover top-tier clothing, footwear, and personalized birthday frames designed for your special moments.</p>
    <a href="https://wa.me/2348125255158?text=Hello%20Presido%20Store,%20I%20want%20to%20make%20an%20inquiry" target="_blank" class="hero-btn">Start Shopping Now</a>
  </section>

  <div class="container">
    <!-- About Card -->
    <div class="about-card">
      <h2>Welcome to Presido Store</h2>
      <p>We supply general merchandise across high-demand categories! Whether you are looking for stylish outfits, long-lasting footwear, or customized picture frames for birthdays and events, we deliver value directly to your location.</p>
    </div>

    <!-- Product Grid -->
    <section class="products-section">
      <h2 class="section-title">Explore Categories</h2>
      <div class="grid">
        
        <!-- Fashion Category -->
        <div class="card">
          <div class="card-img-wrapper">
            <img src="https://images.unsplash.com/photo-1489987707025-afc232f7ea0f?auto=format&fit=crop&w=600&q=80" alt="Clothing Category" class="card-img">
          </div>
          <div class="card-body">
            <h3 class="card-title">Trendy Clothing</h3>
            <p class="card-desc">Quality outfits, corporate attire, hoodies, and casual fashion items tailored to keep you looking sharp.</p>
            <a href="https://wa.me/2348125255158?text=Hello%20Presido%20Store,%20I%20am%20interested%20in%20buying%20Clothes" target="_blank" class="order-btn">Order via WhatsApp</a>
          </div>
        </div>

        <!-- Footwear Category -->
        <div class="card">
          <div class="card-img-wrapper">
            <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=600&q=80" alt="Shoes Category" class="card-img">
          </div>
          <div class="card-body">
            <h3 class="card-title">Shoes & Footwear</h3>
            <p class="card-desc">Stylish sneakers, corporate leather shoes, sliders, and sandals for comfort and long-lasting wear.</p>
            <a href="https://wa.me/2348125255158?text=Hello%20Presido%20Store,%20I%20am%20interested%20in%20buying%20Shoes" target="_blank" class="order-btn">Order via WhatsApp</a>
          </div>
        </div>

        <!-- Birthday Frames Category -->
        <div class="card">
          <div class="card-img-wrapper">
            <img src="https://images.unsplash.com/photo-1513519245088-0e12902e5a38?auto=format&fit=crop&w=600&q=80" alt="Birthday Frame Category" class="card-img">
          </div>
          <div class="card-body">
            <h3 class="card-title">Birthday & Picture Frames</h3>
            <p class="card-desc">Custom photo frames, birthday portrait designs, and memorable frame gifts crafted with care.</p>
            <a href="https://wa.me/2348125255158?text=Hello%20Presido%20Store,%20I%20want%20to%20order%20a%20Birthday%20Frame" target="_blank" class="order-btn">Order via WhatsApp</a>
          </div>
        </div>

        <!-- General Merchandise Category -->
        <div class="card">
          <div class="card-img-wrapper">
            <img src="https://images.unsplash.com/photo-1472851294608-062f824d29cc?auto=format&fit=crop&w=600&q=80" alt="General Goods Category" class="card-img">
          </div>
          <div class="card-body">
            <h3 class="card-title">General Merchandise</h3>
            <p class="card-desc">Searching for a specific product? Contact us directly to make inquiries or place special orders.</p>
            <a href="https://wa.me/2348125255158?text=Hello%20Presido%20Store,%20I%20have%20an%20inquiry%20about%20your%20products" target="_blank" class="order-btn">Order via WhatsApp</a>
          </div>
        </div>

      </div>
    </section>
  </div>

  <!-- Footer -->
  <footer>
    <p><strong>Presido Store</strong> — Quality & Reliability Delivered</p>
    <p>Phone / WhatsApp: <a href="https://wa.me/2348125255158" class="wa-link">08125255158</a></p>
  </footer>

</body>
</html>
