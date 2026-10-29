
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>La Bella | Fine Dining Restaurant</title>

    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            color: #333;
            line-height: 1.7;
        }

        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
        }

        header {
            background: #211b18;
            color: white;
            padding: 18px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .logo {
            color: #d9ae70;
            font-size: 28px;
            font-weight: bold;
            font-family: 'Playfair Display', serif;
        }

        nav {
            display: flex;
            gap: 22px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-size: 14px;
        }

        nav a:hover {
            color: #d9ae70;
        }

        .hero {
            min-height: 85vh;
            background: linear-gradient(#0007, #0008),
            url('https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&w=1800&q=85')
            center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding: 40px 20px;
        }

        .hero h1 {
            font-size: clamp(38px, 6vw, 68px);
            margin-bottom: 15px;
        }

        .hero p {
            font-size: 17px;
            margin-bottom: 28px;
        }

        .btn {
            display: inline-block;
            padding: 12px 26px;
            background: #b88650;
            color: white;
            text-decoration: none;
            border: none;
            cursor: pointer;
            font: inherit;
            transition: 0.3s;
        }

        .btn:hover {
            background: #8e6338;
        }

        section {
            padding: 75px 8%;
            text-align: center;
            scroll-margin-top: 75px;
        }

        .section-title {
            font-size: 38px;
            margin-bottom: 12px;
            color: #30231c;
        }

        .subtitle {
            color: #777;
            margin-bottom: 35px;
        }

        .menu-grid, .chef-grid, .gallery-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
            margin-top: 30px;
        }

        .card {
            background: #fffaf4;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 15px #00000010;
            text-align: left;
        }

        .card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            display: block;
        }

        .card-content {
            padding: 20px;
        }

        .card h3 {
            margin-bottom: 8px;
            font-size: 22px;
        }

        .price {
            color: #a16c37;
            font-weight: 600;
            margin-top: 10px;
        }

        .chefs {
            background: #f8f2eb;
        }

        .gallery-grid {
            grid-template-columns: repeat(3, 1fr);
        }

        .gallery-grid img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
        }

        .testimonials {
            background: #30231c;
            color: white;
        }

        .testimonials .section-title {
            color: #e4c18f;
        }

        .review {
            max-width: 700px;
            margin: 20px auto;
            font-size: 17px;
            font-style: italic;
        }

        .review h3 {
            margin-top: 15px;
            font-style: normal;
            color: #e4c18f;
        }

        .info-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 35px;
            text-align: left;
            margin-top: 35px;
        }

        .info-box {
            background: #fffaf4;
            padding: 28px;
            border-radius: 8px;
        }

        .info-box h3 {
            margin-bottom: 15px;
            color: #a16c37;
        }

        form {
            max-width: 650px;
            margin: 30px auto 0;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            text-align: left;
        }

        input, select, textarea {
            width: 100%;
            padding: 13px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font: inherit;
        }

        textarea {
            grid-column: 1 / -1;
            resize: vertical;
        }

        form button {
            grid-column: 1 / -1;
        }

        .form-message {
            grid-column: 1 / -1;
            color: #276738;
            text-align: center;
        }

        footer {
            background: #211b18;
            color: white;
            text-align: center;
            padding: 25px;
        }

        @media (max-width: 850px) {
            .menu-grid, .chef-grid, .gallery-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            nav {
                gap: 12px;
            }

            header {
                padding: 16px 4%;
            }
        }

        @media (max-width: 600px) {
            header {
                flex-direction: column;
                gap: 12px;
            }

            nav {
                justify-content: center;
                flex-wrap: wrap;
                gap: 10px 15px;
            }

            nav a {
                font-size: 12px;
            }

            section {
                padding: 50px 6%;
            }

            .section-title {
                font-size: 30px;
            }

            .menu-grid, .chef-grid, .gallery-grid,
            .info-grid, form {
                grid-template-columns: 1fr;
            }

            textarea, form button, .form-message {
                grid-column: auto;
            }

            .hero {
                min-height: 70vh;
            }
        }
    </style>
</head>

<body>

<header>
    <div class="logo">La Bella.</div>
    <nav>
        <a href="#home">Home</a>
        <a href="#menu">Menu</a>
        <a href="#chefs">Our Chefs</a>
        <a href="#ambience">Ambience</a>
        <a href="#reviews">Reviews</a>
        <a href="#contact">Contact</a>
        <a href="#reservation">Reserve</a>
    </nav>
</header>

<!-- HERO SECTION -->
<section class="hero" id="home">
    <div>
        <h1>Good Food, Beautiful Moments</h1>
        <p>Experience exceptional flavours in an elegant atmosphere.</p>
        <a href="#menu" class="btn">Explore Our Menu</a>
        <a href="#reservation" class="btn">Book a Table</a>
    </div>
</section>

<!-- MENU SECTION -->
<section id="menu">
    <h2 class="section-title">Our Special Menu</h2>
    <p class="subtitle">Fresh ingredients. Memorable flavours.</p>

    <div class="menu-grid">
        <div class="card">
            <img src="https://images.unsplash.com/photo-1547592180-85f173990554?auto=format&fit=crop&w=800&q=80" alt="Fresh garden salad">
            <div class="card-content">
                <h3>Garden Fresh Salad</h3>
                <p>Crisp greens, fresh vegetables and house dressing.</p>
                <p class="price">₹249</p>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1473093295043-cdd812d0e601?auto=format&fit=crop&w=800&q=80" alt="Italian pasta">
            <div class="card-content">
                <h3>Creamy Italian Pasta</h3>
                <p>Rich creamy sauce, herbs and parmesan flavour.</p>
                <p class="price">₹349</p>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?auto=format&fit=crop&w=800&q=80" alt="Freshly baked pizza">
            <div class="card-content">
                <h3>Signature Pizza</h3>
                <p>Stone-baked pizza with cheese and fresh toppings.</p>
                <p class="price">₹399</p>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1546833999-b9f581a1996d?auto=format&fit=crop&w=800&q=80" alt="Indian curry">
            <div class="card-content">
                <h3>Royal Indian Curry</h3>
                <p>Traditional spices with a rich, aromatic gravy.</p>
                <p class="price">₹299</p>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1563805042-7684c019e1cb?auto=format&fit=crop&w=800&q=80" alt="Ice cream dessert">
            <div class="card-content">
                <h3>Classic Ice Cream</h3>
                <p>A deliciously smooth and refreshing dessert.</p>
                <p class="price">₹149</p>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1517701604599-bb29b565090c?auto=format&fit=crop&w=800&q=80" alt="Coffee">
            <div class="card-content">
                <h3>Signature Coffee</h3>
                <p>Freshly brewed coffee with a rich aroma.</p>
                <p class="price">₹129</p>
            </div>
        </div>
    </div>
</section>

<!-- CHEF PROFILES -->
<section class="chefs" id="chefs">
    <h2 class="section-title">Meet Our Chefs</h2>
    <p class="subtitle">Passion and expertise behind every plate.</p>

    <div class="chef-grid">
        <div class="card">
            <img src="https://images.unsplash.com/photo-1577219491135-ce391730fb2c?auto=format&fit=crop&w=800&q=80" alt="Head chef">
            <div class="card-content">
                <h3>Chef Alessandro</h3>
                <p>Head Chef — Italian cuisine and modern fine dining.</p>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1583394293214-28ded15ee548?auto=format&fit=crop&w=800&q=80" alt="Executive chef">
            <div class="card-content">
                <h3>Chef Meera</h3>
                <p>Executive Chef — Indian flavours and seasonal dishes.</p>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1581299894007-aaa50297cf16?auto=format&fit=crop&w=800&q=80" alt="Pastry chef">
            <div class="card-content">
                <h3>Chef Daniel</h3>
                <p>Pastry Chef — Desserts, pastries and sweet creations.</p>
            </div>
        </div>
    </div>
</section>

<!-- RESTAURANT AMBIENCE -->
<section id="ambience">
    <h2 class="section-title">Our Ambience</h2>
    <p class="subtitle">A warm and elegant setting for every occasion.</p>

    <div class="gallery-grid">
        <img src="https://images.unsplash.com/photo-1414235077428-338989a2e8c0?auto=format&fit=crop&w=800&q=80" alt="Elegant dining tables">
        <img src="https://images.unsplash.com/photo-1515003197210-e0cd7184f8b5?auto=format&fit=crop&w=800&q=80" alt="Restaurant dining experience">
        <img src="https://images.unsplash.com/photo-1514933651103-005eec06c04b?auto=format&fit=crop&w=800&q=80" alt="Warm restaurant interior">
    </div>
</section>

<!-- CUSTOMER TESTIMONIALS -->
<section class="testimonials" id="reviews">
    <h2 class="section-title">What Our Guests Say</h2>

    <div class="review">
        <p>"Beautiful ambience, delicious food and wonderful service. A lovely place for dinner."</p>
        <h3>— Ananya R.</h3>
    </div>

    <div class="review">
        <p>"The pasta was excellent, and the staff made our evening feel special."</p>
        <h3>— Rahul M.</h3>
    </div>

    <div class="review">
        <p>"A comfortable atmosphere, great desserts and a memorable dining experience."</p>
        <h3>— Priya S.</h3>
    </div>
</section>

<!-- HOURS AND LOCATION -->
<section id="contact">
    <h2 class="section-title">Visit Us</h2>
    <p class="subtitle">We look forward to welcoming you.</p>

    <div class="info-grid">
        <div class="info-box">
            <h3>Opening Hours</h3>
            <p>Monday – Friday: 12:00 PM – 10:30 PM</p>
            <p>Saturday – Sunday: 11:00 AM – 11:00 PM</p>
            <p>Public holidays: Please call ahead.</p>
        </div>

        <div class="info-box">
            <h3>Location Details</h3>
            <p>La Bella Restaurant</p>
            <p>MG Road, Vijayawada, Andhra Pradesh, India</p>
            <p>Email: hello@labella.example</p>
            <p>Phone: +91 98765 43210</p>
            <p><a href="https://www.google.com/maps/search/?api=1&query=restaurants+MG+Road+Vijayawada" target="_blank" rel="noopener">Find us on Google Maps</a></p>
        </div>
    </div>
</section>

<!-- TABLE RESERVATION -->
<section id="reservation">
    <h2 class="section-title">Reserve Your Table</h2>
    <p class="subtitle">Plan your next memorable dining experience.</p>

    <form id="reservationForm">
        <input type="text" name="name" placeholder="Your Full Name" required>

        <input type="email" name="email" placeholder="Your Email Address" required>

        <input type="tel" name="phone" placeholder="Phone Number"
               pattern="[0-9+() -]{7,20}" required>

        <select name="guests" required>
            <option value="">Number of Guests</option>
            <option value="1">1 Guest</option>
            <option value="2">2 Guests</option>
            <option value="3">3 Guests</option>
            <option value="4">4 Guests</option>
            <option value="5">5 Guests</option>
            <option value="6">6 Guests</option>
            <option value="7+">7 or More Guests</option>
        </select>

        <input type="date" name="date" id="reservationDate" required>

        <select name="time" required>
            <option value="">Select Time</option>
            <option>12:00 PM</option>
            <option>1:00 PM</option>
            <option>2:00 PM</option>
            <option>6:00 PM</option>
            <option>7:00 PM</option>
            <option>8:00 PM</option>
            <option>9:00 PM</option>
            <option>10:00 PM</option>
        </select>

        <textarea name="message" rows="4"
                  placeholder="Special requests (optional)"></textarea>

        <button type="submit" class="btn">Request a Reservation</button>

        <p id="formMessage" class="form-message" role="status"
           aria-live="polite"></p>
    </form>
</section>

<footer>
    <p>© 2026 La Bella Restaurant. All rights reserved.</p>
    <p>Good food. Great company. Beautiful memories.</p>
</footer>

<script>
    const dateInput = document.getElementById("reservationDate");
    const today = new Date();
    const localToday = [
        today.getFullYear(),
        String(today.getMonth() + 1).padStart(2, "0"),
        String(today.getDate()).padStart(2, "0")
    ].join("-");

    dateInput.min = localToday;

    document.getElementById("reservationForm").addEventListener("submit", function(event) {
        event.preventDefault();

        const formMessage = document.getElementById("formMessage");

        formMessage.textContent =
            "Demo only: your form is filled in, but no reservation has been sent. Connect a booking service or backend to confirm your table.";

        this.reset();
        dateInput.min = localToday;
    });
</script>

</body>
</html>
