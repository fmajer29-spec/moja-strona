<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DermaClinic - Specjalistyczna Klinika Dermatologiczna</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #1a1a1a;
            background: #ffffff;
        }

        /* Navigation */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem 4rem;
            background: #ffffff;
            border-bottom: 1px solid #f0f0f0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 28px;
            font-weight: 700;
            color: #2c5f7f;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 3rem;
        }

        nav a {
            text-decoration: none;
            color: #1a1a1a;
            font-size: 15px;
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #2c5f7f;
        }

        .nav-cta {
            background: #2c5f7f;
            color: white !important;
            padding: 0.75rem 1.5rem;
            border-radius: 4px;
            transition: background 0.3s;
        }

        .nav-cta:hover {
            background: #1f4154;
            color: white;
        }

        /* Hero Section */
        .hero {
            display: grid;
            grid-template-columns: 1fr 1fr;
            align-items: center;
            padding: 4rem;
            gap: 4rem;
            min-height: 600px;
            background: linear-gradient(135deg, #f8fafb 0%, #f0f4f8 100%);
        }

        .hero-content h1 {
            font-family: 'Playfair Display', serif;
            font-size: 56px;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 1.5rem;
            color: #1a1a1a;
        }

        .hero-content p {
            font-size: 18px;
            line-height: 1.6;
            color: #666;
            margin-bottom: 2rem;
        }

        .hero-cta {
            background: #2c5f7f;
            color: white;
            padding: 1rem 2.5rem;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: background 0.3s;
            display: inline-block;
        }

        .hero-cta:hover {
            background: #1f4154;
        }

        .hero-image {
            background: url('keys/derma-hero?prompt=professional%20dermatologist%20examining%20patient%20skin%20in%20modern%20clinic%20environment&model=gemini-flash-2.5-image');
            background-size: cover;
            background-position: center;
            border-radius: 8px;
            min-height: 400px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        /* Services Section */
        .services {
            padding: 5rem 4rem;
            background: #ffffff;
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 42px;
            font-weight: 700;
            margin-bottom: 3rem;
            text-align: center;
            color: #1a1a1a;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2.5rem;
        }

        .service-card {
            padding: 2.5rem;
            background: #f8fafb;
            border-radius: 8px;
            border: 1px solid #e8ecf1;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .service-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.08);
        }

        .service-icon {
            font-size: 32px;
            margin-bottom: 1rem;
        }

        .service-card h3 {
            font-size: 20px;
            font-weight: 600;
            margin-bottom: 1rem;
            color: #1a1a1a;
        }

        .service-card p {
            font-size: 15px;
            color: #666;
            line-height: 1.6;
        }

        /* About Section */
        .about {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            padding: 5rem 4rem;
            background: #f8fafb;
            align-items: center;
        }

        .about-image {
            background: url('keys/derma-clinic?prompt=modern%20dermatology%20clinic%20interior%20with%20modern%20equipment%20and%20comfortable%20patient%20area&model=gemini-flash-2.5-image');
            background-size: cover;
            background-position: center;
            border-radius: 8px;
            min-height: 400px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .about-content h2 {
            font-family: 'Playfair Display', serif;
            font-size: 36px;
            font-weight: 700;
            margin-bottom: 1.5rem;
            color: #1a1a1a;
        }

        .about-content p {
            font-size: 16px;
            color: #666;
            margin-bottom: 1.5rem;
            line-height: 1.7;
        }

        .features-list {
            list-style: none;
        }

        .features-list li {
            padding: 0.75rem 0;
            padding-left: 2rem;
            position: relative;
            font-size: 15px;
            color: #1a1a1a;
        }

        .features-list li:before {
            content: "✓";
            position: absolute;
            left: 0;
            color: #2c5f7f;
            font-weight: bold;
            font-size: 18px;
        }

        /* CTA Section */
        .cta {
            background: linear-gradient(135deg, #2c5f7f 0%, #1f4154 100%);
            color: white;
            padding: 4rem;
            text-align: center;
            border-radius: 8px;
            margin: 5rem 4rem;
        }

        .cta h2 {
            font-family: 'Playfair Display', serif;
            font-size: 36px;
            margin-bottom: 1rem;
        }

        .cta p {
            font-size: 18px;
            margin-bottom: 2rem;
            opacity: 0.95;
        }

        .cta-button {
            background: white;
            color: #2c5f7f;
            padding: 1rem 2.5rem;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .cta-button:hover {
            transform: scale(1.05);
        }

        /* Footer */
        footer {
            background: #1a1a1a;
            color: white;
            padding: 3rem 4rem;
            text-align: center;
        }

        footer p {
            font-size: 14px;
            opacity: 0.8;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-bottom: 2rem;
            text-align: left;
        }

        .footer-section h3 {
            font-size: 16px;
            margin-bottom: 1rem;
            color: #2c5f7f;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section a {
            color: white;
            text-decoration: none;
            font-size: 14px;
            opacity: 0.8;
            transition: opacity 0.3s;
        }

        .footer-section a:hover {
            opacity: 1;
        }

        .footer-divider {
            border-top: 1px solid #333;
            padding-top: 2rem;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="logo">DermaClinic</div>
        <ul>
            <li><a href="#uslugi">Usługi</a></li>
            <li><a href="#omnie">O nas</a></li>
            <li><a href="#kontakt">Kontakt</a></li>
            <li><a href="#" class="nav-cta">Umów wizytę</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Twoja skóra w najlepszych rękach</h1>
            <p>Specjalistyczna klinika dermatologiczna z nowoczesnym zapleczem technicznym i doświadczonym zespołem lekarzy gotowych zadbać o zdrowie i urodę Twojej skóry.</p>
            <button class="hero-cta">Umów bezpłatną konsultację</button>
        </div>
        <div class="hero-image"></div>
    </section>

    <!-- Services Section -->
    <section class="services" id="uslugi">
        <h2 class="section-title">Nasze usługi</h2>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">🔬</div>
                <h3>Diagnostyka skóry</h3>
                <p>Zaawansowana diagnostyka dermatoskopowa i konsultacje specjalistyczne dla precyzyjnego określenia stanu Twojej skóry.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">💉</div>
                <h3>Zabiegi estetyczne</h3>
                <p>Nowoczesne zabiegi upiększające: botoks, kwasy, mezoterapia i zabiegi laserowe realizowane przez doświadczonych specjalistów.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🧴</div>
                <h3>Leczenie dermatologiczne</h3>
                <p>Kompleksowe leczenie problemów dermatologicznych: trądzik, łuszczyca, egzema oraz inne schorzenia skóry.</p>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="omnie">
        <div class="about-image"></div>
        <div class="about-content">
            <h2>Dlaczego my?</h2>
            <p>DermaClinic to zespół specjalistów dermatologii z ponad 15-letnim doświadczeniem w leczeniu i diagnostyce chorób skóry. Naszą misją jest zapewnienie najwyższej jakości opieki dermatologicznej w przyjaznym i nowoczesnym otoczeniu.</p>
            <ul class="features-list">
                <li>Doświadczeni dermatolodzy specjaliści</li>
                <li>Nowoczesne urządzenia diagnostyczne</li>
                <li>Indywidualne podejście do pacjenta</li>
                <li>Szybkie wizyty bez kolejek</li>
                <li>Wsparcie przed i po zabiegu</li>
                <li>Gwarancja zadowolenia pacjenta</li>
            </ul>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta" id="kontakt">
        <h2>Gotów zmienić swoją skórę?</h2>
        <p>Umów wizytę dziś i zacznij swoją transformację z DermaClinic</p>
        <button class="cta-button">Zarezerwuj wizytę</button>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>Kontakt</h3>
                <ul>
                    <li><a href="tel:+48123456789">+48 123 456 789</a></li>
                    <li><a href="mailto:info@dermaclinic.pl">info@dermaclinic.pl</a></li>
                    <li><p style="opacity: 0.8;">ul. Medyczna 5, Warszawa</p></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Godziny otwarcia</h3>
                <ul>
                    <li><p style="opacity: 0.8;">Pon-Pt: 09:00 - 19:00</p></li>
                    <li><p style="opacity: 0.8;">Sobota: 10:00 - 16:00</p></li>
                    <li><p style="opacity: 0.8;">Niedziela: Zamknięte</p></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Obserwuj nas</h3>
                <ul>
                    <li><a href="#">Facebook</a></li>
                    <li><a href="#">Instagram</a></li>
                    <li><a href="#">LinkedIn</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-divider">
            <p>&copy; 2025 DermaClinic. Wszelkie prawa zastrzeżone.</p>
        </div>
    </footer>
</body>
</html>
