<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Innasoft — Instalación y programación de software</title>
  <meta name="description" content="Innasoft — Servicios profesionales de instalación, configuración y programación de software a la medida."/>
  <meta name="theme-color" content="#0b7285"/>

  <!-- Favicon SVG inline -->
  <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><rect width=%22100%25%22 height=%22100%25%22 fill=%22%230b7285%22/><text x=%2250%25%22 y=%2255%25%22 font-size=%2250%22 text-anchor=%22middle%22 fill=%22white%22 font-family=%22Helvetica,Arial,sans-serif%22>IS</text></svg>">

  <style>
    :root{
      --bg:#f7fbfc;
      --card:#ffffff;
      --primary:#0b7285;
      --muted:#6b7280;
      --accent:#0e7490;
      --radius:14px;
      --maxw:1100px;
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      color: #0f1724;
    }
    *{box-sizing:border-box}
    html,body{height:100%;}
    body{
      margin:0;
      background: linear-gradient(180deg, var(--bg), #eef8fb);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      display:flex;
      justify-content:center;
      padding:32px 18px;
    }

    .site{
      width:100%;
      max-width:var(--maxw);
      background:transparent;
    }

    header{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:16px;
      margin-bottom:28px;
    }

    /* Brand */
    .brand{
      display:flex;
      gap:12px;
      align-items:center;
      text-decoration:none;
      color:inherit;
    }
    .logo{
      width:56px;
      height:56px;
      background:linear-gradient(135deg,var(--primary),var(--accent));
      border-radius:12px;
      display:flex;
      align-items:center;
      justify-content:center;
      color:white;
      font-weight:700;
      font-size:20px;
      box-shadow: 0 6px 20px rgba(11,114,133,0.18);
    }
    .brand h1{font-size:18px;margin:0;line-height:1}
    .brand p{margin:0;font-size:12px;color:var(--muted)}

    nav{
      display:flex;
      gap:14px;
      align-items:center;
    }
    nav a{
      text-decoration:none;
      color:var(--muted);
      font-weight:600;
      padding:8px 12px;
      border-radius:8px;
    }
    nav a.primary{
      background:var(--primary);
      color:white;
      box-shadow: 0 6px 16px rgba(11,114,133,0.14);
    }

    /* Hero */
    .hero{
      display:grid;
      grid-template-columns: 1fr 420px;
      gap:28px;
      align-items:center;
    }
    @media (max-width:980px){
      .hero{grid-template-columns:1fr; padding:12px}
      header{flex-direction:column;align-items:flex-start; gap:10px}
    }

    .card{
      background:var(--card);
      border-radius:var(--radius);
      padding:28px;
      box-shadow: 0 12px 40px rgba(6,12,20,0.06);
    }

    .hero-left h2{
      margin:0 0 10px 0;
      font-size:28px;
      line-height:1.05;
    }
    .tagline{
      color:var(--muted);
      margin-bottom:18px;
    }
    .actions{display:flex;gap:12px;flex-wrap:wrap}
    .btn{
      border:0;
      padding:10px 16px;
      border-radius:10px;
      font-weight:700;
      cursor:pointer;
      font-size:14px;
    }
    .btn.primary{background:var(--primary); color:white}
    .btn.ghost{background:transparent; color:var(--primary); border:1px solid rgba(11,114,133,0.12)}

    /* Features */
    .features{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:14px;
      margin-top:18px;
    }
    @media (max-width:980px){ .features{grid-template-columns:1fr} }

    .feature{
      padding:14px;
      border-radius:12px;
      background:linear-gradient(180deg, rgba(14,116,144,0.03), rgba(255,255,255,0));
      border:1px solid rgba(11,114,133,0.04);
    }
    .feature h3{margin:6px 0 0 0;font-size:15px}
    .feature p{margin:6px 0 0 0;color:var(--muted);font-size:13px}

    /* Right column quick contact */
    .contact-quick p{margin:0;color:var(--muted)}
    .contact-card{display:flex;flex-direction:column;gap:12px}

    /* Services section */
    .section{
      margin-top:28px;
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:18px;
    }
    @media (max-width:980px){ .section{grid-template-columns:1fr} }

    .services-list{display:grid;gap:12px}
    .service{
      padding:14px;border-radius:12px;border:1px solid rgba(11,114,133,0.06);
      background:white;
    }
    .service h4{margin:0 0 6px 0}
    .service p{margin:0;color:var(--muted);font-size:14px}

    /* Testimonials */
    .testimonials{display:flex;gap:12px;flex-wrap:wrap}
    .testimonial{
      flex:1 1 220px;
      padding:14px;border-radius:12px;background:linear-gradient(180deg,#fff,#fbffff);
      border:1px solid rgba(6,12,20,0.04);
    }

    /* Contact form */
    form{display:grid;gap:10px}
    label{font-size:13px;color:var(--muted)}
    input[type=text], input[type=email], textarea{
      padding:10px;border-radius:10px;border:1px solid rgba(6,12,20,0.08);font-size:14px;
    }
    textarea{min-height:120px;resize:vertical}
    .form-row{display:flex;gap:10px}
    @media (max-width:600px){ .form-row{flex-direction:column} }

    footer{
      margin-top:30px;padding:18px 8px;color:var(--muted);font-size:13px;text-align:center;
    }

    /* small utilities */
    .muted{color:var(--muted)}
    .small{font-size:13px}
  </style>
</head>
<body>
  <div class="site" role="main">
    <header>
      <a href="#" class="brand" aria-label="Inicio Innasoft">
        <div class="logo" aria-hidden="true">IS</div>
        <div>
          <h1>Innasoft</h1>
          <p>Instalación • Configuración • Programación</p>
        </div>
      </a>

      <nav aria-label="Navegación principal">
        <a href="#servicios">Servicios</a>
        <a href="#proyectos">Proyectos</a>
        <a href="#contacto" class="primary">Contáctanos</a>
      </nav>
    </header>

    <section class="hero">
      <div class="card hero-left" aria-labelledby="hero-title">
        <h2 id="hero-title">Soluciones de software profesionales para tu negocio</h2>
        <p class="tagline">En Innasoft instalamos, configuramos y programamos software a la medida. Tiempo de respuesta rápido, soporte local y precios competitivos.</p>

        <div class="actions" role="region" aria-label="Acciones principales">
          <button class="btn primary" onclick="document.getElementById('contacto').scrollIntoView({behavior:'smooth'})">Solicitar presupuesto</button>
          <button class="btn ghost" onclick="showDemo()">Ver demo</button>
        </div>

        <div class="features" aria-hidden="false" style="margin-top:18px">
          <div class="feature">
            <strong>Instalación segura</strong>
            <p>Instalamos y configuramos software con buenas prácticas y respaldo de datos.</p>
          </div>
          <div class="feature">
            <strong>Programación a medida</strong>
            <p>Desarrollos personalizados según flujo de trabajo y objetivos del cliente.</p>
          </div>
          <div class="feature">
            <strong>Soporte y mantenimiento</strong>
            <p>Soporte remoto y en sitio para mantener tus sistemas funcionando 24/7.</p>
          </div>
        </div>
      </div>

      <aside class="card contact-card" aria-labelledby="contacto-quick">
        <h3 id="contacto-quick">Contacto rápido</h3>
        <p class="muted">Estamos listos para ayudarte. Respuesta típica: <strong>24 horas</strong>.</p>

        <div>
          <p class="small"><strong>Teléfono:</strong> +57 300 000 0000</p>
          <p class="small"><strong>Email:</strong> <a href="mailto:contacto@innasoft.co">contacto@innasoft.co</a></p>
          <p class="small"><strong>Ubicación:</strong> Cali, Colombia</p>
        </div>

        <div style="margin-top:8px">
          <button class="btn primary" onclick="document.getElementById('contacto').scrollIntoView({behavior:'smooth'})">Escribir ahora</button>
        </div>

        <div style="margin-top:12px">
          <p class="small muted">Horario: Lun - Vie, 8:30 - 17:30</p>
        </div>
      </aside>
    </section>

    <!-- Servicios -->
    <section id="servicios" class="section" aria-labelledby="servicios-title">
      <div class="card">
        <h2 id="servicios-title">Nuestros servicios</h2>
        <p class="muted">Ofrecemos una gama completa de servicios técnicos y de desarrollo.</p>

        <div class="services-list" style="margin-top:12px">
          <div class="service">
            <h4>Instalación y configuración</h4>
            <p>Instalación de software de punto de venta, ERPs, bases de datos y herramientas de productividad.</p>
          </div>
          <div class="service">
            <h4>Programación y automatización</h4>
            <p>Desarrollo de pequeñas aplicaciones, scripts y automatizaciones para optimizar procesos.</p>
          </div>
          <div class="service">
            <h4>Migración y respaldo</h4>
            <p>Migramos datos entre sistemas y establecemos estrategias de respaldo y recuperación.</p>
          </div>
          <div class="service">
            <h4>Soporte técnico</h4>
            <p>Planes de soporte para atención remota y presencial según necesidades del cliente.</p>
          </div>
        </div>
      </div>

      <div class="card" id="proyectos" aria-labelledby="proyectos-title">
        <h2 id="proyectos-title">Proyectos recientes</h2>
        <p class="muted">Ejemplos reales de trabajos con empresas locales.</p>

        <div style="margin-top:12px" class="testimonials">
          <div class="testimonial">
            <strong>Proyecto: Punto de venta</strong>
            <p class="muted small">Instalación, configuración y capacitación para 3 sucursales. Resultado: reducción de errores de facturación.</p>
          </div>
          <div class="testimonial">
            <strong>Proyecto: Integración de inventarios</strong>
            <p class="muted small">Automatización del flujo entre almacén y tienda en línea.</p>
          </div>
          <div class="testimonial">
            <strong>Proyecto: Dashboard administrativo</strong>
            <p class="muted small">Dashboard para seguimiento de KPIs en tiempo real.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contacto -->
    <section class="card" id="contacto" aria-labelledby="contacto-title" style="margin-top:26px">
      <h2 id="contacto-title">Contacta a Innasoft</h2>
      <p class="muted">Rellena el formulario y nos pondremos en contacto contigo.</p>

      <form id="contactForm" onsubmit="return handleSubmit(event)" novalidate>
        <div class="form-row">
          <div style="flex:1">
            <label for="name">Nombre</label>
            <input id="name" name="name" type="text" placeholder="Tu nombre" required />
          </div>
          <div style="flex:1">
            <label for="company">Empresa (opcional)</label>
            <input id="company" name="company" type="text" placeholder="Nombre de la empresa" />
          </div>
        </div>

        <div>
          <label for="email">Correo electrónico</label>
          <input id="email" name="email" type="email" placeholder="tu@correo.com" required />
        </div>

        <div>
          <label for="message">Mensaje</label>
          <textarea id="message" name="message" placeholder="Cuéntanos brevemente tu necesidad" required></textarea>
        </div>

        <div style="display:flex;gap:10px;align-items:center;margin-top:6px">
          <button class="btn primary" type="submit">Enviar mensaje</button>
          <button type="button" class="btn ghost" onclick="clearForm()">Limpiar</button>
          <p id="formStatus" class="small muted" style="margin:0"></p>
        </div>
      </form>
    </section>

    <footer>
      <p>© <span id="year"></span> Innasoft — Instalación y programación de software. Todos los derechos reservados.</p>
      <p class="small muted">Dirección demostrativa · Cali, Colombia · <a href="mailto:contacto@innasoft.co">contacto@innasoft.co</a></p>
    </footer>
  </div>

  <script>
    // Small interactive helpers
    document.getElementById('year').textContent = new Date().getFullYear();

    function showDemo(){
      alert("Demo: podemos preparar una demo personalizada. Contáctanos via contacto@innasoft.co");
    }

    function clearForm(){
      document.getElementById('contactForm').reset();
      document.getElementById('formStatus').textContent = '';
    }

    function handleSubmit(e){
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim
