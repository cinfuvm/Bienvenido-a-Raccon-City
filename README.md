<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Resident Evil 2 — Revista Fan (Nintendo 64)</title>
  <meta name="description" content="Revista fan centrada en Resident Evil 2 para Nintendo 64: portada, personajes con imagen y descripción al clic, armas con imagen, enemigos/objetos/trucos y datos sin imágenes innecesarias, gameplay, momento tenso y referencias." />
  <link rel="icon" href="/favicon.ico" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Inter:wght@400;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg:#111217; --ink:#f3f3f6; --muted:#c7c8ce; --accent:#e51a2d;
      --card:#181a20; --line:rgba(255,255,255,.13); --radius:14px; --w:1000px;
      --thumbH:130px; --thumbH-m:120px; --armaH:130px; --armaH-m:110px;
      --secY:68px;         /* padding vertical base de secciones */
      --secYnext:100px;    /* padding-top extra al iniciar cada nueva sección */
    }
    *{box-sizing:border-box}
    body{margin:0; font-family:Inter, system-ui, Segoe UI, Roboto, Helvetica, Arial, sans-serif; color:var(--ink); background:var(--bg)}
    img{max-width:100%; height:auto; display:block}
    a{color:var(--ink); text-decoration:none}
    .wrap{max-width:var(--w); margin:auto; padding:0 16px}

    
    header{position:sticky; top:0; z-index:50; background:rgba(0,0,0,.55); border-bottom:1px solid var(--line); backdrop-filter:blur(6px)}
    .top{display:flex; align-items:center; justify-content:space-between; gap:10px; padding:10px 0}
    .brand{display:flex; align-items:center; gap:8px}
    .brand .dot{width:18px; height:18px; border-radius:6px; background:radial-gradient(circle at 30% 30%, #ff5858, var(--accent))}
    .brand h1{margin:0; font:26px/1 "Bebas Neue", sans-serif; letter-spacing:.5px}
    nav ul{margin:0; padding:0; list-style:none; display:flex; gap:12px; flex-wrap:wrap}
    nav a{padding:6px 10px; border-radius:10px; border:1px solid transparent; transition:.15s}
    nav a:hover{border-color:var(--line); background:rgba(255,255,255,.06); transform:translateY(-1px)}

    
    .hero{position:relative; border-bottom:1px solid var(--line)}
    .hero .cover{ position:relative; height:56svh; overflow:hidden; border-bottom:1px solid var(--line); }
    .hero img.hero-cover{width:100%; height:100%; object-fit:cover; object-position:center}
    .hero .overlay{position:absolute; inset:0; background:linear-gradient(180deg, rgba(0,0,0,.15), rgba(0,0,0,.75) 70%)}
    .hero .titlebox{position:absolute; left:0; right:0; bottom:0; padding:18px 0 20px}
    .hero h2{margin:0; font:clamp(42px,7vw,84px)/.9 "Bebas Neue", sans-serif; letter-spacing:.6px}
    .chips{display:flex; flex-wrap:wrap; gap:8px; margin-top:6px}
    .chip{padding:6px 10px; border-radius:999px; border:1px solid var(--line); background:rgba(0,0,0,.35); font-weight:700; font-size:12px; transition:.15s}
    .chip:hover{transform:translateY(-1px) scale(1.02)}

    
    main section{padding:var(--secY) 0 calc(var(--secY) - 8px);}
    main section + section{padding-top:var(--secYnext);}  /* espacio visible antes del siguiente título */
    h3.section{margin:0 0 18px; font:32px/1 "Bebas Neue", sans-serif; display:flex; align-items:center; gap:10px}
    h3.section::before{content:""; width:8px; height:20px; border-radius:6px; background:linear-gradient(180deg, var(--accent), #ff6d6d)}
    .card{background:var(--card); border:1px solid var(--line); border-radius:var(--radius); padding:14px}
    .muted{color:var(--muted)}

    
    .grid-2{display:grid; gap:16px}
    @media(min-width:860px){ .grid-2{grid-template-columns:2fr 1fr} }

    .grid-cards{display:grid; gap:12px; grid-template-columns:repeat(auto-fit, minmax(230px, 1fr))}
    .info-card{border:1px solid var(--line); background:var(--card); border-radius:12px; overflow:hidden; display:flex; flex-direction:column; transition:transform .2s ease, box-shadow .2s ease}
    .info-card:hover{transform:translateY(-2px); box-shadow:0 10px 24px rgba(0,0,0,.25)}
    .i-img{width:100%; height:var(--armaH); object-fit:cover; margin:0}
    .i-body{padding:12px 12px 14px}  /* espacio interno para armas */
    .i-title{margin:0 0 6px}
    @media(max-width:640px){ .i-img{height:var(--armaH-m)} }

    
    .char-grid{display:grid; gap:12px; grid-template-columns:repeat(auto-fit, minmax(220px, 1fr))}
    .char{scroll-margin-top:90px}
    .char details{border:1px solid var(--line); background:var(--card); border-radius:12px; overflow:hidden; transition:box-shadow .2s}
    .char details:hover{box-shadow:0 10px 24px rgba(0,0,0,.25)}
    .char summary{list-style:none; cursor:pointer; padding:0; outline:none}
    .char summary::-webkit-details-marker{display:none}
    .char .thumb{height:var(--thumbH); overflow:hidden; background:#000; display:flex; align-items:center; justify-content:center; position:relative; padding:6px}
    .char .thumb img{max-height:100%; width:auto; object-fit:contain; transition:transform .2s ease}
    .char .thumb:hover img{transform:scale(1.02)}
    .char .thumb .hint{position:absolute; right:8px; bottom:8px; font-size:12px; background:rgba(0,0,0,.45); padding:4px 8px; border-radius:8px; border:1px solid var(--line)}
    .char h4{margin:10px 10px 0; font:24px/1 "Bebas Neue", sans-serif}
    .char p.role{margin:8px 10px; color:var(--muted)}
    .char .more-btn{margin:0 10px 12px; display:inline-block; padding:8px 10px; border-radius:8px; border:1px solid var(--line); font-weight:700; background:transparent}
    .char .more-btn::after{content:"Ver descripción"}
    .char details[open] .more-btn::after{content:"Ocultar descripción"}
    .char .panel{display:grid; grid-template-rows:0fr; transition:grid-template-rows .35s ease, opacity .25s ease; border-top:1px solid var(--line); background:rgba(255,255,255,.03); opacity:.0}
    .char .panel>div{overflow:hidden; padding:10px 12px}
    .char details[open] .panel{grid-template-rows:1fr; opacity:1}
    @media(max-width:640px){ .char .thumb{height:var(--thumbH-m)} }

    
    .moment{display:grid; gap:14px}
    @media(min-width:860px){ .moment{grid-template-columns:1.1fr 1fr} }
    .shot{border:1px solid var(--line); border-radius:12px; overflow:hidden; background:#000}
    .shot img{width:100%; height:320px; object-fit:cover}
    .story{border:1px solid var(--line); border-radius:12px; background:var(--card); padding:14px}
    .story p{margin:0 0 10px}

   
    .video{position:relative; width:100%; max-width:var(--w); margin:0 auto}
    .video::before{content:""; display:block; padding-top:56.25%}
    .video>iframe{position:absolute; inset:0; width:100%; height:100%; border:0; border-radius:12px; border:1px solid var(--line)}

    footer{border-top:1px solid var(--line); padding:18px 0; text-align:center; color:var(--muted)}

    /* Aparición suave */
    .reveal{opacity:.001; transform:translateY(8px); transition:opacity .35s ease, transform .35s ease}
    .reveal.in{opacity:1; transform:none}
  </style>
</head>
<body>
  
  <header>
    <div class="wrap top">
      <div class="brand"><span class="dot"></span><h1>Resident Evil 2 · N64</h1></div>
      <nav aria-label="Principal">
        <ul>
          <li><a href="#intro">Inicio</a></li>
          <li><a href="#dossier">Contexto</a></li>
          <li><a href="#personajes">Personajes</a></li>
          <li><a href="#armas">Armas</a></li>
          <li><a href="#enemigos">Enemigos</a></li>
          <li><a href="#objetos">Objetos</a></li>
          <li><a href="#datos">Datos</a></li>
          <li><a href="#momento">Mi momento tenso</a></li> <!-- cambiado -->
          <li><a href="#gameplay">Gameplay</a></li>
          <li><a href="#curiosidades">Curiosidades</a></li>
          <li><a href="#referencias">Referencias</a></li>
        </ul>
      </nav>
    </div>
  </header>

 
  <section class="hero reveal" id="hero">
    <div class="cover">
      <img class="hero-cover" src="Portada.jpg" alt="Portada RE2 (reemplaza por tu imagen)">
      <div class="overlay"></div>
      <div class="titlebox">
        <div class="wrap">
          <h2>Bienvenido a <span style="color:var(--accent)">Raccoon City</span></h2>
          <div class="chips">
            <span class="chip">Nintendo 64 (1999)</span>
            <span class="chip">Terror</span>
            <span class="chip">Tips y Cositas</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <main>
    
    <section id="intro" class="wrap reveal">
      <h3 class="section">Un par de datitos</h3>
      <div class="card">
        <p><strong>Esta página se centra en la versión de Nintendo 64</strong> de <em>Resident Evil 2</em>. Este port comprimió dos discos de PS1 en un cartucho de 64&nbsp;MB.</p>
        <ul style="margin:8px 0 0; padding-left:18px" class="muted">
          <li><strong>Núcleo:</strong> cámaras fijas, inventario limitado y rutas A/B.</li>
          <li><strong>Ritmo:</strong> explora, resuelve puzles y escapa (¡hola, Mr. X!).</li>
        </ul>
      </div>
    </section>

    <section id="dossier" class="wrap reveal">
      <h3 class="section"> Contexto - La noche del desastre</h3>
      <div class="grid-2">
        <article class="card">
          <p>Claire busca a su hermano Chris. Leon llega a su primer día en el R.P.D. Ambos quedan atrapados en Raccoon City por el <strong>T-Virus</strong>. La historia se vive en paralelo y afecta qué objetos y escenas encontrarás.</p>
          <p class="muted"><strong>Trama en una línea:</strong> escapar, exponer a Umbrella y sobrevivir a bioarmas como el Tyrant y las mutaciones G.</p>
        </article>
        <aside>
          <div class="card">
            <p class="muted"><strong>Ficha rápida (N64):</strong> Port por Angel Studios (con Capcom Studio 3 y Factor 5).</p>
            <ul class="muted" style="margin:8px 0 0; padding-left:18px">
              <li><strong>Diseño:</strong> cámaras fijas + fondos prerrenderizados.</li>
              <li><strong>Progreso:</strong> llaves de naipes, medallones y puzles.</li>
            </ul>
          </div>
        </aside>
      </div>
    </section>

    
    <section id="personajes" class="wrap reveal">
      <h3 class="section">Personajes</h3>
      <ul class="char-grid" style="padding:0; list-style:none">
        <!-- (mismas tarjetas que tenías) -->
        <li class="char">
          <details>
            <summary>
              <div class="thumb"><img src="leon-s-kennedy.png" alt="Leon S. Kennedy"><span class="hint"></span></div>
              <h4>Leon S. Kennedy</h4>
              <p class="role">Novato del R.P.D. · Primer día</p>
              <span class="more-btn"></span>
            </summary>
            <div class="panel"><div>
              <p>¡Pro tip! Templado en el caos. Sus rutas priorizan armas de fuego y momentos con el Tyrant.</p>
              <p class="muted"><strong>Consejo:</strong> apunta a las piernas para ralentizar. Guarda granadas flash.</p>
            </div></div>
          </details>
        </li>

        <li class="char">
          <details>
            <summary>
              <div class="thumb"><img src="claire.jpg" alt="Claire Redfield"><span class="hint"></span></div>
              <h4>Claire Redfield</h4>
              <p class="role">Estudiante y motociclista</p>
              <span class="more-btn"></span>
            </summary>
            <div class="panel"><div>
              <p>¡Valiente total! Accede al lanzagranadas y protagoniza secciones con Sherry.</p>
              <p class="muted"><strong>Consejo:</strong> alterna munición incendiaria/ácida según el enemigo.</p>
            </div></div>
          </details>
        </li>

        <li class="char">
          <details>
            <summary>
              <div class="thumb"><img src="Adawong.jpg" alt="Ada Wong"><span class="hint"></span></div>
              <h4>Ada Wong</h4>
              <p class="role">Aliada misteriosa</p>
              <span class="more-btn"></span>
            </summary>
            <div class="panel"><div>
              <p>¡Giro tras giro! Sus acciones impactan la ruta de Leon.</p>
              <p class="muted"><strong>Pista:</strong> explora a fondo: siempre hay señales.</p>
            </div></div>
          </details>
        </li>

        <li class="char">
          <details>
            <summary>
              <div class="thumb"><img src="mr x.jpg" alt="Tyrant T-103 (Mr. X)"><span class="hint"></span></div>
              <h4>“Mr. X” (T-103)</h4>
              <p class="role">Bioarma de Umbrella</p>
              <span class="more-btn"></span>
            </summary>
            <div class="panel"><div>
              <p>¡Se siente en los pasos! Perseguidor implacable: condiciona rutas y ritmo.</p>
              <p class="muted"><strong>Consejo:</strong> evita duelos largos; usa puertas y atajos.</p>
            </div></div>
          </details>
        </li>

        
        <li class="char">
          <details>
            <summary>
              <div class="thumb"><img src="sherry.jpg" alt="Sherry Birkin"><span class="hint"></span></div>
              <h4>Sherry Birkin</h4>
              <p class="role">Niña atrapada en el brote</p>
              <span class="more-btn"></span>
            </summary>
            <div class="panel"><div><p>Momentos de sigilo y rescate junto a Claire. ¡Tensión pura!</p></div></div>
          </details>
        </li>

        <li class="char">
          <details>
            <summary>
              <div class="thumb"><img src="william.jpg" alt="William Birkin"><span class="hint"></span></div>
              <h4>William Birkin</h4>
              <p class="role">Científico · Mutación G</p>
              <span class="more-btn"></span>
            </summary>
            <div class="panel"><div><p>Responsable del Proyecto G. Su transformación muestra el precio del experimento.</p></div></div>
          </details>
        </li>

        <li class="char">
          <details>
            <summary>
              <div class="thumb"><img src="Annette.webp" alt="Annette Birkin"><span class="hint"></span></div>
              <h4>Annette Birkin</h4>
              <p class="role">Investigadora · Madre de Sherry</p>
              <span class="more-btn"></span>
            </summary>
            <div class="panel"><div><p>Entre la culpa y el deber. Conoce secretos clave del laboratorio y el virus G.</p></div></div>
          </details>
        </li>

        <li class="char">
          <details>
            <summary>
              <div class="thumb"><img src="marvin.jpg" alt="Marvin Branagh"><span class="hint"></span></div>
              <h4>Marvin Branagh</h4>
              <p class="role">Oficial del R.P.D.</p>
              <span class="more-btn"></span>
            </summary>
            <div class="panel"><div><p>Apoyo temprano en la comisaría. ¡Un héroe silencioso!</p></div></div>
          </details>
        </li>

        <li class="char">
          <details>
            <summary>
              <div class="thumb"><img src="brian.jpg" alt="Brian Irons"><span class="hint"></span></div>
              <h4>Brian Irons</h4>
              <p class="role">Jefe de policía</p>
              <span class="more-btn"></span>
            </summary>
            <div class="panel"><div><p>Oscuro y corrupto. Añade crudeza al colapso de la ciudad.</p></div></div>
          </details>
        </li>

        <li class="char">
          <details>
            <summary>
              <div class="thumb"><img src="hunk.jpg" alt="HUNK"><span class="hint"></span></div>
              <h4>HUNK</h4>
              <p class="role">Operativo de seguridad</p>
              <span class="more-btn"></span>
            </summary>
            <div class="panel"><div><p>“El cuarto superviviente”. Desafío intenso de principio a fin.</p></div></div>
          </details>
        </li>

        <li class="char">
          <details>
            <summary>
              <div class="thumb"><img src="descarga.jpg" alt="Tofu"><span class="hint"></span></div>
              <h4>Tofu</h4>
              <p class="role">Modo extra (broma)</p>
              <span class="more-btn"></span>
            </summary>
            <div class="panel"><div><p>¡Memorable! Pone a prueba tu dominio del mapa bajo condiciones únicas.</p></div></div>
          </details>
        </li>
      </ul>
    </section>

    
    <section id="armas" class="wrap reveal">
      <h3 class="section">Armas</h3>
      <div class="grid-cards">
        <article class="info-card"><img class="i-img" src="matilda.webp" alt="Pistola 9mm"><div class="i-body"><h4 class="i-title">Pistolas 9mm</h4><p>Base de ambos protagonistas. Precisas y con munición común. Ideales para controlar zombis.</p><div class="i-meta"><span class="tag">N64: misma lógica</span></div></div></article>
        <article class="info-card"><img class="i-img" src="escopeta.jpg" alt="Escopeta"><div class="i-body"><h4 class="i-title">Escopeta</h4><p>Daño alto a corta distancia. Perfecta contra grupos o lickers a quemarropa.</p><div class="i-meta"><span class="tag">Apunta hacia arriba</span></div></div></article>
        <article class="info-card"><img class="i-img" src="lanzagranadas.jpg" alt="Lanzagranadas"><div class="i-body"><h4 class="i-title">Lanzagranadas (Claire)</h4><p>Munición ácida/incendiaria para adaptarte al enemigo. Muy útil en el laboratorio.</p><div class="i-meta"><span class="tag">Selección de munición</span></div></div></article>
        <article class="info-card"><img class="i-img" src="magnum.jpg" alt="Magnum"><div class="i-body"><h4 class="i-title">Magnum</h4><p>Golpea durísimo, pero es escasa. Guárdala para jefes o emergencias.</p><div class="i-meta"><span class="tag">Jefes</span></div></div></article>
        <article class="info-card"><img class="i-img" src="ballesta.jpg" alt="Ballesta"><div class="i-body"><h4 class="i-title">Ballesta (Claire)</h4><p>Dispara tres saetas. Buen control en pasillos cortos.</p><div class="i-meta"><span class="tag">Tri-salva</span></div></div></article>
        <article class="info-card"><img class="i-img" src="lanzallamas.jpg" alt="Lanzallamas"><div class="i-body"><h4 class="i-title">Lanzallamas</h4><p>Armas situacionales muy efectivas contra tipos específicos de criatura.</p><div class="i-meta"><span class="tag">Contra plantas</span></div></div></article>
      </div>
    </section>

    
    <section id="enemigos" class="wrap reveal">
      <h3 class="section">Enemigos & Criaturas</h3>
      <div class="grid-cards">
        <article class="info-card"><div class="i-body"><h4 class="i-title">Zombi clásico</h4><p>Lentos pero numerosos. Controla con disparos a cabeza o piernas.</p><div class="i-meta"><span class="tag">Consejo: piernas</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Licker</h4><p>No ve, pero oye. Camina para no hacer ruido y remata de cerca.</p><div class="i-meta"><span class="tag">Sigilo</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Perros (Cerberus)</h4><p>Rápidos y en grupo. La escopeta limpia bien.</p><div class="i-meta"><span class="tag">Corta distancia</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Cuervos</h4><p>Molestos. Si puedes, ignóralos para ahorrar munición.</p><div class="i-meta"><span class="tag">Ahorro</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Arañas</h4><p>Veneno y alcance. Evítalas o usa armas de área.</p><div class="i-meta"><span class="tag">Área</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Plantas (Ivy)</h4><p>Vulnerables al fuego y ácido. No las dejes acercarse.</p><div class="i-meta"><span class="tag">Fuego/Ácido</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">G-engendros</h4><p>Pequeños pero peligrosos en grupo. Avanza con cuidado.</p><div class="i-meta"><span class="tag">Emboscadas</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Cocodrilo gigante</h4><p>Encuentro específico: observa el entorno y actúa rápido.</p><div class="i-meta"><span class="tag">Evento</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Tyrant T-103 (Mr. X)</h4><p>Te acosa en la comisaría. Usa atajos y puertas para perderlo.</p><div class="i-meta"><span class="tag">No malgastes balas</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Mutaciones de Birkin</h4><p>Jefes por fases. Aprende patrones y guarda munición pesada.</p><div class="i-meta"><span class="tag">Fases</span></div></div></article>
      </div>
    </section>

    
    <section id="objetos" class="wrap reveal">
      <h3 class="section">Objetos & Curación</h3>
      <div class="grid-cards">
        <article class="info-card"><div class="i-body"><h4 class="i-title">Hierba verde</h4><p>Cura básica. Combina para mejores efectos.</p><div class="i-meta"><span class="tag">Base</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Hierba roja</h4><p>No cura sola; potencia la mezcla con verde.</p><div class="i-meta"><span class="tag">Potenciador</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Hierba azul</h4><p>Antídoto contra veneno. Úsala en mezcla.</p><div class="i-meta"><span class="tag">Antídoto</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Spray de primeros auxilios</h4><p>Cura completa de emergencia. Úsalo con cabeza.</p><div class="i-meta"><span class="tag">Cura total</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Cintas de tinta</h4><p>Guardado clásico en máquinas de escribir. Adminístralas.</p><div class="i-meta"><span class="tag">Guardar</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Llaves de naipes</h4><p>Diamante, pica, trébol y corazón abren alas de la comisaría.</p><div class="i-meta"><span class="tag">Progreso</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Medallones/enchufes</h4><p>Ítems de puzle que desbloquean nuevas áreas.</p><div class="i-meta"><span class="tag">Puzles</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Encendedor / Llave especial</h4><p>Herramientas clave para acciones puntuales.</p><div class="i-meta"><span class="tag">Contextual</span></div></div></article>
      </div>
      <div class="card" style="margin-top:12px">
        <div class="chips" style="gap:8px; flex-wrap:wrap">
          <span class="chip">¡Mezclas top!</span>
          <span class="chip">Verde + Roja = cura total</span>
          <span class="chip">Verde + Azul = cura + antídoto</span>
        </div>
      </div>
    </section>

    
    <section id="datos" class="wrap reveal">
      <h3 class="section">Datos interesantes</h3>
      <div class="grid-cards">
        <article class="info-card"><div class="i-body"><h4 class="i-title">Prototipo “1.5”</h4><p>La versión inicial se reinició y dio lugar al RE2 final.</p><div class="i-meta"><span class="tag">Reinicio</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Puertas = carga</h4><p>Las animaciones de puertas hacían de pantalla de carga creativa.</p><div class="i-meta"><span class="tag">Truco técnico</span></div></div></article>
        <article class="info-card"><div class="i-body"><h4 class="i-title">Comisaría-museo</h4><p>Explica la estética de salas, vitrales y símbolos.</p><div class="i-meta"><span class="tag">Ambientación</span></div></div></article>
      </div>
    </section>

    
    <section id="momento" class="wrap reveal">
      <h3 class="section">Mi primer momento tenso en el juego</h3>
      <div class="moment">
      
        <figure class="shot">
          <img src="Licker.webp" alt="Primer encuentro con un Licker (reemplaza por tu imagen)">
        </figure>
        <article class="story">
          <p><strong>¡Me llevé un gran susto!</strong> Porque venía tranquilo por el pasillo cuando escuché el <em>ras-ras</em> en el techo. Miré arriba y… <strong>¡Un Feo Licker!</strong></p>
          <p>Me congelé por  un segundo. Aprendí que caminar despacio ayuda (no ven, pero sí oyen). Dos pasos atrás, escopeta lista… y de milagro salí vivo.</p>
          <p class="muted">Si lo ves a distancia, avanza lento y remata a quemarropa. Ahorras balas y nervios.</p>
        </article>
      </div>
    </section>

    
    <section id="gameplay" class="wrap reveal">
      <h3 class="section">Gameplay (Nintendo 64)</h3>
      <div class="card" style="margin-bottom:10px">
        <p class="muted">Gameplay completo de Resident Evil 2 (Y si, es el juego completo).</p>
      </div>
      <div class="video">
        <iframe src="https://www.youtube.com/embed/cOEB3TGQAIc" title="Resident Evil 2 (N64) - Gameplay" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen loading="lazy"></iframe>
      </div>
      <p class="muted" style="margin-top:8px">Enlace directo: <a href="https://www.youtube.com/watch?v=cOEB3TGQAIc" target="_blank" rel="noopener">YouTube — Longplay RE2 N64</a></p>
    </section>

    
    <section id="curiosidades" class="wrap reveal">
      <h3 class="section">Curiosidades</h3>
      <div class="card">
        <details><summary>¿Qué es el Sistema A/B?</summary><p>Completar con un personaje abre la ruta del otro con cambios de objetos, jefes y escenas.</p></details>
        <details><summary>Consejo rápido</summary><p>Deja siempre un espacio libre en el inventario para llaves o ítems clave.</p></details>
      </div>
    </section>

    
    <section id="referencias" class="wrap reveal">
      <h3 class="section">Referencias</h3>
      <div class="card">
        <ul style="margin:0; padding-left:18px">
          <li>Wikipedia — <a href="https://en.wikipedia.org/wiki/Resident_Evil_2#Nintendo_64" target="_blank" rel="noopener">Resident Evil 2 · Nintendo 64</a></li>
          <li>GameSpot (1999) — <a href="https://www.gamespot.com/reviews/resident-evil-2-review/1900-2543705/" target="_blank" rel="noopener">Reseña N64</a></li>
          <li>GamesRadar — <a href="https://www.gamesradar.com/games/survival-horror/how-resident-evil-2-came-to-nintendo-64-despite-capcoms-doubts-i-recall-having-daily-meetings-and-someone-asked-should-we-be-worried/" target="_blank" rel="noopener">Historia del port</a></li>
          <li>TCRF — <a href="https://tcrf.net/Resident_Evil_2_(Nintendo_64)" target="_blank" rel="noopener">Detalles técnicos de N64</a></li>
          <li>Gameplay — <a href="https://www.youtube.com/watch?v=cOEB3TGQAIc" target="_blank" rel="noopener">Longplay RE2 (N64)</a></li>
        </ul>
      </div>
    </section>
  </main>

  <footer>
    <div class="wrap">
      <small>© <span id="anio"></span> · Sitio creado por <strong>Jeremias Carrasco</strong> · Proyecto académico de fans — Marcas pertenecen a sus dueños (Capcom, etc.).</small>
    </div>
  </footer>

  <script>
    
    document.getElementById('anio').textContent = new Date().getFullYear();

    
    const obs = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); obs.unobserve(e.target);} });
    }, {threshold:.18});
    document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));

    
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', (e)=>{
        const id = a.getAttribute('href'); const target = document.querySelector(id);
        if(target){ e.preventDefault(); target.scrollIntoView({behavior:'smooth'}); }
      });
    });
  </script>
</body>
</html>
