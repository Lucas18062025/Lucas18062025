<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>README Preview · GitHub Dark · Lucas Villagra</title>
<script src="https://cdn.jsdelivr.net/npm/marked@12.0.0/marked.min.js"></script>
<style>
  /* === GitHub Dark Default theme (recreated) === */
  :root {
    --bg-canvas: #0d1117;
    --bg-overlay: #161b22;
    --bg-inset: #010409;
    --bg-subtle: #161b22;
    --border-default: #30363d;
    --border-muted: #21262d;
    --fg-default: #c9d1d9;
    --fg-muted: #8b949e;
    --fg-subtle: #6e7681;
    --accent-fg: #58a6ff;
    --success-fg: #3fb950;
    --danger-fg: #f85149;
    --cyan: #00e5ff;
    --violet: #a78bfa;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  html, body {
    background: var(--bg-canvas);
    color: var(--fg-default);
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Noto Sans", Helvetica, Arial, sans-serif;
    font-size: 16px;
    line-height: 1.5;
    min-height: 100vh;
  }

  /* === Top bar (simula GitHub header) === */
  .gh-topbar {
    background: var(--bg-inset);
    border-bottom: 1px solid var(--border-default);
    padding: 12px 24px;
    position: sticky;
    top: 0;
    z-index: 10;
  }
  .gh-topbar .repo-path {
    color: var(--fg-default);
    font-size: 14px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .gh-topbar .repo-path .octicon { color: var(--fg-muted); }
  .gh-topbar .repo-path a { color: var(--accent-fg); text-decoration: none; }
  .gh-topbar .repo-path a:hover { text-decoration: underline; }
  .gh-topbar .repo-path .sep { color: var(--fg-muted); margin: 0 2px; }
  .gh-topbar .badge {
    display: inline-block;
    padding: 2px 8px;
    font-size: 12px;
    font-weight: 500;
    color: var(--cyan);
    border: 1px solid var(--border-default);
    border-radius: 999px;
    margin-left: auto;
    background: rgba(0, 229, 255, 0.08);
  }

  /* === Main container === */
  .gh-container {
    max-width: 1280px;
    margin: 0 auto;
    padding: 32px 24px;
    display: grid;
    grid-template-columns: 1fr;
    gap: 24px;
  }
  @media (min-width: 1012px) {
    .gh-container { grid-template-columns: 1fr 296px; }
    .gh-sidebar { display: block !important; }
  }

  /* === README card === */
  .readme-card {
    background: var(--bg-canvas);
    border: 1px solid var(--border-default);
    border-radius: 8px;
    overflow: hidden;
  }
  .readme-header {
    background: var(--bg-overlay);
    border-bottom: 1px solid var(--border-default);
    padding: 16px 20px;
    display: flex;
    align-items: center;
    gap: 8px;
    color: var(--fg-default);
    font-size: 14px;
    font-weight: 600;
  }
  .readme-header svg { fill: currentColor; }
  .readme-body {
    padding: 32px;
    overflow-x: auto;
  }

  /* === Markdown body (GitHub styles) === */
  .markdown-body {
    color: var(--fg-default);
    font-size: 16px;
    line-height: 1.5;
    word-wrap: break-word;
  }
  .markdown-body > *:first-child { margin-top: 0 !important; }
  .markdown-body > *:last-child { margin-bottom: 0 !important; }

  .markdown-body h1, .markdown-body h2, .markdown-body h3,
  .markdown-body h4, .markdown-body h5, .markdown-body h6 {
    margin-top: 24px;
    margin-bottom: 16px;
    font-weight: 600;
    line-height: 1.25;
  }
  .markdown-body h1 { font-size: 2em; padding-bottom: .3em; border-bottom: 1px solid var(--border-muted); }
  .markdown-body h2 { font-size: 1.5em; padding-bottom: .3em; border-bottom: 1px solid var(--border-muted); }
  .markdown-body h3 { font-size: 1.25em; }
  .markdown-body h4 { font-size: 1em; }
  .markdown-body h5 { font-size: .875em; }
  .markdown-body h6 { font-size: .85em; color: var(--fg-muted); }

  .markdown-body p { margin-top: 0; margin-bottom: 16px; }

  .markdown-body a {
    color: var(--accent-fg);
    text-decoration: none;
  }
  .markdown-body a:hover { text-decoration: underline; }

  .markdown-body img { max-width: 100%; vertical-align: middle; background-color: var(--bg-canvas); }

  .markdown-body code {
    padding: .2em .4em;
    margin: 0;
    font-size: 85%;
    background-color: rgba(110,118,129,0.4);
    border-radius: 6px;
    font-family: ui-monospace, SFMono-Regular, "SF Mono", Menlo, Consolas, "Liberation Mono", monospace;
  }
  .markdown-body pre {
    padding: 16px;
    overflow: auto;
    font-size: 85%;
    line-height: 1.45;
    color: var(--fg-default);
    background-color: var(--bg-overlay);
    border-radius: 6px;
    margin-bottom: 16px;
  }
  .markdown-body pre code {
    padding: 0;
    margin: 0;
    font-size: 100%;
    background-color: transparent;
    border: 0;
    display: block;
  }

  .markdown-body table {
    margin-top: 0;
    margin-bottom: 16px;
    display: block;
    width: 100%;
    overflow: auto;
    border-spacing: 0;
    border-collapse: collapse;
  }
  .markdown-body table th, .markdown-body table td {
    padding: 6px 13px;
    border: 1px solid var(--border-default);
  }
  .markdown-body table tr {
    background-color: var(--bg-canvas);
    border-top: 1px solid var(--border-muted);
  }
  .markdown-body table tr:nth-child(2n) {
    background-color: var(--bg-overlay);
  }
  .markdown-body table img { background-color: transparent; }

  .markdown-body blockquote {
    padding: 0 1em;
    color: var(--fg-muted);
    border-left: .25em solid var(--border-default);
    margin: 0 0 16px 0;
  }
  .markdown-body blockquote > :first-child { margin-top: 0; }
  .markdown-body blockquote > :last-child { margin-bottom: 0; }

  .markdown-body ul, .markdown-body ol {
    padding-left: 2em;
    margin-bottom: 16px;
  }
  .markdown-body li + li { margin-top: .25em; }
  .markdown-body li > p { margin-top: 16px; }

  .markdown-body hr {
    height: .25em;
    padding: 0;
    margin: 24px 0;
    background-color: var(--border-default);
    border: 0;
  }

  .markdown-body input[type="checkbox"] {
    margin-right: .5em;
    accent-color: var(--cyan);
  }

  /* === Sidebar (simula la barra lateral de GitHub) === */
  .gh-sidebar {
    display: none;
  }
  .gh-sidebar .panel {
    background: var(--bg-canvas);
    border: 1px solid var(--border-default);
    border-radius: 8px;
    padding: 16px;
    margin-bottom: 16px;
  }
  .gh-sidebar .panel h2 {
    font-size: 14px;
    font-weight: 600;
    color: var(--fg-default);
    padding-bottom: 8px;
    margin-bottom: 8px;
    border-bottom: 1px solid var(--border-muted);
  }
  .gh-sidebar .panel ul { list-style: none; padding: 0; }
  .gh-sidebar .panel li {
    padding: 4px 0;
    font-size: 13px;
    color: var(--fg-muted);
  }
  .gh-sidebar .panel li a {
    color: var(--accent-fg);
    text-decoration: none;
  }
  .gh-sidebar .panel li a:hover { text-decoration: underline; }

  /* === Info banner === */
  .info-banner {
    background: linear-gradient(90deg, rgba(0,229,255,0.08), rgba(167,139,250,0.08));
    border: 1px solid rgba(0,229,255,0.3);
    border-radius: 8px;
    padding: 12px 16px;
    margin-bottom: 16px;
    color: var(--fg-default);
    font-size: 13px;
    display: flex;
    align-items: flex-start;
    gap: 12px;
  }
  .info-banner .icon {
    font-size: 18px;
    color: var(--cyan);
    flex-shrink: 0;
  }
  .info-banner strong { color: var(--cyan); }

  /* === Footer note === */
  .preview-footer {
    text-align: center;
    padding: 24px;
    color: var(--fg-muted);
    font-size: 13px;
    border-top: 1px solid var(--border-muted);
    margin-top: 24px;
  }
  .preview-footer code {
    background: var(--bg-overlay);
    padding: 2px 6px;
    border-radius: 4px;
    font-family: ui-monospace, SFMono-Regular, monospace;
    color: var(--cyan);
  }

  /* Force alignment styles that GitHub strips but markdown allows */
  .markdown-body div[align="center"] {
    text-align: center;
  }
  .markdown-body p[align="left"] { text-align: left; }

  /* Live badge pulse animation (simulates online indicator) */
  @keyframes pulse-cyan {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.6; }
  }
</style>
</head>
<body>

<div class="gh-topbar">
  <div class="repo-path">
    <svg class="octicon" width="16" height="16" viewBox="0 0 16 16" aria-hidden="true">
      <path fill-rule="evenodd" d="M2 2.5A2.5 2.5 0 014.5 0h8.75a.75.75 0 01.75.75v12.5a.75.75 0 01-.75.75h-2.5a.75.75 0 110-1.5h1.75v-2h-8a1 1 0 00-.714 1.7.75.75 0 01-1.072 1.05A2.495 2.495 0 012 11.5v-9zm10.5-1V9h-8c-.356 0-.694.074-1 .208V2.5a1 1 0 011-1h8zM5 12.25v3.25a.25.25 0 00.4.2l1.45-1.087a.25.25 0 01.3 0L8.6 15.7a.25.25 0 00.4-.2v-3.25a.25.25 0 00-.25-.25h-3.5a.25.25 0 00-.25.25z"></path>
    </svg>
    <a href="#">Lucas18062025</a>
    <span class="sep">/</span>
    <a href="#"><strong>Lucas18062025</strong></a>
    <span class="badge">PREVIEW · GitHub Dark</span>
  </div>
</div>

<div class="gh-container">
  <main class="readme-card">
    <div class="readme-header">
      <svg width="16" height="16" viewBox="0 0 16 16" aria-hidden="true">
        <path fill-rule="evenodd" d="M1.326 1.185a.67.67 0 00.61.85h.711l1.55 6.074A2.25 2.25 0 006.38 10.5h5.058a2.25 2.25 0 002.183-1.769l.768-3.348A.75.75 0 0013.66 4.5H3.715l-.688-2.694A.75.75 0 002.298 1.5H1.134a.67.67 0 00.192.685zm1.827 9.465a1.75 1.75 0 11-3.499.247 1.75 1.75 0 013.499-.247zm9.5 0a1.75 1.75 0 11-3.499.247 1.75 1.75 0 013.499-.247zM6.5 12.5a1.75 1.75 0 11-3.499.247 1.75 1.75 0 013.499-.247zM14 4.75a.75.75 0 11-1.5 0 .75.75 0 011.5 0z"></path>
      </svg>
      README.md
    </div>
    <div class="readme-body">
      <div class="info-banner">
        <span class="icon">⚡</span>
        <div>
          <strong>Preview real de GitHub Dark Mode.</strong>
          Esto es exactamente cómo se va a ver tu README cuando lo subas a GitHub (rama <code>main</code> o repo de perfil). 
          Las imágenes, badges, tablas y animaciones se renderizan correctamente. 
          El navegador no entiende Markdown por eso se veía el código en bruto — GitHub sí lo interpreta.
        </div>
      </div>
      <div class="markdown-body" id="readme-output">Cargando preview...</div>
    </div>
  </main>

  <aside class="gh-sidebar">
    <div class="panel">
      <h2>📍 Sobre este preview</h2>
      <p style="font-size: 13px; color: var(--fg-muted); line-height: 1.5;">
        Este HTML simula el motor de renderizado de GitHub para archivos <code style="color: var(--cyan);">README.md</code>.
        Las imágenes se cargan en vivo desde los mismos servicios que usa GitHub (shields.io, skillicons.dev, etc.).
      </p>
    </div>
    <div class="panel">
      <h2>🚀 Próximos pasos</h2>
      <ul>
        <li>1. Descargar <code>README.md</code></li>
        <li>2. Crear repo <code>Lucas18062025/Lucas18062025</code></li>
        <li>3. Subir como <code>README.md</code></li>
        <li>4. Verlo en tu perfil de GitHub</li>
      </ul>
    </div>
    <div class="panel">
      <h2>🎨 Paleta Quantum Noir</h2>
      <ul>
        <li><span style="color:#00e5ff">●</span> Cyan <code>#00E5FF</code></li>
        <li><span style="color:#a78bfa">●</span> Violet <code>#A78BFA</code></li>
        <li><span style="color:#22c55e">●</span> Green <code>#22C55E</code></li>
        <li><span style="color:#0d1117;background:#fff">●</span> BG <code>#0D1117</code></li>
      </ul>
    </div>
  </aside>
</div>

<div class="preview-footer">
  Generado para <strong style="color: var(--fg-default);">Lucas Villagra</strong> · Cybersecurity Analyst · 
  Para producción: subí <code>README.md</code> a tu repo <code>Lucas18062025/Lucas18062025</code>
</div>

<script>
  // README content embedded as JSON string
  const readmeRaw = "<!-- \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\n     README.md \u00b7 Lucas Villagra \u00b7 Cybersecurity Analyst\n     Estilo: Dark Mode \u00b7 Quantum Noir \u00b7 Premium\n     Inspiraci\u00f3n: Linear / Vercel / GitHub Dark Default\n     \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 -->\n\n<!-- HEADER PRINCIPAL \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<div align=\"center\">\n\n<!-- Banner con efecto typing animado -->\n<img src=\"https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=28&pause=1200&color=00E5FF&center=true&vCenter=true&repeat=true&width=720&height=70&lines=Cybersecurity+Analyst;Ethical+Hacker;Security+Automation+Engineer;Red+Team+Operator;SIEM+%E2%80%A2+MCP+%E2%80%A2+AI+Integrator\" alt=\"Typing SVG\" />\n\n<!-- Separador con l\u00ednea gradient -->\n<img src=\"https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif\" width=\"100%\" />\n\n<!-- Badges principales \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<a href=\"https://lucas18062025.github.io/Portafolio/\">\n  <img src=\"https://img.shields.io/badge/\ud83c\udf10_PORTAFOLIO-GitHub_Pages-0D1117?style=for-the-badge&logo=github&logoColor=00E5FF&labelColor=0D1117&color=00E5FF\"/>\n</a>\n<a href=\"https://linkedin.com/in/lucas-villagra-9b5097147\">\n  <img src=\"https://img.shields.io/badge/\ud83d\udcbc_LINKEDIN-Connect-0D1117?style=for-the-badge&logo=linkedin&logoColor=0A66C2&labelColor=0D1117&color=0A66C2\"/>\n</a>\n<a href=\"https://github.com/Lucas18062025?tab=followers\">\n  <img src=\"https://img.shields.io/badge/\u2b50_STATUS-Open_to_Work-0D1117?style=for-the-badge&logo=target&logoColor=22C55E&labelColor=0D1117&color=22C55E\"/>\n</a>\n\n<br/><br/>\n\n<!-- Status operacional con estilo terminal -->\n<img src=\"https://img.shields.io/badge/\u25cf_SYSTEM-ONLINE-0D1117?style=flat-square&logo=server&logoColor=00E5FF&labelColor=0D1117&color=00E5FF\"/>\n<img src=\"https://img.shields.io/badge/\u25cf_THREAT-MONITORED-0D1117?style=flat-square&logo=shield&logoColor=A78BFA&labelColor=0D1117&color=A78BFA\"/>\n<img src=\"https://img.shields.io/badge/\u25cf_UPTIME-\u221e-0D1117?style=flat-square&logo=clock&logoColor=22C55E&labelColor=0D1117&color=22C55E\"/>\n\n<br/><br/>\n\n<!-- Skill icons con tema dark -->\n<img src=\"https://skillicons.dev/icons?i=linux,windows,python,powershell,bash,html,css,javascript,nodejs,netlify,cloudflare,docker,vscode,github&theme=dark\" />\n\n</div>\n\n<!-- SEPARADOR \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<img src=\"https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif\" width=\"100%\" />\n\n<!-- ABOUT \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<table>\n<tr>\n<td width=\"50%\">\n\n### \ud83d\udc64 `whoami`\n\n```bash\nlucas@kali:~$ ./identity.sh\n\u250c\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2510\n\u2502  USER    : Lucas Villagra           \u2502\n\u2502  ROLE    : Cybersecurity Analyst    \u2502\n\u2502  FOCUS   : Red Team \u00b7 AI Integrator \u2502\n\u2502  LOC     : Tucum\u00e1n, Argentina       \u2502\n\u2502  STATUS  : Operational              \u2502\n\u2514\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2518\n```\n\n</td>\n<td width=\"50%\">\n\n### \ud83c\udfaf `cat mindset.md`\n\n> **Autodidacta \u00b7 Met\u00f3dico \u00b7 Orientado a resultados**\n>\n> Defensa ofensiva con mente anal\u00edtica. Combino auditor\u00eda t\u00e9cnica rigurosa con automatizaci\u00f3n mediante n8n, IA generativa y Python para blindar activos digitales.\n>\n> Home labs ofensivos/defensivos sobre **Kali, Parrot, Ubuntu** con Metasploit, herramientas wireless y flujos de inteligencia integrados con **Claude MCP** y **Gemini CLI**.\n\n</td>\n</tr>\n</table>\n\n<!-- SEPARADOR \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<img src=\"https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif\" width=\"100%\" />\n\n<!-- GITHUB STATS \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<div align=\"center\">\n\n### \ud83d\udcca `git log --stats`\n\n<!-- Stats principales con tema dark -->\n<img height=\"170\" src=\"https://github-readme-stats.vercel.app/api?username=Lucas18062025&show_icons=true&theme=github_dark&bg_color=0D1117&title_color=00E5FF&icon_color=A78BFA&text_color=C9D1D9&border_color=30363D&hide_border=false&count_private=true&include_all_commits=true\" />\n<img height=\"170\" src=\"https://github-readme-streak-stats.herokuapp.com/?user=Lucas18062025&theme=github-dark-blue&background=0D1117&stroke=30363D&ring=00E5FF&fire=A78BFA&currStreakLabel=00E5FF&sideLabels=C9D1D9&dates=C9D1D9\" />\n\n<!-- Lenguajes m\u00e1s usados -->\n<img height=\"200\" src=\"https://github-readme-stats.vercel.app/api/top-langs/?username=Lucas18062025&layout=compact&theme=github_dark&bg_color=0D1117&title_color=00E5FF&text_color=C9D1D9&border_color=30363D&hide_border=false&langs_count=8&card_width=400\" />\n<img height=\"200\" src=\"https://github-readme-activity-graph.vercel.app/graph?username=Lucas18062025&theme=github-compact&bg_color=0D1117&color=00E5FF&line=A78BFA&point=FFFFFF&hide_border=true&area=true&title=Contribution+Activity\" />\n\n<!-- Trofeos -->\n<img src=\"https://github-profile-trophy.vercel.app/?username=Lucas18062025&theme=onedark&no-bg=true&no-frame=true&column=7&margin-w=8&margin-h=8\" />\n\n</div>\n\n<!-- SEPARADOR \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<img src=\"https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif\" width=\"100%\" />\n\n<!-- PROYECTOS DESTACADOS \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<div align=\"center\">\n\n### \ud83d\ude80 `ls -la /home/lab/active --featured`\n\n*Trabajo operacional \u00b7 Laboratorios activos \u00b7 Automatizaci\u00f3n*\n\n</div>\n\n<table>\n<tr>\n<td width=\"50%\" align=\"center\">\n\n<h3>\ud83d\udee1\ufe0f <a href=\"https://github.com/Lucas18062025/Sentinel\"><b>Sentinel V5 \"Apex\"</b></a></h3>\n<img src=\"https://img.shields.io/badge/STATUS-ACTIVE-22C55E?style=flat-square&logo=github&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/LANG-PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white\"/>\n\n<p align=\"left\">Motor de mantenimiento y auditor\u00eda de seguridad para Windows 11. Limpieza inteligente + auditor\u00eda de firewall con evidencia forense.</p>\n\n<p align=\"left\">\n<img src=\"https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/NetSecurity-30363D?style=flat-square&logo=windows&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Windows_11-0078D4?style=flat-square&logo=windows11&logoColor=white\"/>\n</p>\n\n</td>\n<td width=\"50%\" align=\"center\">\n\n<h3>\ud83d\udce1 <a href=\"https://github.com/Lucas18062025/SIEM_Windows_11\"><b>SIEM \u2014 Windows 11</b></a></h3>\n<img src=\"https://img.shields.io/badge/STATUS-ACTIVE-22C55E?style=flat-square&logo=github&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/LANG-Python-3776AB?style=flat-square&logo=python&logoColor=white\"/>\n\n<p align=\"left\">Monitor de eventos en tiempo real con alertas v\u00eda Telegram. Procesa eventos cr\u00edticos, clasifica riesgos con CVSS v3.1.</p>\n\n<p align=\"left\">\n<img src=\"https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Win_Events-30363D?style=flat-square&logo=windows&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Telegram_API-229ED9?style=flat-square&logo=telegram&logoColor=white\"/>\n</p>\n\n</td>\n</tr>\n<tr>\n<td width=\"50%\" align=\"center\">\n\n<h3>\ud83c\udf10 <a href=\"https://github.com/Lucas18062025/NETWORK-EGRESS-MONITOR-\"><b>Network Egress Monitor</b></a></h3>\n<img src=\"https://img.shields.io/badge/STATUS-ACTIVE-22C55E?style=flat-square&logo=github&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/LANG-PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white\"/>\n\n<p align=\"left\">Monitor de tr\u00e1fico TCP saliente (egress) en tiempo real para Windows. Correlaci\u00f3n de procesos, Reverse DNS y detecci\u00f3n de organizaciones para SOC, DFIR y Threat Hunting.</p>\n\n<p align=\"left\">\n<img src=\"https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Windows-0078D4?style=flat-square&logo=windows&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/TCP/IP-30363D?style=flat-square&logo=cisco&logoColor=white\"/>\n</p>\n\n</td>\n<td width=\"50%\" align=\"center\">\n\n<h3>\ud83c\udfa3 <a href=\"https://github.com/Lucas18062025/Gophish-Lab\"><b>Gophish Lab</b></a></h3>\n<img src=\"https://img.shields.io/badge/STATUS-LAB-FFBD2E?style=flat-square&logo=github&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/LANG-Go-00ADD8?style=flat-square&logo=go&logoColor=white\"/>\n\n<p align=\"left\">Simulaci\u00f3n de campa\u00f1a de phishing con GoPhish + Mailpit. Ciclo completo: template \u2192 landing \u2192 captura de credenciales.</p>\n\n<p align=\"left\">\n<img src=\"https://img.shields.io/badge/GoPhish-CC0000?style=flat-square&logo=go&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Mailpit-30363D?style=flat-square&logo=mailtrap&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Kali_Linux-268BEE?style=flat-square&logo=kalilinux&logoColor=white\"/>\n</p>\n\n</td>\n</tr>\n<tr>\n<td width=\"50%\" align=\"center\">\n\n<h3>\ud83d\udcc4 <a href=\"https://lucas18062025.github.io/Portafolio/\"><b>Reportes Ejecutivos PDF</b></a></h3>\n<img src=\"https://img.shields.io/badge/STATUS-ACTIVE-22C55E?style=flat-square&logo=github&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/LANG-Python-3776AB?style=flat-square&logo=python&logoColor=white\"/>\n\n<p align=\"left\">Informes PDF profesionales para auditor\u00edas WiFi con scoring CVSS para PYMEs argentinas. Generaci\u00f3n autom\u00e1tica con datos estructurados.</p>\n\n<p align=\"left\">\n<img src=\"https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/ReportLab-30363D?style=flat-square&logo=python&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white\"/>\n</p>\n\n</td>\n<td width=\"50%\" align=\"center\">\n\n<h3>\ud83d\udd0d <a href=\"https://github.com/Lucas18062025/security-audit-checker\"><b>Security-Audit-Checker</b></a></h3>\n<img src=\"https://img.shields.io/badge/STATUS-ACTIVE-22C55E?style=flat-square&logo=github&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/LANG-Node.js-339933?style=flat-square&logo=node.js&logoColor=white\"/>\n\n<p align=\"left\">Auditor\u00eda de infraestructura con protecci\u00f3n Arcjet Shield y backend serverless. Detecci\u00f3n de bots y rate limiting inteligente.</p>\n\n<p align=\"left\">\n<img src=\"https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Arcjet-30363D?style=flat-square&logo=shield&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white\"/>\n</p>\n\n</td>\n</tr>\n<tr>\n<td width=\"100%\" align=\"center\" colspan=\"2\">\n\n<h3>\u23f1\ufe0f <a href=\"https://github.com/Lucas18062025/zenhub-dashboard\"><b>ZenHub Dashboard</b></a></h3>\n<img src=\"https://img.shields.io/badge/STATUS-ACTIVE-22C55E?style=flat-square&logo=github&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/LANG-JavaScript-FF9500?style=flat-square&logo=javascript&logoColor=white\"/>\n\n<p>Panel de productividad personal con Pomodoro, gestor de tareas, rastreador de h\u00e1bitos y clima en tiempo real (Open-Meteo).</p>\n\n<p>\n<img src=\"https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/JavaScript-FF9500?style=flat-square&logo=javascript&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Open_Meteo-30363D?style=flat-square&logo=weather&logoColor=white\"/>\n</p>\n\n</td>\n</tr>\n</table>\n\n<!-- SEPARADOR \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<img src=\"https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif\" width=\"100%\" />\n\n<!-- ARSENAL T\u00c9CNICO \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<div align=\"center\">\n\n### \ud83d\udee1\ufe0f `./arsenal.sh --list`\n\n</div>\n\n<table>\n<tr>\n<td width=\"50%\" valign=\"top\">\n\n#### \u26a1 Lenguajes & Scripting\n\n<p>\n<img src=\"https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/JavaScript-FF9500?style=flat-square&logo=javascript&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white\"/>\n</p>\n\n#### \ud83d\udd25 Herramientas Ofensivas\n\n<p>\n<img src=\"https://img.shields.io/badge/Kali_Linux-268BEE?style=flat-square&logo=kalilinux&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Metasploit-CC0000?style=flat-square&logo=metasploit&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Nmap-FF6633?style=flat-square&logo=nmap&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Burp_Suite-FF6600?style=flat-square&logo=burpsuite&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Aircrack--ng-C0392B?style=flat-square&logo=aircrackng&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/John_the_Ripper-CC0000?style=flat-square&logo=johnthegiant&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/GoPhish-CC0000?style=flat-square&logo=go&logoColor=white\"/>\n</p>\n\n</td>\n<td width=\"50%\" valign=\"top\">\n\n#### \ud83d\udee1\ufe0f Defensa & Monitoreo\n\n<p>\n<img src=\"https://img.shields.io/badge/SIEM-30363D?style=flat-square&logo=dataproc&logoColor=00E5FF\"/>\n<img src=\"https://img.shields.io/badge/Splunk-65A637?style=flat-square&logo=splunk&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Suricata-DC2C2E?style=flat-square&logo=suricata&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Wazuh-00A6E2?style=flat-square&logo=wazuh&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/CVSS_v3.1-30363D?style=flat-square&logo=shield&logoColor=00E5FF\"/>\n<img src=\"https://img.shields.io/badge/NIST_DB-003366?style=flat-square&logo=nist&logoColor=white\"/>\n</p>\n\n#### \ud83c\udf10 Infraestructura & Red\n\n<p>\n<img src=\"https://img.shields.io/badge/Docker-0DB7ED?style=flat-square&logo=docker&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/WireGuard-88171A?style=flat-square&logo=wireguard&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/VirtualBox-183153?style=flat-square&logo=virtualbox&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/ProtonVPN-6D4AFF?style=flat-square&logo=protonmail&logoColor=white\"/>\n</p>\n\n#### \ud83e\udd16 AI & Automation\n\n<p>\n<img src=\"https://img.shields.io/badge/Claude_MCP-7C3AED?style=flat-square&logo=anthropic&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/Gemini_CLI-4285F4?style=flat-square&logo=google&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white\"/>\n<img src=\"https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black\"/>\n</p>\n\n</td>\n</tr>\n</table>\n\n<!-- SEPARADOR \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<img src=\"https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif\" width=\"100%\" />\n\n<!-- HOJA DE RUTA \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<div align=\"center\">\n\n### \ud83c\udfaf `cat roadmap_2026.md`\n\n</div>\n\n<table>\n<tr>\n<td width=\"50%\" valign=\"top\">\n\n#### \u2705 Completado\n\n- [x] <img src=\"https://img.shields.io/badge/\u2713-Google_Cybersecurity-30363D?style=flat-square&logo=google&logoColor=white\"/> Certificado de Ciberseguridad de Google\n- [x] <img src=\"https://img.shields.io/badge/\u2713-Google_AI_Essentials-30363D?style=flat-square&logo=google&logoColor=white\"/> AI Essentials\n- [x] <img src=\"https://img.shields.io/badge/\u2713-SIEM-30363D?style=flat-square&logo=python&logoColor=white\"/> SIEM personalizado con alertas Telegram\n- [x] <img src=\"https://img.shields.io/badge/\u2713-GitHub_Pages-30363D?style=flat-square&logo=github&logoColor=white\"/> Portafolio p\u00fablico deployado\n- [x] <img src=\"https://img.shields.io/badge/\u2713-Arcjet-30363D?style=flat-square&logo=shield&logoColor=white\"/> Protecci\u00f3n activa en apps web\n- [x] <img src=\"https://img.shields.io/badge/\u2713-Sentinel_V5-30363D?style=flat-square&logo=powershell&logoColor=white\"/> Motor de auditor\u00eda Open Source\n- [x] <img src=\"https://img.shields.io/badge/\u2713-Cloudflare-30363D?style=flat-square&logo=cloudflare&logoColor=white\"/> Dominio .dev propio\n\n</td>\n<td width=\"50%\" valign=\"top\">\n\n#### \ud83d\udd04 En Progreso / Pr\u00f3ximo\n\n- [ ] <img src=\"https://img.shields.io/badge/\ud83d\udd35-Cisco_Ethical_Hacker-1BA0D7?style=flat-square&logo=cisco&logoColor=white\"/> *(en curso)*\n- [ ] <img src=\"https://img.shields.io/badge/\u23f3-eJPT-CC0000?style=flat-square&logo=ine&logoColor=white\"/> eJPT \u2014 Junior Penetration Tester\n- [ ] <img src=\"https://img.shields.io/badge/\u23f3-Security%2B-FF0000?style=flat-square&logo=comptia&logoColor=white\"/> CompTIA Security+\n- [ ] <img src=\"https://img.shields.io/badge/\u23f3-TryHackMe_Top_1%25-88CC14?style=flat-square&logo=tryhackme&logoColor=white\"/> Top 1% en TryHackMe\n- [ ] <img src=\"https://img.shields.io/badge/\ud83c\udfaf-SOC_Analyst-22C55E?style=flat-square&logo=target&logoColor=white\"/> Primer rol SOC Analyst\n- [ ] <img src=\"https://img.shields.io/badge/\ud83c\udfaf-Junior_Pentester-22C55E?style=flat-square&logo=target&logoColor=white\"/> Primer rol Junior Pentester\n- [ ] <img src=\"https://img.shields.io/badge/\ud83c\udfaf-OSCP-CC0000?style=flat-square&logo=offensive-security&logoColor=white\"/> *(objetivo 2027)*\n\n</td>\n</tr>\n</table>\n\n<!-- SEPARADOR \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<img src=\"https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif\" width=\"100%\" />\n\n<!-- ACTIVIDAD \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<div align=\"center\">\n\n### \ud83d\udcc8 `git commit --activity`\n\n<!-- Activity graph detallado -->\n<img src=\"https://github-readme-activity-graph.vercel.app/graph?username=Lucas18062025&theme=react-dark&bg_color=0D1117&color=00E5FF&line=A78BFA&point=FFFFFF&hide_border=true&area=true&title_color=00E5FF&title=Contributions+in+the+last+year\" width=\"95%\"/>\n\n<!-- Snake animation - requiere action configurada en el repo -->\n<img src=\"https://raw.githubusercontent.com/Lucas18062025/Lucas18062025/output/github-contribution-grid-snake-dark.svg\" width=\"95%\" alt=\"Snake contribution animation\"/>\n\n</div>\n\n<!-- SEPARADOR \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<img src=\"https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif\" width=\"100%\" />\n\n<!-- CONECTA \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<div align=\"center\">\n\n### \ud83d\udcac `./connect.sh --channel`\n\n<a href=\"mailto:lucaslean1806@gmail.com\">\n  <img src=\"https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D1117\"/>\n</a>\n<a href=\"https://t.me/UserName9816\">\n  <img src=\"https://img.shields.io/badge/Telegram-229ED9?style=for-the-badge&logo=telegram&logoColor=white&labelColor=0D1117\"/>\n</a>\n<a href=\"mailto:lucaslean1806@proton.me\">\n  <img src=\"https://img.shields.io/badge/ProtonMail-6D4AFF?style=for-the-badge&logo=protonmail&logoColor=white&labelColor=0D1117\"/>\n</a>\n<a href=\"https://linkedin.com/in/lucas-villagra-9b5097147\">\n  <img src=\"https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0D1117\"/>\n</a>\n<a href=\"https://lucas18062025.github.io/Portafolio/\">\n  <img src=\"https://img.shields.io/badge/Portafolio-00E5FF?style=for-the-badge&logo=github&logoColor=0D1117&labelColor=0D1117\"/>\n</a>\n\n<br/><br/>\n\n<!-- Visitor badge con estilo dark -->\n<img src=\"https://komarev.com/visits?name=Lucas18062025&label=VISITAS&color=00E5FF&labelColor=0D1117&iconColor=00E5FF&style=for-the-badge\" alt=\"Visitor Count\"/>\n\n</div>\n\n<!-- SEPARADOR \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<img src=\"https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif\" width=\"100%\" />\n\n<!-- REFLEXIONES \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<div align=\"center\">\n\n### \ud83d\udcdc `cat reflexiones.log`\n\n</div>\n\n<table>\n<tr>\n<td>\n\n> #### \ud83e\udde0 `[ RED_TEAM_MINDSET ]`\n>\n> *\"Pensar como atacante te ense\u00f1a a defender\u2026 pero actuar con \u00e9tica define qui\u00e9n sos.\"*\n\n</td>\n</tr>\n<tr>\n<td>\n\n> #### \ud83d\udcda `[ CONTINUOUS_LEARNING ]`\n>\n> *\"En el mundo de la ciberseguridad, la curiosidad es tu mejor herramienta. Cada vulnerabilidad es una oportunidad para aprender y cada ataque es una lecci\u00f3n para mejorar. Mantente siempre un paso adelante, porque en este juego, el conocimiento es poder.\"*\n\n</td>\n</tr>\n<tr>\n<td>\n\n> #### \ud83d\udda5\ufe0f `[ VM_ISOLATION_PRINCIPLE ]`\n>\n> *\"El aislamiento de una VM no es absoluto, es probabil\u00edstico. La seguridad real viene de entender cada vector de contacto entre la VM y el host, y eliminar los que no necesit\u00e1s activamente.\"*\n\n</td>\n</tr>\n</table>\n\n<!-- FOOTER \u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500\u2500 -->\n<img src=\"https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif\" width=\"100%\" />\n\n<div align=\"center\">\n\n<img src=\"https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=400&size=14&pause=2000&color=8B949E&center=true&vCenter=true&repeat=true&width=500&lines=uptime+%E2%88%9E+%C2%B7+threat+monitored+%C2%B7+operational;system+secured+%C2%B7+built+with+%E2%9D%A4+on+GitHub\" alt=\"Footer typing\" />\n\n<br/>\n\n<!-- Status final tipo terminal -->\n```\n\u2554\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2557\n\u2551  \u00a9 2026 Lucas Villagra \u00b7 System Secured                  \u2551\n\u2551  Built on GitHub Pages \u00b7 Deployed via Cloudflare Workers \u2551\n\u2551  uptime: \u221e \u00b7 threat level: monitored \u00b7 status: online    \u2551\n\u255a\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u255d\n```\n\n</div>\n\n<!--\n\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\nNOTAS DE PERSONALIZACI\u00d3N (no visibles en el render):\n\n1. SNAKE ANIMATION:\n   La imagen del snake requiere configurar una GitHub Action en tu repo.\n   Cre\u00e1 .github/workflows/snake.yml con:\n   name: Generate Snake\n   on:\n     schedule:\n       - cron: \"0 0 * * *\"\n     workflow_dispatch:\n   jobs:\n     build:\n       runs-on: ubuntu-latest\n       steps:\n         - uses: Platane/snk@master\n           with:\n             github_user_name: Lucas18062025\n             outputs: |\n               dist/github-contribution-grid-snake-dark.svg\n         - uses: crazy-max/ghaction-github-pages@v2.1.3\n           with:\n             target_branch: output\n             build_dir: dist\n           env:\n             GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}\n\n2. STATS WIDGETS:\n   - github-readme-stats: funciona out-of-the-box\n   - streak-stats: funciona out-of-the-box\n   - activity-graph: funciona out-of-the-box\n   - trophy: funciona out-of-the-box\n\n3. PARA EDITAR COLORES (paleta Quantum Noir):\n   - Background: 0D1117 (GitHub dark)\n   - Primary cyan: 00E5FF\n   - Secondary violet: A78BFA / 7C3AED\n   - Success green: 22C55E\n   - Border: 30363D\n\n4. PARA AGREGAR NUEVOS PROYECTOS:\n   Copi\u00e1 un bloque <td width=\"50%\" align=\"center\">...</td> dentro de la tabla\n   de proyectos y reemplaz\u00e1 los datos.\n\n5. ACTUALIZAR VISITOR COUNT:\n   El badge de komarev funciona autom\u00e1ticamente cuando alguien visita tu perfil.\n\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\n-->\n";

  // Configure marked with GitHub-flavored markdown
  marked.setOptions({
    gfm: true,
    breaks: false,
    headerIds: false,
    mangle: false
  });

  // Render
  document.getElementById('readme-output').innerHTML = marked.parse(readmeRaw);

  // Optional: log to console for debugging
  console.log('README preview rendered successfully.');
  console.log('Length:', readmeRaw.length, 'chars');
</script>

</body>
</html>
