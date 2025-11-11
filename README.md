<html lang="ka">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>IMED Hub</title>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&amp;display=swap" rel="stylesheet">
  <style>
    body {
      box-sizing: border-box;
    }
    
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      height: 100%;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
      color: #2c3e50;
    }

    .container {
      min-height: 100%;
      display: flex;
      flex-direction: column;
      padding: 2rem 1rem;
      max-width: 1200px;
      margin: 0 auto;
    }

    header {
      text-align: center;
      margin-bottom: 3rem;
      padding: 2rem;
      background: #ffffff;
      border-radius: 16px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.07);
    }

    .logo {
      width: 80px;
      height: 80px;
      margin: 0 auto 1.5rem;
      background: #0B3D91;
      border-radius: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 8px 16px rgba(11, 61, 145, 0.2);
    }

    .logo-text {
      font-size: 2rem;
      font-weight: 700;
      color: #ffffff;
    }

    h1 {
      font-size: 2.5rem;
      font-weight: 700;
      color: #0B3D91;
      margin-bottom: 0.5rem;
    }

    .subtitle {
      font-size: 1.125rem;
      color: #64748b;
      font-weight: 400;
    }

    main {
      flex: 1;
    }

    .section-title {
      font-size: 1.875rem;
      font-weight: 600;
      color: #0B3D91;
      margin-bottom: 2rem;
      text-align: center;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 1.5rem;
      margin-bottom: 3rem;
    }

    .project-card {
      background: #ffffff;
      border-radius: 12px;
      padding: 2rem;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
      transition: all 0.3s ease;
      border: 2px solid transparent;
    }

    .project-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 8px 24px rgba(11, 61, 145, 0.15);
      border-color: #0B3D91;
    }

    .project-icon {
      width: 48px;
      height: 48px;
      background: linear-gradient(135deg, #0B3D91 0%, #1e5bb8 100%);
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 1rem;
    }

    .project-icon svg {
      width: 24px;
      height: 24px;
      fill: #ffffff;
    }

    .project-title {
      font-size: 1.25rem;
      font-weight: 600;
      color: #1e293b;
      margin-bottom: 0.75rem;
    }

    .project-description {
      font-size: 0.9375rem;
      color: #64748b;
      line-height: 1.6;
      margin-bottom: 1rem;
    }

    .project-category {
      display: inline-block;
      padding: 0.375rem 0.875rem;
      background: #e0f2fe;
      color: #0B3D91;
      border-radius: 20px;
      font-size: 0.8125rem;
      font-weight: 500;
      margin-bottom: 1.25rem;
    }

    .project-button {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.75rem 1.5rem;
      background: #0B3D91;
      color: #ffffff;
      text-decoration: none;
      border-radius: 8px;
      font-weight: 500;
      font-size: 0.9375rem;
      transition: all 0.3s ease;
      border: none;
      cursor: pointer;
    }

    .project-button:hover {
      background: #1e5bb8;
      transform: translateX(2px);
    }

    .project-button svg {
      width: 16px;
      height: 16px;
      fill: currentColor;
    }

    footer {
      text-align: center;
      padding: 2rem;
      color: #64748b;
      font-size: 0.875rem;
      margin-top: 2rem;
    }

    @media (max-width: 768px) {
      .container {
        padding: 1rem;
      }

      h1 {
        font-size: 1.875rem;
      }

      .subtitle {
        font-size: 1rem;
      }

      .section-title {
        font-size: 1.5rem;
      }

      .projects-grid {
        grid-template-columns: 1fr;
      }

      .logo {
        width: 64px;
        height: 64px;
      }

      .logo-text {
        font-size: 1.5rem;
      }
    }
  </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
  <script src="https://cdn.tailwindcss.com" type="text/javascript"></script>
 </head>
 <body>
  <div class="container">
   <header>
    <div class="logo"><span class="logo-text" id="logo-text">IM</span>
    </div>
    <h1 id="site-title">IMED Hub</h1>
    <p class="subtitle" id="site-subtitle">ჩემი ვებპროექტების ცენტრი</p>
   </header>
   <main>
    <h2 class="section-title" id="projects-heading">ჩემი პროექტები</h2>
    <div class="projects-grid">
     <div class="project-card">
      <div class="project-icon">
       <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z" />
       </svg>
      </div>
      <h3 class="project-title">კლინიკის ექიმების მობილური ნომრები</h3>
      <p class="project-description">სწრაფი წვდომა კლინიკის ექიმების საკონტაქტო ინფორმაციაზე. პაროლი: med123</p><span class="project-category">კონტაქტები</span> <br><a href="https://imed458.github.io/phone.github.io/" target="_blank" rel="noopener noreferrer" class="project-button"> Open 
       <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M19 19H5V5h7V3H5c-1.11 0-2 .9-2 2v14c0 1.1.89 2 2 2h14c1.1 0 2-.9 2-2v-7h-2v7zM14 3v2h3.59l-9.83 9.83 1.41 1.41L19 6.41V10h2V3h-7z" />
       </svg></a>
     </div>
     <div class="project-card">
      <div class="project-icon">
       <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z" />
       </svg>
      </div>
      <h3 class="project-title">კალკულატორები</h3>
      <p class="project-description">სამედიცინო კალკულატორების კოლექცია სხვადასხვა გამოთვლებისთვის</p><span class="project-category">ინსტრუმენტები</span> <br><a href="https://imed458.github.io/imedcalc.github.io/" target="_blank" rel="noopener noreferrer" class="project-button"> Open 
       <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M19 19H5V5h7V3H5c-1.11 0-2 .9-2 2v14c0 1.1.89 2 2 2h14c1.1 0 2-.9 2-2v-7h-2v7zM14 3v2h3.59l-9.83 9.83 1.41 1.41L19 6.41V10h2V3h-7z" />
       </svg></a>
     </div>
     <div class="project-card">
      <div class="project-icon">
       <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M19 3h-4.18C14.4 1.84 13.3 1 12 1c-1.3 0-2.4.84-2.82 2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-7 0c.55 0 1 .45 1 1s-.45 1-1 1-1-.45-1-1 .45-1 1-1zm2 14H7v-2h7v2zm3-4H7v-2h10v2zm0-4H7V7h10v2z" />
       </svg>
      </div>
      <h3 class="project-title">დანიშნულების საიტი</h3>
      <p class="project-description">სამედიცინო დანიშნულებების მართვის სისტემა</p><span class="project-category">მენეჯმენტი</span> <br><a href="https://imed458.github.io/danishnuleba1.github.io/" target="_blank" rel="noopener noreferrer" class="project-button"> Open 
       <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M19 19H5V5h7V3H5c-1.11 0-2 .9-2 2v14c0 1.1.89 2 2 2h14c1.1 0 2-.9 2-2v-7h-2v7zM14 3v2h3.59l-9.83 9.83 1.41 1.41L19 6.41V10h2V3h-7z" />
       </svg></a>
     </div>
    </div>
   </main>
   <footer id="footer-text">
    © 2024 IMED Hub. All rights reserved.
   </footer>
  </div>
  <script>
    const defaultConfig = {
      site_title: "IMED Hub",
      site_subtitle: "ჩემი ვებპროექტების ცენტრი",
      projects_heading: "ჩემი პროექტები",
      footer_text: "© 2024 IMED Hub. All rights reserved.",
      primary_color: "#0B3D91",
      background_gradient_start: "#f5f7fa",
      background_gradient_end: "#c3cfe2",
      card_background: "#ffffff",
      text_color: "#2c3e50",
      font_family: "Inter",
      font_size: 16
    };

    async function onConfigChange(config) {
      const baseSize = config.font_size || defaultConfig.font_size;
      const customFont = config.font_family || defaultConfig.font_family;
      const baseFontStack = '-apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif';
      const fontFamily = `'${customFont}', ${baseFontStack}`;

      document.body.style.fontFamily = fontFamily;

      const primaryColor = config.primary_color || defaultConfig.primary_color;
      const bgGradientStart = config.background_gradient_start || defaultConfig.background_gradient_start;
      const bgGradientEnd = config.background_gradient_end || defaultConfig.background_gradient_end;
      const cardBg = config.card_background || defaultConfig.card_background;
      const textColor = config.text_color || defaultConfig.text_color;

      document.body.style.background = `linear-gradient(135deg, ${bgGradientStart} 0%, ${bgGradientEnd} 100%)`;
      document.body.style.color = textColor;

      const header = document.querySelector('header');
      if (header) header.style.background = cardBg;

      const logo = document.querySelector('.logo');
      if (logo) logo.style.background = primaryColor;

      const h1Elements = document.querySelectorAll('h1, .section-title');
      h1Elements.forEach(el => {
        el.style.color = primaryColor;
        el.style.fontSize = `${baseSize * 2.5 / 16}rem`;
      });

      const sectionTitle = document.querySelector('.section-title');
      if (sectionTitle) sectionTitle.style.fontSize = `${baseSize * 1.875 / 16}rem`;

      const projectCards = document.querySelectorAll('.project-card');
      projectCards.forEach(card => {
        card.style.background = cardBg;
        card.style.borderColor = 'transparent';
      });

      const projectIcons = document.querySelectorAll('.project-icon');
      projectIcons.forEach(icon => {
        icon.style.background = `linear-gradient(135deg, ${primaryColor} 0%, ${primaryColor}dd 100%)`;
      });

      const projectCategories = document.querySelectorAll('.project-category');
      projectCategories.forEach(cat => {
        cat.style.color = primaryColor;
        cat.style.fontSize = `${baseSize * 0.8125 / 16}rem`;
      });

      const projectButtons = document.querySelectorAll('.project-button');
      projectButtons.forEach(btn => {
        btn.style.background = primaryColor;
        btn.style.fontSize = `${baseSize * 0.9375 / 16}rem`;
      });

      document.getElementById('site-title').textContent = config.site_title || defaultConfig.site_title;
      document.getElementById('site-subtitle').textContent = config.site_subtitle || defaultConfig.site_subtitle;
      document.getElementById('projects-heading').textContent = config.projects_heading || defaultConfig.projects_heading;
      document.getElementById('footer-text').textContent = config.footer_text || defaultConfig.footer_text;

      const subtitle = document.querySelector('.subtitle');
      if (subtitle) subtitle.style.fontSize = `${baseSize * 1.125 / 16}rem`;

      const projectTitles = document.querySelectorAll('.project-title');
      projectTitles.forEach(title => title.style.fontSize = `${baseSize * 1.25 / 16}rem`);

      const projectDescriptions = document.querySelectorAll('.project-description');
      projectDescriptions.forEach(desc => desc.style.fontSize = `${baseSize * 0.9375 / 16}rem`);

      const footer = document.querySelector('footer');
      if (footer) footer.style.fontSize = `${baseSize * 0.875 / 16}rem`;
    }

    function mapToCapabilities(config) {
      return {
        recolorables: [
          {
            get: () => config.primary_color || defaultConfig.primary_color,
            set: (value) => {
              config.primary_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ primary_color: value });
            }
          },
          {
            get: () => config.background_gradient_start || defaultConfig.background_gradient_start,
            set: (value) => {
              config.background_gradient_start = value;
              if (window.elementSdk) window.elementSdk.setConfig({ background_gradient_start: value });
            }
          },
          {
            get: () => config.background_gradient_end || defaultConfig.background_gradient_end,
            set: (value) => {
              config.background_gradient_end = value;
              if (window.elementSdk) window.elementSdk.setConfig({ background_gradient_end: value });
            }
          },
          {
            get: () => config.card_background || defaultConfig.card_background,
            set: (value) => {
              config.card_background = value;
              if (window.elementSdk) window.elementSdk.setConfig({ card_background: value });
            }
          },
          {
            get: () => config.text_color || defaultConfig.text_color,
            set: (value) => {
              config.text_color = value;
              if (window.elementSdk) window.elementSdk.setConfig({ text_color: value });
            }
          }
        ],
        borderables: [],
        fontEditable: {
          get: () => config.font_family || defaultConfig.font_family,
          set: (value) => {
            config.font_family = value;
            if (window.elementSdk) window.elementSdk.setConfig({ font_family: value });
          }
        },
        fontSizeable: {
          get: () => config.font_size || defaultConfig.font_size,
          set: (value) => {
            config.font_size = value;
            if (window.elementSdk) window.elementSdk.setConfig({ font_size: value });
          }
        }
      };
    }

    function mapToEditPanelValues(config) {
      return new Map([
        ["site_title", config.site_title || defaultConfig.site_title],
        ["site_subtitle", config.site_subtitle || defaultConfig.site_subtitle],
        ["projects_heading", config.projects_heading || defaultConfig.projects_heading],
        ["footer_text", config.footer_text || defaultConfig.footer_text]
      ]);
    }

    if (window.elementSdk) {
      window.elementSdk.init({
        defaultConfig,
        onConfigChange,
        mapToCapabilities,
        mapToEditPanelValues
      });
    }
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'99ce39d0b77ee59a',t:'MTc2Mjg2ODY4Mi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
