<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Zen Vida | Centro de Masajes Terapéuticos y Nutrición</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    body {
      margin: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background-color: #020617; /* fondo oscuro tipo presentación */
      color: #e5e7eb;
      line-height: 1.6;
    }

    a { color: #38bdf8; text-decoration: none; }

    header {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 50;
      background: rgba(15,23,42,0.95);
      border-bottom: 1px solid #1e293b;
    }

    .nav-container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 0.75rem 1.5rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .nav-logo {
      font-weight: 700;
      color: #38bdf8;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      font-size: 0.9rem;
    }

    nav a {
      margin-left: 1.25rem;
      font-size: 0.9rem;
      color: #cbd5e1;
    }

    .btn-primary {
      display: inline-block;
      background: #38bdf8;
      color: #0f172a;
      padding: 0.75rem 1.5rem;
      border-radius: 999px;
      font-weight: 600;
      font-size: 0.95rem;
    }

    .btn-outline {
      display: inline-block;
      border: 1px solid #38bdf8;
      color: #e5e7eb;
      padding: 0.6rem 1.25rem;
      border-radius: 999px;
      font-size: 0.9rem;
    }

    main {
      padding-top: 70px; /* altura del header fijo */
    }

    section {
      padding: 4rem 1.5rem;
    }

    .section-inner {
      max-width: 1100px;
      margin: 0 auto;
    }

    h1, h2, h3 {
      color: #f9fafb;
      margin-top: 0;
    }

    h1 { font-size: 2.4rem; margin-bottom: 0.75rem; }
    h2 { font-size: 1.8rem; margin-bottom: 0.75rem; }
    h3 { font-size: 1.3rem; margin-bottom: 0.5rem; }

    .text-muted { color: #9ca3af; }

    .hero {
      background: radial-gradient(circle at top left, #334155 0, #020617 45%);
    }

    .hero-grid {
      display: grid;
      grid-template-columns: minmax(0, 2.2fr) minmax(0, 1.8fr);
      gap: 2rem;
      align-items: center;
    }

    .hero-tag {
      display: inline-block;
      padding: 0.25rem 0.75rem;
      border-radius: 999px;
      background: rgba(56,189,248,0.12);
      color: #38bdf8;
      font-size: 0.8rem;
      margin-bottom: 0.75rem;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
      margin-top: 1.75rem;
    }

    .hero-card {
      background: rgba(15,23,42,0.8);
      border-radius: 1rem;
      padding: 1.5rem;
      border: 1px solid #1e293b;
    }

    .pill {
      display: inline-block;
      padding: 0.25rem 0.75rem;
      border-radius: 999px;
      font-size: 0.75rem;
      margin-right: 0.4rem;
      margin-bottom: 0.4rem;
    }

    .pill-green { background: rgba(34,197,94,0.14); color: #4ade80; }
    .pill-blue { background: rgba(59,130,246,0.14); color: #60a5fa; }

    .grid-2 {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.75rem;
      align-items: flex-start;
    }

    .card {
      background: #020617;
      border-radius: 1rem;
      padding: 1.5rem;
      border: 1px solid #1f2937;
    }

    ul {
      padding-left: 1.1rem;
      margin: 0.7rem 0 0;
    }

    li { margin-bottom: 0.4rem; }

    .badge {
      display: inline-block;
      padding: 0.25rem 0.65rem;
      border-radius: 999px;
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      margin-bottom: 0.6rem;
    }

    .badge-soft { background: rgba(148,163,184,0.15); color: #e5e7eb; }
    .badge-green { background: rgba(34,197,94,0.16); color: #bbf7d0; }
    .badge-blue { background: rgba(59,130,246,0.16); color: #bfdbfe; }
    .badge-amber { background: rgba(245,158,11,0.16); color: #fed7aa; }

    .testimonials {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.25rem;
    }

    .testimonial {
      background: #020617;
      border-radius: 0.9rem;
      border: 1px solid #1e293b;
      padding: 1.25rem;
      font-size: 0.95rem;
    }

    .form-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.5rem;
    }

    .form-field {
      display: flex;
      flex-direction: column;
      gap: 0.25rem;
      font-size: 0.9rem;
    }

    input, textarea, select {
      padding: 0.6rem 0.75rem;
      border-radius: 0.5rem;
      border: 1px solid #4b5563;
      background: #020617;
      color: #e5e7eb;
      font: inherit;
    }

    textarea { min-height: 110px; resize: vertical; }

    footer {
      border-top: 1px solid #1f2937;
      padding: 1.5rem;
      text-align: center;
      font-size: 0.85rem;
      color: #9ca3af;
    }

    @media (max-width: 800px) {
      .hero-grid {
        grid-template-columns: 1fr;
      }
      header { position: static; }
      main { padding-top: 0; }
      nav { display: none; } /* simplificación móvil; se podría sustituir por menú hamburguesa */
    }
  </style>
</head>
<body>

<header>
  <div class="nav-container">
    <div class="nav-logo">ZEN VIDA · BARCELONA</div>
    <nav>
      <a href="#inicio">Inicio</a>
      <a href="#zenvida">Zen Vida</a>
      <a href="#servicios">Servicios</a>
      <a href="#empresas">Wellness empresas</a>
      <a href="#opiniones">Opiniones</a>
      <a href="#reserva">Reserva</a>
      <a href="#contacto">Contacto</a>
    </nav>
  </div>
</header>

<main>

  <!-- INICIO / HERO -->
  <section id="inicio" class="hero">
    <div class="section-inner hero-grid">
      <div>
        <div class="hero-tag">Masajes terapéuticos · Nutrición personalizada</div>
        <h1>Bienestar profundo en el corazón de Barcelona</h1>
        <p class="text-muted">
          Centro especializado en masajes terapéuticos y nutrición, con 7 años de experiencia
          ayudando a reducir dolor, estrés y fatiga desde un enfoque integral cuerpo &amp; alimentación.
        </p>
        <div class="hero-buttons">
          <a href="#reserva" class="btn-primary">Reservar cita ahora</a>
          <a href="#servicios" class="btn-outline">Ver servicios</a>
        </div>
      </div>
      <div class="hero-card">
        <h3>Tu momento Zen, sin complicaciones</h3>
        <p class="text-muted">
          Elige el servicio que necesitas y reserva en pocos pasos. Confirmaremos tu cita por WhatsApp o correo.
        </p>
        <div style="margin-top: 0.75rem;">
          <span class="pill pill-green">Ubicación céntrica</span>
          <span class="pill pill-green">Enfoque integral</span>
          <span class="pill pill-blue">Atención cercana</span>
        </div>
        <p style="margin-top: 1.25rem; font-size: 0.9rem;" class="text-muted">
          7 años de trayectoria · Pareja de profesionales con formación certificada · Equipo en crecimiento.
        </p>
      </div>
    </div>
  </section>

  <!-- ZEN VIDA -->
  <section id="zenvida">
    <div class="section-inner">
      <div class="badge badge-soft">Quiénes somos</div>
      <h2>Zen Vida · Centro de Masajes Terapéuticos y Nutrición</h2>
      <div class="grid-2" style="margin-top: 1.25rem;">
        <div>
          <p>
            Zen Vida es un centro de bienestar ubicado en pleno centro de Barcelona, con 7 años de experiencia
            y una base fiel de clientes que confían en nuestro acompañamiento para mejorar su salud física y emocional.
          </p>
          <p>
            El centro está gestionado por una pareja de profesionales con formación certificada en terapias manuales
            y nutrición, apoyados por un equipo en crecimiento que comparte la misma filosofía: escuchar a cada persona,
            personalizar cada sesión y acompañar el cambio de hábitos a su ritmo.
          </p>
        </div>
        <div>
          <h3>Por qué elegir Zen Vida</h3>
          <ul>
            <li>Ubicación céntrica, bien comunicada y fácil de encontrar.</li>
            <li>Enfoque integral: masajes terapéuticos y nutrición trabajando en la misma dirección.</li>
            <li>Trato cálido, cercano y profesional, con seguimiento cuando es necesario.</li>
            <li>Centro en evolución constante, incorporando nuevas terapias y servicios de bienestar.</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- SERVICIOS -->
  <section id="servicios">
    <div class="section-inner">
      <div class="badge badge-green">Servicios</div>
      <h2>Qué podemos hacer por ti</h2>
      <div class="grid-2" style="margin-top: 1.5rem;">

        <div class="card">
          <h3>Masajes terapéuticos</h3>
          <p class="text-muted">
            Masajes orientados a aliviar dolor muscular, contracturas, sobrecarga por estrés o deporte,
            combinando distintas técnicas según tus necesidades.
          </p>
          <ul>
            <li>Masaje terapéutico descontracturante.</li>
            <li>Masaje deportivo y de recuperación.</li>
            <li>Masaje relajante anti-estrés.</li>
            <li>Protocolos específicos para dolor crónico (lumbar, cervical, etc.).</li>
          </ul>
        </div>

        <div class="card">
          <h3>Nutrición personalizada</h3>
          <p class="text-muted">
            Asesoramiento nutricional práctico y realista para mejorar energía, digestión y composición
            corporal sin dietas extremas ni soluciones milagro.
          </p>
          <ul>
            <li>Primera visita de valoración y objetivos.</li>
            <li>Plan nutricional personalizado con seguimiento.</li>
            <li>Nutrición para deporte y recuperación.</li>
            <li>Programas para estrés, descanso y salud digestiva.</li>
          </ul>
        </div>
      </div>

      <div class="card" style="margin-top: 1.75rem;">
        <h3>Paquetes integrales bienestar</h3>
        <p class="text-muted">
          Combinamos masajes terapéuticos y nutrición en programas diseñados para abordar tu bienestar
          desde varios ángulos al mismo tiempo.
        </p>
        <ul>
          <li><strong>Pack Zen Dolor Crónico:</strong> valoración + plan nutricional + 4 masajes terapéuticos específicos.</li>
          <li><strong>Pack Estrés Ejecutivo:</strong> protocolo de masajes + pautas de descanso y alimentación.</li>
          <li><strong>Pack Deportista:</strong> masajes de descarga + nutrición para rendimiento y recuperación.</li>
        </ul>
        <div style="margin-top: 1rem;">
          <a href="#reserva" class="btn-outline">Quiero más información / Reservar</a>
        </div>
      </div>
    </div>
  </section>

  <!-- WELLNESS EMPRESAS -->
  <section id="empresas">
    <div class="section-inner">
      <div class="badge badge-blue">Wellness corporativo</div>
      <h2>Bienestar para empresas</h2>
      <div class="grid-2" style="margin-top: 1.25rem;">
        <div>
          <p>
            Cada vez más empresas apuestan por cuidar la salud física y emocional de sus equipos.
            En Zen Vida diseñamos programas de bienestar corporativo adaptados a la realidad de cada organización.
          </p>
          <ul>
            <li>Sesiones de masajes in-situ en la empresa en días u horarios definidos.</li>
            <li>Bonos y descuentos corporativos para que tus equipos acudan al centro.</li>
            <li>Talleres de autocuidado, ergonomía y alimentación saludable para empleados.</li>
          </ul>
        </div>
        <div class="card">
          <h3>¿Eres empresa?</h3>
          <p class="text-muted">
            Cuéntanos cuántas personas sois, qué tipo de servicio buscáis y en qué horarios.
            Te enviaremos una propuesta ajustada a vuestras necesidades y presupuesto.
          </p>
          <a href="#contacto" class="btn-primary">Solicitar propuesta</a>
        </div>
      </div>
    </div>
  </section>

  <!-- OPINIONES -->
  <section id="opiniones">
    <div class="section-inner">
      <div class="badge badge-soft">Opiniones</div>
      <h2>Lo que dicen nuestros clientes</h2>
      <p class="text-muted">
        Una parte importante del crecimiento de Zen Vida viene de las recomendaciones de quienes ya confían en nosotros.
      </p>
      <div class="testimonials" style="margin-top: 1.25rem;">
        <div class="testimonial">
          <p>“Llevaba años con dolor cervical y desde que acudo a Zen Vida he reducido molestias y duermo mucho mejor.”</p>
          <p class="text-muted">– Nombre cliente, profesión</p>
        </div>
        <div class="testimonial">
          <p>“Me gustó mucho el enfoque integral: masaje, pautas de descanso y pequeños cambios en la alimentación.”</p>
          <p class="text-muted">– Nombre cliente</p>
        </div>
        <div class="testimonial">
          <p>“Trato muy cercano y profesional. Se nota la experiencia y la personalización de cada sesión.”</p>
          <p class="text-muted">– Nombre cliente</p>
        </div>
      </div>
    </div>
  </section>

  <!-- RESERVA -->
  <section id="reserva">
    <div class="section-inner">
      <div class="badge badge-green">Reserva</div>
      <h2>Reserva tu momento Zen</h2>
      <p class="text-muted">
        Elige el canal que te resulte más cómodo para reservar. Te responderemos lo antes posible para confirmar día y hora.
      </p>
      <div class="hero-buttons" style="margin-top: 1.25rem;">
        <!-- Sustituye # por tus enlaces reales -->
        <a href="https://wa.me/000000000" class="btn-primary">Reservar por WhatsApp</a>
        <a href="tel:000000000" class="btn-outline">Llamar al centro</a>
      </div>

      <div class="card" style="margin-top: 1.75rem;">
        <h3>Formulario rápido de reserva</h3>
        <form class="form-grid">
          <div class="form-field">
            <label for="nombre">Nombre y apellidos</label>
            <input id="nombre" type="text" placeholder="Tu nombre" />
          </div>
          <div class="form-field">
            <label for="email">Correo electrónico</label>
            <input id="email" type="email" placeholder="tucorreo@ejemplo.com" />
          </div>
          <div class="form-field">
            <label for="tel">Teléfono</label>
            <input id="tel" type="tel" placeholder="Tu teléfono" />
          </div>
          <div class="form-field">
            <label for="servicio">Servicio deseado</label>
            <select id="servicio">
              <option>Selecciona un servicio</option>
              <option>Masaje terapéutico</option>
              <option>Masaje relajante</option>
              <option>Masaje deportivo</option>
              <option>Primera visita nutrición</option>
              <option>Pack integral bienestar</option>
            </select>
          </div>
          <div class="form-field">
            <label for="franja">Franja horaria preferida</label>
            <input id="franja" type="text" placeholder="Ej. Lunes tarde, entre 17:00 y 19:00" />
          </div>
          <div class="form-field">
            <label for="mensaje">Comentarios adicionales</label>
            <textarea id="mensaje" placeholder="Cuéntanos brevemente qué necesitas"></textarea>
          </div>
        </form>
        <div style="margin-top: 1.25rem;">
          <button type="submit" class="btn-primary">Enviar solicitud de reserva</button>
        </div>
        <p class="text-muted" style="margin-top: 0.75rem; font-size: 0.8rem;">
          Tus datos se utilizarán únicamente para gestionar tu reserva y la comunicación relacionada con tus citas.
        </p>
      </div>
    </div>
  </section>

  <!-- CONTACTO -->
  <section id="contacto">
    <div class
