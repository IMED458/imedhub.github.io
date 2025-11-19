<html lang="en">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>IMED Hub - Clinic Tools Portal</title>
  <script src="/_sdk/element_sdk.js"></script>
  <style>
        body {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
            min-height: 100vh;
            color: #1e293b;
            line-height: 1.6;
        }
        html {
            height: 100%;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }
        /* Hero Section */
        .hero {
            text-align: center;
            padding: 4rem 0;
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 0.8s ease-out forwards;
        }
        .hero h1 {
            font-size: 3.5rem;
            font-weight: 700;
            margin: 0 0 1rem 0;
            background: linear-gradient(135deg, #0ea5e9 0%, #06b6d4 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 2px 4px rgba(6, 182, 212, 0.2);
        }
        .hero .subtitle-ka {
            font-size: 1.25rem;
            color: #475569;
            margin: 0 0 0.5rem 0;
            font-weight: 500;
        }
        .hero .subtitle-en {
            font-size: 1.125rem;
            color: #64748b;
            margin: 0 0 1rem 0;
        }
        .logo-container {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }
        .logo-placeholder {
            width: 80px;
            height: 80px;
            border-radius: 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(14, 165, 233, 0.3);
        }
        .logo-image {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
        /* Links Section */
        .links-section {
            flex: 1;
            padding: 2rem 0;
        }
        .section-title {
            text-align: center;
            font-size: 2rem;
            font-weight: 600;
            margin: 0 0 3rem 0;
            color: #1e293b;
            text-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
        }
        .cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 800px;
            margin: 0 auto;
        }
        .card {
            background: white;
            border-radius: 1.5rem;
            padding: 2rem;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 0.8s ease-out forwards;
            border: 1px solid rgba(226, 232, 240, 0.5);
            position: relative;
            overflow: hidden;
        }
        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(135deg, #0ea5e9 0%, #06b6d4 100%);
            opacity: 0.8;
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }
        .card:hover::before {
            transform: scaleX(1);
        }
        .card:nth-child(1) { animation-delay: 0.1s; }
        .card:nth-child(2) { animation-delay: 0.2s; }
        .card:nth-child(3) { animation-delay: 0.3s; }
        .card:nth-child(4) { animation-delay: 0.4s; }
        .card:nth-child(5) { animation-delay: 0.5s; }
        .card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 40px rgba(0, 0, 0, 0.15);
        }
        .card-icon {
            width: 48px;
            height: 48px;
            margin: 0 0 1rem 0;
            opacity: 0.8;
            transition: transform 0.3s ease;
        }
        .card:hover .card-icon {
            transform: scale(1.1);
        }
        .card-title {
            font-size: 1.25rem;
            font-weight: 600;
            margin: 0 0 0.5rem 0;
            color: #1e293b;
        }
        .card-subtitle {
            font-size: 0.95rem;
            color: #64748b;
            margin: 0 0 1rem 0;
        }
        .card-note {
            font-size: 0.875rem;
            color: #f59e0b;
            margin: 0 0 1.5rem 0;
            font-weight: 500;
            background: #fef3c7;
            padding: 0.5rem 0.75rem;
            border-radius: 0.5rem;
            display: inline-block;
        }
        .card-button {
            background: linear-gradient(135deg, #0ea5e9 0%, #06b6d4 100%);
            color: white;
            border: none;
            padding: 0.75rem 1.5rem;
            border-radius: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            width: 100%;
            font-size: 1rem;
            box-shadow: 0 2px 8px rgba(6, 182, 212, 0.2);
        }
        .card-button:hover {
            background: linear-gradient(135deg, #0284c7 0%, #0891b2 100%);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(6, 182, 212, 0.3);
        }
        /* Footer */
        .footer {
            text-align: center;
            padding: 2rem 0;
            color: #64748b;
            font-size: 0.875rem;
            border-top: 1px solid rgba(226, 232, 240, 0.5);
            margin-top: auto;
            background: rgba(255, 255, 255, 0.8);
        }
        /* Animations */
        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }
            .hero {
                padding: 2rem 0;
            }
            .hero h1 {
                font-size: 2.5rem;
            }
            .hero .subtitle-ka {
                font-size: 1.125rem;
            }
            .logo-placeholder {
                width: 60px;
                height: 60px;
            }
            .cards-grid {
                grid-template-columns: 1fr;
                gap: 1.5rem;
            }
            .card {
                padding: 1.5rem;
            }
        }
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2rem;
            }
            .hero .subtitle-ka {
                font-size: 1rem;
            }
            .hero .subtitle-en {
                font-size: 1rem;
            }
            .logo-container {
                flex-direction: column;
                gap: 0.5rem;
            }
            .logo-placeholder {
                width: 50px;
                height: 50px;
            }
        }
    </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
  <script src="https://cdn.tailwindcss.com" type="text/javascript"></script>
 </head>
 <body>
  <div class="container"><!-- Hero Section -->
   <header class="hero">
    <div class="logo-container">
     <div class="logo-placeholder">
      <img src="imed-hub-logo.png" alt="IMED Hub Logo" class="logo-image">
     </div>
     <h1 id="main-title">IMED Hub</h1>
    </div>
    <p class="subtitle-ka" id="subtitle-ka">კლინიკური ხელსაწყოების პორტალი</p>
    <p class="subtitle-en" id="subtitle-en">Quick access to clinic tools &amp; microsites</p>
   </header><!-- Links Section -->
   <main class="links-section" id="links">
    <h2 class="section-title">Clinic Tools &amp; Sites</h2>
    <div class="cards-grid"><!-- Card 1: Phone Numbers -->
     <div class="card">
      <svg class="card-icon" viewbox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z" />
      </svg>
      <h3 class="card-title" id="card1-title">კლინიკის ექიმების ნომრები</h3>
      <p class="card-subtitle" id="card1-subtitle">Clinic phone list</p>
      <div class="card-note">
       🔒 pass: med123
      </div><button class="card-button" onclick="openLink('https://imed458.github.io/phone.github.io/')">Open</button>
     </div><!-- Card 2: Calculators -->
     <div class="card">
      <svg class="card-icon" viewbox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="4" y="2" width="16" height="20" rx="2"></rect> <line x1="8" y1="6" x2="16" y2="6"></line> <line x1="8" y1="10" x2="16" y2="10"></line> <line x1="8" y1="14" x2="16" y2="14"></line> <line x1="8" y1="18" x2="12" y2="18"></line>
      </svg>
      <h3 class="card-title" id="card2-title">კალკულატორები</h3>
      <p class="card-subtitle" id="card2-subtitle">Medical calculators</p><button class="card-button" onclick="openLink('https://imed458.github.io/imedcalc.github.io/')">Open</button>
     </div><!-- Card 3: Appointments -->
     <div class="card">
      <svg class="card-icon" viewbox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 11H5a2 2 0 0 0-2 2v7a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7a2 2 0 0 0-2-2h-4" /> <path d="M9 11V9a2 2 0 0 1 2-2h2a2 2 0 0 1 2 2v2" /> <circle cx="12" cy="16" r="1"></circle>
      </svg>
      <h3 class="card-title" id="card3-title">დანიშნულება</h3>
      <p class="card-subtitle" id="card3-subtitle">Appointment site</p><button class="card-button" onclick="openLink('https://imed458.github.io/danishnuleba1.github.io/')">Open</button>
     </div><!-- Card 4: Calendar -->
     <div class="card">
      <svg class="card-icon" viewbox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect> <line x1="16" y1="2" x2="16" y2="6"></line> <line x1="8" y1="2" x2="8" y2="6"></line> <line x1="3" y1="10" x2="21" y2="10"></line>
      </svg>
      <h3 class="card-title" id="card4-title">მორიგეობის კალენდარი</h3>
      <p class="card-subtitle" id="card4-subtitle">Duty schedule calendar</p><button class="card-button" onclick="openLink('https://imed458.github.io/calendar.github.io/')">Open</button>
     </div><!-- New Card 5: Inpatient -->
     <div class="card">
      <svg class="card-icon" viewbox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 21v-6a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v6"></path><polyline points="9 10 4 15 9 20"></polyline><path d="M20 4H9.5a2 2 0 0 0 0 4h11a2 2 0 0 1 2 2v9"></path></svg>
      <h3 class="card-title" id="card5-title">საწოლების მართვის სისტემა</h3>
      <p class="card-subtitle" id="card5-subtitle">Bed and Patient Management in Inpatient Ward</p>
      <button class="card-button" onclick="openLink('https://imed458.github.io/inpatienter.github.io/')">Open</button>
     </div>
    </div>
   </main><!-- Footer -->
   <footer class="footer">
    <p id="footer-text">© 2025 IMED Hub🩺. Created for clinic efficiency.</p>
   </footer>
  </div>
  <script>
        // Configuration object
        const defaultConfig = {
            main_title: "IMED Hub",
            subtitle_ka: "კლინიკური ხელსაწყოების პორტალი",
            subtitle_en: "Quick access to clinic tools & microsites",
            card1_title: "კლინიკის ექიმების ნომრები",
            card1_subtitle: "Clinic phone list",
            card2_title: "კალკულატორები",
            card2_subtitle: "Medical calculators",
            card3_title: "დანიშნულება",
            card3_subtitle: "Appointment site",
            card4_title: "მორიგეობის კალენდარი",
            card4_subtitle: "Duty schedule calendar",
            card5_title: "საწოლების მართვის სისტემა",
            card5_subtitle: "Bed and Patient Management in Inpatient Ward",
            footer_text: "© 2025 IMED Hub. Created for clinic efficiency.",
            background_color: "#f8fafc",
            primary_color: "#0ea5e9",
            text_color: "#1e293b",
            card_background: "#ffffff",
            accent_color: "#06b6d4",
            font_family: "Inter",
            font_size: 16
        };
        // Function to open links in new tab
        function openLink(url) {
            window.open(url, '_blank', 'noopener,noreferrer');
        }
        // Element SDK implementation
        async function onConfigChange(config) {
            const customFont = config.font_family || defaultConfig.font_family;
            const baseSize = config.font_size || defaultConfig.font_size;
            const baseFontStack = 'Inter, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif';
            // Update text content
            document.getElementById('main-title').textContent = config.main_title || defaultConfig.main_title;
            document.getElementById('subtitle-ka').textContent = config.subtitle_ka || defaultConfig.subtitle_ka;
            document.getElementById('subtitle-en').textContent = config.subtitle_en || defaultConfig.subtitle_en;
          
            document.getElementById('card1-title').textContent = config.card1_title || defaultConfig.card1_title;
            document.getElementById('card1-subtitle').textContent = config.card1_subtitle || defaultConfig.card1_subtitle;
            document.getElementById('card2-title').textContent = config.card2_title || defaultConfig.card2_title;
            document.getElementById('card2-subtitle').textContent = config.card2_subtitle || defaultConfig.card2_subtitle;
            document.getElementById('card3-title').textContent = config.card3_title || defaultConfig.card3_title;
            document.getElementById('card3-subtitle').textContent = config.card3_subtitle || defaultConfig.card3_subtitle;
            document.getElementById('card4-title').textContent = config.card4_title || defaultConfig.card4_title;
            document.getElementById('card4-subtitle').textContent = config.card4_subtitle || defaultConfig.card4_subtitle;
            document.getElementById('card5-title').textContent = config.card5_title || defaultConfig.card5_title;
            document.getElementById('card5-subtitle').textContent = config.card5_subtitle || defaultConfig.card5_subtitle;
          
            document.getElementById('footer-text').textContent = config.footer_text || defaultConfig.footer_text;
            // Update colors
            const backgroundColor = config.background_color || defaultConfig.background_color;
            const primaryColor = config.primary_color || defaultConfig.primary_color;
            const textColor = config.text_color || defaultConfig.text_color;
            const cardBackground = config.card_background || defaultConfig.card_background;
            const accentColor = config.accent_color || defaultConfig.accent_color;
            document.body.style.background = `linear-gradient(135deg, ${backgroundColor} 0%, #e2e8f0 100%)`;
            document.body.style.color = textColor;
            // Update primary color elements
            const heroTitle = document.querySelector('.hero h1');
            heroTitle.style.background = `linear-gradient(135deg, ${primaryColor} 0%, ${accentColor} 100%)`;
            heroTitle.style.webkitBackgroundClip = 'text';
            heroTitle.style.webkitTextFillColor = 'transparent';
            heroTitle.style.backgroundClip = 'text';
            // Update buttons and logo
            const buttons = document.querySelectorAll('.card-button');
            buttons.forEach(button => {
                button.style.background = `linear-gradient(135deg, ${primaryColor} 0%, ${accentColor} 100%)`;
            });
            // Update logo placeholder (transparent for custom image)
            const logoPlaceholder = document.querySelector('.logo-placeholder');
            if (logoPlaceholder) {
                logoPlaceholder.style.background = 'transparent';
            }
            // Update card backgrounds
            const cards = document.querySelectorAll('.card');
            cards.forEach(card => {
                card.style.background = cardBackground;
            });
            // Update fonts
            document.body.style.fontFamily = `${customFont}, ${baseFontStack}`;
          
            // Update font sizes proportionally
            document.querySelector('.hero h1').style.fontSize = `${baseSize * 2.2}px`;
            document.querySelector('.hero .subtitle-ka').style.fontSize = `${baseSize * 1.25}px`;
            document.querySelector('.hero .subtitle-en').style.fontSize = `${baseSize * 1.125}px`;
            document.querySelector('.section-title').style.fontSize = `${baseSize * 2}px`;
          
            const cardTitles = document.querySelectorAll('.card-title');
            cardTitles.forEach(title => {
                title.style.fontSize = `${baseSize * 1.25}px`;
            });
          
            const cardSubtitles = document.querySelectorAll('.card-subtitle');
            cardSubtitles.forEach(subtitle => {
                subtitle.style.fontSize = `${baseSize * 0.95}px`;
            });
        }
        function mapToCapabilities(config) {
            return {
                recolorables: [
                    {
                        get: () => config.background_color || defaultConfig.background_color,
                        set: (value) => {
                            config.background_color = value;
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ background_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.card_background || defaultConfig.card_background,
                        set: (value) => {
                            config.card_background = value;
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ card_background: value });
                            }
                        }
                    },
                    {
                        get: () => config.text_color || defaultConfig.text_color,
                        set: (value) => {
                            config.text_color = value;
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ text_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.primary_color || defaultConfig.primary_color,
                        set: (value) => {
                            config.primary_color = value;
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ primary_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.accent_color || defaultConfig.accent_color,
                        set: (value) => {
                            config.accent_color = value;
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ accent_color: value });
                            }
                        }
                    }
                ],
                borderables: [],
                fontEditable: {
                    get: () => config.font_family || defaultConfig.font_family,
                    set: (value) => {
                        config.font_family = value;
                        if (window.elementSdk) {
                            window.elementSdk.setConfig({ font_family: value });
                        }
                    }
                },
                fontSizeable: {
                    get: () => config.font_size || defaultConfig.font_size,
                    set: (value) => {
                        config.font_size = value;
                        if (window.elementSdk) {
                            window.elementSdk.setConfig({ font_size: value });
                        }
                    }
                }
            };
        }
        function mapToEditPanelValues(config) {
            return new Map([
                ["main_title", config.main_title || defaultConfig.main_title],
                ["subtitle_ka", config.subtitle_ka || defaultConfig.subtitle_ka],
                ["subtitle_en", config.subtitle_en || defaultConfig.subtitle_en],
                ["card1_title", config.card1_title || defaultConfig.card1_title],
                ["card1_subtitle", config.card1_subtitle || defaultConfig.card1_subtitle],
                ["card2_title", config.card2_title || defaultConfig.card2_title],
                ["card2_subtitle", config.card2_subtitle || defaultConfig.card2_subtitle],
                ["card3_title", config.card3_title || defaultConfig.card3_title],
                ["card3_subtitle", config.card3_subtitle || defaultConfig.card3_subtitle],
                ["card4_title", config.card4_title || defaultConfig.card4_title],
                ["card4_subtitle", config.card4_subtitle || defaultConfig.card4_subtitle],
                ["card5_title", config.card5_title || defaultConfig.card5_title],
                ["card5_subtitle", config.card5_subtitle || defaultConfig.card5_subtitle],
                ["footer_text", config.footer_text || defaultConfig.footer_text]
            ]);
        }
        // Initialize Element SDK
        if (window.elementSdk) {
            window.elementSdk.init({
                defaultConfig,
                onConfigChange,
                mapToCapabilities,
                mapToEditPanelValues
            });
        }
    </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'99f5febce36d95a5',t:'MTc2MzI4NTY5My4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
