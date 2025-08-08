<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Marathon Pro — Plan de entrenamiento y nutrición</title>
  <meta name="description" content="Plan completo: nutrición, entrenamiento, ejercicios de pierna para maratonistas y trucos profesionales.">
  <meta name="author" content="Marathon Pro">
  <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🏃‍♂️</text></svg>">
  <style>
    /* --- Reset y tipografía --- */
    :root{
      --bg:#f6f8fb; --card:#ffffff; --muted:#57606a; --accent:#1f6feb; --accent-2:#06b6d4;
      --shadow: 0 6px 24px rgba(20,33,61,0.08);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,"Helvetica Neue",Arial;background:linear-gradient(180deg,#f3f7fb, #eef6fb);color:#0b1320;padding:28px;display:flex;justify-content:center}
    .container{width:100%;max-width:1100px}
    header{display:flex;align-items:center;justify-content:space-between;gap:12px;margin-bottom:18px}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:52px;height:52px;border-radius:10px;background:linear-gradient(135deg,var(--accent),var(--accent-2));display:flex;align-items:center;justify-content:center;color:white;font-weight:700;box-shadow:var(--shadow)}
    h1{margin:0;font-size:20px}
    .subtitle{color:var(--muted);font-size:13px}
    .controls{display:flex;gap:8px}
    button{background:transparent;border:1px solid rgba(11,19,32,0.06);padding:8px 12px;border-radius:8px;cursor:pointer;font-weight:600}
    button.primary{background:linear-gradient(90deg,var(--accent),var(--accent-2));color:white;border:0}
    main{display:grid;grid-template-columns:320px 1fr;gap:18px}
    nav.sidebar{position:sticky;top:28px;align-self:start}
    .card{background:var(--card);padding:14px;border-radius:12px;box-shadow:var(--shadow);border:1px solid rgba(11,19,32,0.03)}
    .nav-list{display:flex;flex-direction:column;gap:8px}
    .nav-item{padding:10px;border-radius:10px;cursor:pointer;color:#0b1320}
    .nav-item.active{background:linear-gradient(90deg, rgba(31,111,235,0.12), rgba(6,182,212,0.08));font-weight:700}
    .panel{min-height:300px}
    .grid{display:grid;gap:12px}
    @media(min-width:900px){ .grid.two{grid-template-columns:repeat(2,1fr)} .grid.three{grid-template-columns:repeat(3,1fr)} }
    h2{margin:0 0 8px 0}
    .muted{color:var(--muted);font-size:13px}
    .exercise-name{font-weight:700;margin-bottom:6px}
    .meta{font-size:13px;color:var(--muted);margin-top:6px}
    .hint{background:#f0fbff;border-left:4px solid var(--accent-2);padding:10px;border-radius:8px}
    footer{margin-top:18px;color:var(--muted);font-size:13px;text-align:center}

    /* Botones de acción reducidos */
    .actions{display:flex;gap:8px}
    .small{font-size:13px;color:var(--muted)}

    /* Print */
    @media print{
      body{padding:0;background:white}
      header, .controls, .nav-item, .actions, button{display:none}
      main{grid-template-columns:1fr}
      .card{box-shadow:none;border:0}
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo" aria-hidden="true">MP</div>
        <div>
          <h1>Marathon Pro</h1>
          <div class="subtitle">Plan completo: nutrición • entrenamiento • fuerza (piernas)</div>
        </div>
      </div>

      <div class="controls">
        <div class="actions">
          <button id="downloadHtmlBtn">Descargar HTML</button>
          <button id="printBtn">Imprimir / Guardar PDF</button>
        </div>
      </div>
    </header>

    <main>
      <!-- Sidebar -->
      <aside class="sidebar">
        <div class="card">
          <nav class="nav-list" role="navigation" aria-label="Secciones">
            <div class="nav-item active" data-tab="nutricion">Nutrición</div>
            <div class="nav-item" data-tab="entrenamiento">Entrenamiento</div>
            <div class="nav-item" data-tab="gimnasio">Gimnasio — Piernas</div>
            <div class="nav-item" data-tab="trucos">Trucos & Checklist</div>
            <div style="height:8px"></div>
            <div class="small">Comparte el enlace si has publicado en GitHub Pages o Netlify.</div>
          </nav>
        </div>

        <div style="height:12px"></div>

        <div class="card small">
          <strong>Nivel:</strong> Personaliza sets/reps según tu experiencia.<br>
          <strong>Sugerencia:</strong> 2 sesiones de fuerza semanales, 1 tirada larga.
        </div>
      </aside>

      <!-- Content -->
      <section class="panel">
        <!-- NUTRICION -->
        <article id="nutricion" class="card content-section">
          <h2>Nutrición — ejemplo diario</h2>
          <p class="muted">Ejemplos prácticos para cubrir energía y recuperación.</p>
          <div style="height:10px"></div>
          <div class="grid two">
            <div class="card">
              <h3>Desayuno</h3>
              <ul>
                <li>Avena + leche/bebida vegetal + plátano + 1 cda miel</li>
                <li>Huevos revueltos con espinacas + tostada integral</li>
                <li>Opción rápida: batido (plátano + proteína + avena)</li>
              </ul>
              <p class="meta">Carbohidratos complejos y proteína. Ideal 60–90 min antes de entreno largo.</p>
            </div>

            <div class="card">
              <h3>Almuerzo</h3>
              <ul>
                <li>Pechuga de pollo/pescado + quinoa/pasta integral + verduras</li>
                <li>Ensalada con garbanzos + aguacate + arroz integral</li>
              </ul>
              <p class="meta">Restaurar glucógeno y proteína para recuperación.</p>
            </div>

            <div class="card">
              <h3>Cena</h3>
              <ul>
                <li>Salmón o pescado graso + camote + brócoli</li>
                <li>Tortilla de claras con verduras</li>
              </ul>
              <p class="meta">Ligera, prioriza proteína y verduras.</p>
            </div>

            <div class="card">
              <h3>Snacks / Durante tiradas</h3>
              <ul>
                <li>Frutos secos, plátano, yogur griego</li>
                <li>Geles / barritas durante tiradas largas (pruébalos antes)</li>
              </ul>
              <p class="meta">Practica lo que usarás el día de la carrera.</p>
            </div>
          </div>

          <div style="height:12px"></div>
          <div class="hint">
            <strong>Consejo:</strong> 2–3 días antes de la carrera aumenta la proporción de carbohidratos (carb-loading moderado). En semanas de alto volumen, no recortes calorías drásticamente.
          </div>
        </article>

        <!-- ENTRENAMIENTO -->
        <article id="entrenamiento" class="card content-section" style="display:none">
          <h2>Plan semanal (ejemplo)</h2>
          <p class="muted">Estructura típica para maratón. Ajusta volumen y ritmos a tu nivel.</p>
          <div style="height:10px"></div>
          <div class="grid two">
            <div class="card"><strong>Lunes</strong><p class="muted">Rodaje suave 8–10 km + movilidad.</p></div>
            <div class="card"><strong>Martes</strong><p class="muted">Series: 10×400 m a ritmo 5–10K, rec. 60–90s.</p></div>
            <div class="card"><strong>Miércoles</strong><p class="muted">Rodaje medio 10–14 km + core 10–15 min.</p></div>
            <div class="card"><strong>Jueves</strong><p class="muted">Series largas: 3–5×2 km a ritmo medio-alto.</p></div>
            <div class="card"><strong>Viernes</strong><p class="muted">Descanso activo: bici o natación 30–45 min.</p></div>
            <div class="card"><strong>Sábado</strong><p class="muted">Tirada larga: 18–32 km (progresiva).</p></div>
            <div class="card"><strong>Domingo</strong><p class="muted">Recuperación: 6–8 km o descanso.</p></div>
          </div>

          <details style="margin-top:10px"><summary class="small">Cómo combinar fuerza</summary>
            <p class="small">2 sesiones/semana: una de fuerza (3–5 reps series pesadas) y una de resistencia/potencia (8–15 reps, explosividad). Evita fatigar piernas antes de la tirada larga.</p>
          </details>
        </article>

        <!-- GIMNASIO PIERNA -->
        <article id="gimnasio" class="card content-section" style="display:none">
          <h2>Gimnasio — Fuerza de piernas (específico para maratonistas)</h2>
          <p class="muted">Enfócate en fuerza unilateral, cadena posterior y tolerancia al impacto.</p>

          <div style="height:10px"></div>
          <div class="grid two">
            <div class="card">
              <div class="exercise-name">Sentadilla con barra (Back squat)</div>
              <p><strong>Técnica:</strong> barra sobre trapecio alto; pies a anchura de hombros; bajar controlado hasta paralelo; impulsar con talón y glúteo; mantener espalda neutra.</p>
              <p class="meta">Sets/Reps: 3–4×6–10 (fuerza) o 3×10–12 (resistencia).</p>
            </div>

            <div class="card">
              <div class="exercise-name">Zancadas caminando con mancuernas</div>
              <p><strong>Técnica:</strong> paso largo, rodilla trasera cerca del suelo, empujar con talón delantero; mantener torso estable.</p>
              <p class="meta">Sets/Reps: 3×8–12 por pierna. Excelente para equilibrio y potencia unilateral.</p>
            </div>

            <div class="card">
              <div class="exercise-name">Peso muerto rumano</div>
              <p><strong>Técnica:</strong> cadera hacia atrás, espalda recta, sentir estiramiento en isquios, subir apretando glúteos.</p>
              <p class="meta">Sets/Reps: 3–4×6–10. Fortalece cadena posterior.</p>
            </div>

            <div class="card">
              <div class="exercise-name">Step-ups (unilateral)</div>
              <p><strong>Técnica:</strong> subir con talón, extensión completa de cadera; bajar controlado.</p>
              <p class="meta">Sets/Reps: 3×8–12 por pierna. Simula gesto de carrera en pendientes.</p>
            </div>

            <div class="card">
              <div class="exercise-name">Sentadilla búlgara</div>
              <p><strong>Técnica:</strong> pie trasero apoyado; bajar 90°; empujar con talón delantero.</p>
              <p class="meta">Sets/Reps: 3×8–10 por pierna. Corrige asimetrías.</p>
            </div>

            <div class="card">
              <div class="exercise-name">Elevaciones de talones (gemelos)</div>
              <p><strong>Técnica:</strong> sobre borde; subir a puntas, mantener 1–2s; bajar lentamente.</p>
              <p class="meta">Sets/Reps: 3×12–20 (resistencia). Variante: una pierna.</p>
            </div>
          </div>

          <div style="height:12px"></div>
          <div class="hint">
            <strong>Integración:</strong> 2 sesiones de fuerza (1 fuerza / 1 resistencia/potencia). Evita sesiones intensas 48–72 h antes de tiradas clave.
          </div>
        </article>

        <!-- TRUCOS -->
        <article id="trucos" class="card content-section" style="display:none">
          <h2>Trucos, checklist y recomendaciones</h2>
          <ul>
            <li class="muted">Practica geles y bebidas isotónicas durante las tiradas largas para saber cómo te sientan.</li>
            <li class="muted">Alterna dos pares de zapatillas: uno para volumen y otro para ritmos rápidos.</li>
            <li class="muted">Sueño 7–9 h en fases de volumen alto.</li>
            <li class="muted">Foam rolling y movilidad 10–15 min post sesión.</li>
            <li class="muted">Aumenta volumen <strong>máx. 10%/semana</strong> para prevenir sobrecargas.</li>
          </ul>

          <div style="height:12px"></div>
          <div class="small">¿Quieres que adapte sets/reps a tu peso, edad y km semanales? Dime esos datos y lo personalizo.</div>
        </article>

        <footer style="margin-top:14px" class="small">
          Puedes publicar este archivo tal cual en GitHub Pages o Netlify para compartir un enlace público.
        </footer>
      </section>
    </main>
  </div>

  <script>
    // ---- Tabs ----
    const items = document.querySelectorAll('.nav-item');
    const sections = document.querySelectorAll('.content-section');
    function setTab(name){
      items.forEach(i => i.classList.toggle('active', i.dataset.tab === name));
      sections.forEach(s => s.style.display = (s.id === name ? 'block' : 'none'));
      window.scrollTo({top:0, behavior:'smooth'});
    }
    items.forEach(i => i.addEventListener('click', ()=> setTab(i.dataset.tab)));
    // default
    setTab('nutricion');

    // ---- Descargar HTML ----
    document.getElementById('downloadHtmlBtn').addEventListener('click', () => {
      const blob = new Blob([document.documentElement.outerHTML], { type: 'text/html' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = 'marathon_pro.html';
      document.body.appendChild(a);
      a.click();
      a.remove();
      URL.revokeObjectURL(url);
      alert('Descargado: marathon_pro.html');
    });

    // ---- Imprimir / Guardar PDF ----
    document.getElementById('printBtn').addEventListener('click', () => {
      window.print();
    });
  </script>
</body>
</html>
