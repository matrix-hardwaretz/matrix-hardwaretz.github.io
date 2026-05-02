Matrix Hardware

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Matrix Hardware | Premium Industrial Tools</title>
    <style>
        :root {
            --orange: #ff781f;
            --blue: #0a3d62;
            --white: #ffffff;
            --holo-gradient: linear-gradient(120deg, #00d2ff 0%, #3a7bd5 20%, #ff781f 50%, #00d2ff 100%);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Inter', sans-serif; }

        body {
            background-color: var(--white);
            /* Subtle orange accent background */
            background-image: radial-gradient(circle at top right, rgba(255, 120, 31, 0.05), transparent),
                              radial-gradient(circle at bottom left, rgba(255, 120, 31, 0.1), transparent);
            color: #333;
        }

        /* Header & Contact Bar */
        header {
            background: var(--blue);
            color: white;
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        .contact-top a {
            color: var(--orange);
            text-decoration: none;
            margin-left: 20px;
            font-weight: bold;
            font-size: 0.9rem;
        }

        /* Hero Section */
        .hero {
            height: 60vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            background: white;
            border-bottom: 5px solid var(--orange);
        }

        /* Holographic Logo */
        .matrix-logo {
            font-size: clamp(2.5rem, 10vw, 6rem);
            font-weight: 900;
            text-transform: uppercase;
            background: var(--holo-gradient);
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: holo-flow 4s linear infinite;
            filter: drop-shadow(0px 5px 15px rgba(10, 61, 98, 0.2));
            letter-spacing: -2px;
        }

        @keyframes holo-flow {
            0% { background-position: 0% center; }
            100% { background-position: 200% center; }
        }

        /* Product Grid */
        .shop-container {
            max-width: 1200px;
            margin: -50px auto 50px;
            padding: 0 20px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .tool-card {
            background: white;
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            border: 1px solid #eee;
            transition: transform 0.3s ease;
        }

        .tool-card:hover {
            transform: translateY(-10px);
            border-color: var(--orange);
        }

        .tool-img {
            width: 100%;
            height: 200px;
            object-fit: contain;
            background: #f9f9f9;
            border-radius: 10px;
            margin-bottom: 15px;
        }

        .price-tag {
            display: block;
            font-size: 1.4rem;
            font-weight: 800;
            color: var(--blue);
            margin: 10px 0;
        }

        .tool-name {
            font-weight: 600;
            color: #555;
            min-height: 50px;
        }

        .btn-buy {
            background: var(--orange);
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            display: inline-block;
            margin-top: 10px;
            font-weight: bold;
        }

        /* Mobile View */
        @media (max-width: 768px) {
            header { flex-direction: column; gap: 10px; }
            .contact-top { display: flex; flex-direction: column; align-items: center; gap: 5px; }
            .matrix-logo { font-size: 3rem; }
            .hero { height: 40vh; }
        }
    </style>
</head>
<body>

    <header>
        <div style="font-weight: 900; letter-spacing: 1px;">MATRIX<span style="color:var(--orange)">.</span></div>
        <div class="contact-top">
            <a href="mailto:ajoamko@yahoo.com">ajoamko@yahoo.com</a>
            <a href="tel:+255652717647">+255 652 717 647</a>
        </div>
    </header>

    <section class="hero">
        <h1 class="matrix-logo">MATRIX HARDWARE</h1>
    </section>

    <main class="shop-container">
        <div class="grid">
            <div class="tool-card">
                <img src="https://images.unsplash.com/photo-1504148455328-c376907d081c?auto=format&fit=crop&w=400&q=80" alt="Drill" class="tool-img">
                <p class="tool-name">Impact Drill Machine 1010W</p>
                <span class="price-tag">TZS 172,000</span>
                <a href="tel:+255652717647" class="btn-buy">Call to Order</a>
            </div>

            <div class="tool-card">
                <img src="https://images.unsplash.com/photo-1581147036324-c17ac41dfa6c?auto=format&fit=crop&w=400&q=80" alt="Grinder" class="tool-img">
                <p class="tool-name">Angle Grinder 115mm Professional</p>
                <span class="price-tag">TZS 120,000</span>
                <a href="tel:+255652717647" class="btn-buy">Call to Order</a>
            </div>

            <div class="tool-card">
                <img src="https://images.unsplash.com/photo-1530124560676-46c55981440d?auto=format&fit=crop&w=400&q=80" alt="Screwdriver" class="tool-img">
                <p class="tool-name">Insulated Screwdriver Set (2pcs)</p>
                <span class="price-tag">TZS 12,500</span>
                <a href="tel:+255652717647" class="btn-buy">Call to Order</a>
            </div>

            <div class="tool-card">
                <img src="https://images.unsplash.com/photo-1586864387418-f39393f3e2c6?auto=format&fit=crop&w=400&q=80" alt="Saw" class="tool-img">
                <p class="tool-name">Hardened Teeth Hand Saw 20"</p>
                <span class="price-tag">TZS 19,500</span>
                <a href="tel:+255652717647" class="btn-buy">Call to Order</a>
            </div>
        </div>
    </main>

    <footer style="text-align: center; padding: 40px; 
