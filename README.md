# RadarGlobal
Repositorio de noticias y artículos sobre política internacional y geopolítica.

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="description" content="Radar Global: noticias internacionales y análisis geopolítico.">
  <title>Radar Global | Noticias y geopolítica</title>
  <style>
    :root {
      --navy: #183d50;
      --light: #d8e7e9;
      --paper: #f3f5f4;
      --ink: #18252b;
      --muted: #5b6b71;
      --white: #ffffff;
    }
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: Inter, system-ui, -apple-system, "Segoe UI", sans-serif;
      color: var(--ink);
      background: var(--paper);
      line-height: 1.6;
    }
    header {
      background: var(--navy);
      color: white;
      padding: 48px max(22px, calc((100% - 1100px)/2));
    }
    .eyebrow {
      text-transform: uppercase;
      letter-spacing: .15em;
      font-size: .75rem;
      opacity: .8;
    }
    h1 {
      font-size: clamp(2.5rem, 7vw, 4.5rem);
      letter-spacing: -.05em;
      line-height: 1.05;
      margin: 16px 0;
    }
    header p { max-width: 680px; color: #d8e7e9; }
    .chips { display: flex; gap: 8px; flex-wrap: wrap; margin-top: 24px; }
    .chip {
      border: 1px solid #ffffff55;
      border-radius: 30px;
      padding: 5px 12px;
      font-size: .8rem;
    }
    main { max-width: 1100px; margin: auto; padding: 28px 20px 60px; }
    .metrics {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
    }
    .metric, .filters, .card, .note {
      background: var(--white);
      border: 1px solid #dce4e4;
      border-radius: 15px;
    }
    .metric { padding: 17px; }
    .metric strong { display: block; font-size: 1.5rem; color: var(--navy); }
    .metric span { font-size: .83rem; color: var(--muted); }
    .section-head { margin: 32px 0 14px; }
    h2 { margin-bottom: 5px; }
    .section-head p { margin-top: 0; color: var(--muted); }
    .filters {
      padding: 16px;
      display: grid;
      grid-template-columns: 2fr 1fr 1fr;
      gap: 12px;
    }
    label { display: block; font-size: .8rem; font-weight: 700; margin-bottom: 5px; }
    input, select {
      width: 100%;
      padding: 11px;
      border: 1px solid #cbd8da;
      border-radius: 9px;
      background: white;
      color: var(--ink);
      font: inherit;
    }
    input:focus, select:focus, a:focus-visible {
      outline: 3px solid #75b8c5;
      outline-offset: 2px;
    }
    .result { color: var(--muted); font-size: .85rem; padding: 14px 2px; }
    .grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 15px; }
    .card { padding: 20px; min-width: 0; display: flex; flex-direction: column; }
    .tag {
      display: inline-block;
      background: var(--light);
      color: var(--navy);
      border-radius: 5px;
      padding: 4px 8px;
      font-size: .72rem;
      font-weight: 800;
      text-transform: uppercase;
    }
    .date { color: var(--muted); font-size: .78rem; }
    .card h3 { margin: 15px 0 8px; line-height: 1.3; }
    .card p { font-size: .92rem; }
    .label {
      text-transform: uppercase;
      letter-spacing: .08em;
      font-size: .7rem;
      font-weight: 800;
      color: var(--muted);
      margin-bottom: -8px;
    }
    .analysis { border-left: 3px solid #78aab5; padding-left: 12px; }
    .card-footer { border-top: 1px solid #e4eaea; padding-top: 13px; margin-top: auto; }
    a { color: #17617a; font-weight: 700; text-decoration: none; }
    a:hover { text-decoration: underline; }
    .note { margin-top: 24px; padding: 18px; font-size: .88rem; }
    .empty { grid-column: 1/-1; padding: 30px; text-align: center; }
    footer {
      border-top: 1px solid #dce4e4;
      padding: 24px;
      text-align: center;
      color: var(--muted);
      font-size: .8rem;
    }
    @media(max-width:700px) {
      .grid, .filters { grid-template-columns: 1fr; }
      .metrics { grid-template-columns: 1fr 1fr; }
      .metric:last-child { grid-column: 1/-1; }
    }
  </style>
</head>
<body>
<header>
  <div class="eyebrow">Briefing · Política mundial · Análisis</div>
  <h1>Radar Global</h1>
  <p>Un espacio para seguir los acontecimientos internacionales, comprender sus protagonistas e interpretar sus implicancias para las Relaciones Internacionales.</p>
  <div class="chips">
    <span class="chip">Cobertura global</span>
    <span class="chip">Geopolítica</span>
    <span class="chip">Hechos y análisis</span>
  </div>
</header>

<main>
  <section class="metrics">
    <div class="metric"><strong id="total">0</strong><span>fichas publicadas</span></div>
    <div class="metric"><strong>Global</strong><span>Enfoque internacional</span></div>
    <div class="metric"><strong>RI</strong><span>Perspectiva académica</span></div>
  </section>

  <section class="section-head">
    <h2>Repositorio de noticias</h2>
    <p>Buscá por tema, actor o palabra clave y filtrá los resultados.</p>
  </section>

  <section class="filters">
    <div>
      <label for="search">Buscar</label>
      <input id="search" type="search" placeholder="Ej. China, energía, diplomacia">
    </div>
    <div>
      <label for="region">Región</label>
      <select id="region">
        <option value="">Todas las regiones</option>
        <option>Asia</option><option>Europa</option>
        <option>América Latina</option><option>América del Norte</option>
        <option>África</option><option>Medio Oriente</option>
      </select>
    </div>
    <div>
      <label for="topic">Área temática</label>
      <select id="topic">
        <option value="">Todas las áreas</option>
        <option>Geopolítica</option><option>Economía</option>
        <option>Diplomacia</option><option>Seguridad</option>
        <option>Comercio</option><option>Tecnología</option>
      </select>
    </div>
  </section>

  <div class="result" id="result" aria-live="polite"></div>
  <section class="grid" id="news"></section>

  <section class="section-head">
    <h2>Fuentes internacionales</h2>
    <p>Acceso a medios y búsquedas de noticias que se actualizan externamente.</p>
  </section>

  <section class="grid">
    <article class="card">
      <span class="tag">Global</span>
      <h3>Noticias internacionales</h3>
      <p>Actualidad mundial a través de distintas fuentes periodísticas.</p>
      <div class="card-footer"><a target="_blank" rel="noopener noreferrer" href="https://news.google.com/">Explorar Google News ↗</a></div>
    </article>
    <article class="card">
      <span class="tag">Geopolítica</span>
      <h3>Política y seguridad internacional</h3>
      <p>Seguimiento de las relaciones entre potencias, conflictos y diplomacia.</p>
      <div class="card-footer"><a target="_blank" rel="noopener noreferrer" href="https://news.google.com/search?q=geopolitics%20international%20security">Consultar noticias ↗</a></div>
    </article>
    <article class="card">
      <span class="tag">Economía</span>
      <h3>Economía internacional</h3>
      <p>Comercio, energía, mercados y geoeconomía.</p>
      <div class="card-footer"><a target="_blank" rel="noopener noreferrer" href="https://news.google.com/search?q=global%20economy%20international%20trade">Consultar noticias ↗</a></div>
    </article>
    <article class="card">
      <span class="tag">Asia y tecnología</span>
      <h3>China y Estados Unidos</h3>
      <p>Competencia tecnológica, inteligencia artificial y política industrial.</p>
      <div class="card-footer"><a target="_blank" rel="noopener noreferrer" href="https://news.google.com/search?q=China%20US%20technology%20competition">Consultar noticias ↗</a></div>
    </article>
    <article class="card">
      <span class="tag">Diplomacia</span>
      <h3>Organismos internacionales</h3>
      <p>Naciones Unidas, cooperación multilateral y negociaciones internacionales.</p>
      <div class="card-footer"><a target="_blank" rel="noopener noreferrer" href="https://news.un.org/es/">ONU Noticias ↗</a></div>
    </article>
    <article class="card">
      <span class="tag">América Latina</span>
      <h3>La región en el mundo</h3>
      <p>Política exterior latinoamericana, integración y vínculos con otras potencias.</p>
      <div class="card-footer"><a target="_blank" rel="noopener noreferrer" href="https://news.google.com/search?q=Latin%20America%20foreign%20policy">Consultar noticias ↗</a></div>
    </article>
  </section>

  <aside class="note">
    <strong>Nota editorial:</strong> las fichas marcadas como ejemplos sirven para probar el funcionamiento del sitio y no son noticias verificadas. Antes de publicar información como actualidad, comprobá la fecha, el contenido y la fuente original. Los enlaces de esta página abren sitios externos; no importan automáticamente sus noticias al repositorio.
  </aside>
</main>

<footer>
  RADAR GLOBAL · Noticias internacionales y Relaciones Internacionales
</footer>

<script>
const news = [
  {
    title: "Ejemplo: competencia tecnológica entre China y Estados Unidos",
    region: "Asia", topic: "Tecnología",
    date: "Ficha de demostración",
    summary: "Esta ficha muestra cómo presentar un acontecimiento internacional y sus actores. Reemplazá este texto por un resumen basado en una fuente periodística verificable.",
    actors: "China, Estados Unidos y empresas tecnológicas.",
    analysis: "Analizá cómo la competencia tecnológica influye en la autonomía estratégica, las cadenas de valor y la distribución internacional del poder.",
    source: "Buscar fuentes", url: "https://news.google.com/search?q=China%20US%20technology"
  },
  {
    title: "Ejemplo: comercio y economía internacional",
    region: "Europa", topic: "Economía",
    date: "Ficha de demostración",
    summary: "Utilizá este espacio para describir un hecho económico confirmado y distinguir los datos publicados de las proyecciones.",
    actors: "Gobiernos, organismos económicos y socios comerciales.",
    analysis: "Considerá las consecuencias de las decisiones económicas para la interdependencia y la cooperación internacional.",
    source: "Buscar fuentes", url: "https://news.google.com/search?q=international%20trade"
  },
  {
    title: "Ejemplo: diplomacia y cooperación multilateral",
    region: "América Latina", topic: "Diplomacia",
    date: "Ficha de demostración",
    summary: "Incorporá aquí los detalles de una negociación, cumbre o decisión diplomática, citando la fuente y su fecha.",
    actors: "Estados, organismos internacionales y representantes diplomáticos.",
    analysis: "Examiná los intereses de los actores, las posibilidades de cooperación y los límites de los acuerdos.",
    source: "Noticias ONU", url: "https://news.un.org/es/"
  }
];

const $ = id => document.getElementById(id);
function render() {
  const q = $("search").value.trim().toLocaleLowerCase("es");
  const r = $("region").value;
  const t = $("topic").value;
  const filtered = news.filter(n =>
    (!r || n.region === r) &&
    (!t || n.topic === t) &&
    (!q || [n.title,n.summary,n.actors,n.analysis,n.region,n.topic]
      .join(" ").toLocaleLowerCase("es").includes(q))
  );

  $("total").textContent = news.length;
  $("result").textContent = `${filtered.length} fichas encontradas`;
  $("news").innerHTML = filtered.length ? filtered.map(n => `
    <article class="card">
      <div><span class="tag">${n.topic}</span>
      <span class="date"> · ${n.date}</span></div>
      <h3>${n.title}</h3>
      <div class="label">Resumen</div><p>${n.summary}</p>
      <div class="label">Actores involucrados</div><p>${n.actors}</p>
      <div class="label">Análisis geopolítico</div><p class="analysis">${n.analysis}</p>
      <div class="card-footer"><a href="${n.url}" target="_blank" rel="noopener noreferrer">Fuente: ${n.source} ↗</a></div>
    </article>`).join("") :
    '<div class="empty">No hay resultados. Probá cambiar los filtros.</div>';
}
["search","region","topic"].forEach(id => $(id).addEventListener("input", render));
render();
</script>
</body>
</html>
