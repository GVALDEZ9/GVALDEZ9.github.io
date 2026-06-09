<style>
:root {
  --gia-bg: #ffffff;
  --gia-ink: #172026;
  --gia-muted: #5f6b76;
  --gia-line: #d9dee3;
  --gia-soft: #f4f6f8;
  --gia-accent: #205f73;
  --gia-warm: #9a463f;
}
html {
  scroll-behavior: smooth;
}
.site-header {
  display: none;
}
body.gia-dark {
  --gia-bg: #101418;
  --gia-ink: #e9eef2;
  --gia-muted: #b9c3cc;
  --gia-line: #2d3740;
  --gia-soft: #182028;
  --gia-accent: #7dc3d9;
  --gia-warm: #e29b8e;
  background: var(--gia-bg);
  color: var(--gia-ink);
}
.wrapper {
  max-width: min(1120px, calc(100% - 40px));
}
.page-content {
  padding-top: 1rem;
}
.post-content {
  font-size: 1rem;
  line-height: 1.65;
}
.hero-name {
  font-size: clamp(2.7rem, 7vw, 5.6rem);
  line-height: 0.95;
  margin: 0 0 0.7rem;
}
.hero-subtitle {
  color: var(--gia-muted);
  font-size: 1.08rem;
  margin-bottom: 1rem;
}
.science-banner {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 0.75rem;
  margin: 1rem 0 1.25rem;
}
.banner-tile {
  position: relative;
  min-height: 112px;
  overflow: hidden;
  border: 1px solid var(--gia-line);
  border-radius: 10px;
  padding: 0.9rem;
  background: var(--gia-soft);
}
.banner-tile strong {
  position: relative;
  z-index: 1;
  display: block;
  margin-bottom: 0.25rem;
}
.banner-tile span {
  position: relative;
  z-index: 1;
  color: var(--gia-muted);
  font-size: 0.92rem;
}
.banner-tile::after {
  content: "";
  position: absolute;
  width: 150px;
  height: 150px;
  right: -44px;
  bottom: -64px;
  border-radius: 50%;
  opacity: 0.42;
}
.banner-microglia::after {
  background:
    radial-gradient(circle, #5aa6b8 0 10%, transparent 11%),
    conic-gradient(from 20deg, transparent 0 12%, #5aa6b8 13% 18%, transparent 19% 38%, #5aa6b8 39% 44%, transparent 45% 68%, #5aa6b8 69% 74%, transparent 75%);
}
.banner-endo::after {
  background:
    repeating-linear-gradient(135deg, #d88477 0 8px, transparent 8px 16px),
    radial-gradient(circle, #d88477, transparent 62%);
}
.banner-window::after {
  border-radius: 14px;
  background:
    linear-gradient(90deg, #6b9f7d 0 2px, transparent 2px 32px),
    linear-gradient(#6b9f7d 0 2px, transparent 2px 32px);
  background-size: 34px 34px;
}
.banner-germline::after {
  background:
    radial-gradient(circle at 35% 35%, #b784c5 0 8%, transparent 9%),
    radial-gradient(circle at 62% 58%, #b784c5 0 8%, transparent 9%),
    linear-gradient(130deg, transparent 37%, #b784c5 38% 42%, transparent 43%);
}
.quick-links {
  position: sticky;
  top: 0.6rem;
  z-index: 5;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  gap: 0.75rem;
  margin: 1rem 0 1.5rem;
  padding: 0.7rem 0.85rem;
  background: color-mix(in srgb, var(--gia-bg) 92%, transparent);
  border: 1px solid var(--gia-line);
  border-radius: 14px;
  box-shadow: 0 14px 30px rgba(23, 32, 38, 0.08);
  backdrop-filter: blur(12px);
}
.nav-group {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 0.45rem;
}
.quick-links .nav-label {
  align-self: center;
  color: var(--gia-muted);
  font-size: 0.84rem;
  padding-right: 0.1rem;
}
.quick-links a,
.quick-links button {
  border: 1px solid var(--gia-line);
  border-radius: 999px;
  padding: 0.34rem 0.68rem;
  text-decoration: none;
  color: var(--gia-ink);
  background: var(--gia-soft);
  font: inherit;
  cursor: pointer;
}
.quick-links a:hover,
.quick-links button:hover {
  border-color: var(--gia-accent);
  color: var(--gia-accent);
}
.quick-links a.active-section {
  border-color: var(--gia-accent);
  box-shadow: inset 0 0 0 1px var(--gia-accent);
}
.intro-grid {
  display: grid;
  grid-template-columns: minmax(0, 1.05fr) minmax(330px, 0.95fr);
  gap: 1.3rem;
  align-items: stretch;
  margin: 1.2rem 0 1.35rem;
}
.intro-copy {
  background: var(--gia-soft);
  border: 1px solid var(--gia-line);
  border-radius: 10px;
  padding: 1.15rem 1.25rem;
}
.intro-copy h2 {
  margin-top: 0;
}
.intro-copy p:last-child {
  margin-bottom: 0;
}
.site-photo {
  margin: 0;
}
.site-photo img {
  width: 100%;
  height: 100%;
  min-height: 360px;
  max-height: 520px;
  object-fit: cover;
  object-position: center;
  border-radius: 8px;
  box-shadow: 0 18px 42px rgba(23, 32, 38, 0.16);
}
.site-photo figcaption,
.cat-card figcaption {
  color: var(--gia-muted);
  font-size: 0.92rem;
  margin-top: 0.45rem;
}
.card-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 0.85rem;
  margin: 1.2rem 0 1.35rem;
}
.mini-card {
  background: var(--gia-soft);
  border: 1px solid var(--gia-line);
  border-radius: 8px;
  padding: 0.9rem;
  transition: transform 160ms ease, border-color 160ms ease, box-shadow 160ms ease;
}
.mini-card:hover {
  transform: translateY(-3px);
  border-color: var(--gia-accent);
  box-shadow: 0 12px 24px rgba(23, 32, 38, 0.08);
}
.mini-card strong {
  display: block;
  margin-bottom: 0.3rem;
}
.mini-card span {
  color: var(--gia-muted);
}
.theme-lab {
  display: grid;
  grid-template-columns: 260px minmax(0, 1fr);
  gap: 1rem;
  margin: 1.1rem 0 1.6rem;
}
.theme-menu,
.theme-panel {
  border: 1px solid var(--gia-line);
  border-radius: 10px;
  background: var(--gia-soft);
}
.theme-menu {
  padding: 0.8rem;
}
.theme-menu strong {
  display: block;
  margin: 0.1rem 0 0.6rem;
}
.theme-menu p {
  color: var(--gia-muted);
  font-size: 0.92rem;
  margin: 0;
}
.theme-button,
.theme-action {
  width: 100%;
  text-align: left;
  border: 1px solid var(--gia-line);
  border-radius: 8px;
  padding: 0.55rem 0.65rem;
  margin-top: 0.45rem;
  color: var(--gia-ink);
  background: var(--gia-bg);
  cursor: pointer;
  font: inherit;
  transition: transform 150ms ease, border-color 150ms ease, color 150ms ease;
}
.theme-button {
  display: grid;
  grid-template-columns: 34px minmax(0, 1fr);
  align-items: center;
  gap: 0.55rem;
}
.theme-icon {
  position: relative;
  width: 30px;
  height: 30px;
  border: 1px solid color-mix(in srgb, var(--gia-accent) 35%, var(--gia-line));
  border-radius: 50%;
  background: color-mix(in srgb, var(--gia-accent) 8%, var(--gia-bg));
}
.theme-icon::before,
.theme-icon::after {
  content: "";
  position: absolute;
  border-color: var(--gia-accent);
}
.icon-exposure::before {
  width: 6px;
  height: 6px;
  border: 1px solid var(--gia-accent);
  border-radius: 50%;
  left: 7px;
  top: 7px;
  box-shadow: 10px 0 0 -1px var(--gia-bg), 10px 0 0 0 var(--gia-accent), 5px 10px 0 -1px var(--gia-bg), 5px 10px 0 0 var(--gia-accent);
}
.icon-exposure::after {
  width: 16px;
  height: 1px;
  left: 7px;
  top: 14px;
  background: var(--gia-accent);
  transform: rotate(28deg);
}
.icon-microglia::before {
  width: 8px;
  height: 8px;
  left: 10px;
  top: 10px;
  border-radius: 50%;
  background: var(--gia-accent);
}
.icon-microglia::after {
  width: 20px;
  height: 20px;
  left: 4px;
  top: 4px;
  border-top: 2px solid var(--gia-accent);
  border-right: 2px solid var(--gia-accent);
  border-radius: 50%;
  transform: rotate(35deg);
}
.icon-window::before {
  width: 18px;
  height: 12px;
  left: 5px;
  top: 8px;
  border: 1px solid var(--gia-accent);
  border-radius: 2px;
}
.icon-window::after {
  width: 1px;
  height: 12px;
  left: 14px;
  top: 8px;
  background: var(--gia-accent);
  box-shadow: 5px 0 0 var(--gia-accent);
}
.icon-germline::before {
  width: 18px;
  height: 18px;
  left: 5px;
  top: 5px;
  border-left: 2px solid var(--gia-accent);
  border-right: 2px solid var(--gia-accent);
  border-radius: 50%;
  transform: rotate(35deg);
}
.icon-germline::after {
  width: 16px;
  height: 2px;
  left: 6px;
  top: 14px;
  background: var(--gia-accent);
  box-shadow: 0 -5px 0 color-mix(in srgb, var(--gia-accent) 65%, transparent), 0 5px 0 color-mix(in srgb, var(--gia-accent) 65%, transparent);
  transform: rotate(-35deg);
}
.icon-rnaseq::before {
  width: 20px;
  height: 8px;
  left: 4px;
  top: 10px;
  border-top: 2px solid var(--gia-accent);
  border-radius: 50%;
}
.icon-rnaseq::after {
  width: 18px;
  height: 10px;
  left: 5px;
  top: 9px;
  border-bottom: 2px solid var(--gia-warm);
  border-radius: 50%;
}
.theme-button:hover,
.theme-button.active-theme,
.theme-action:hover {
  transform: translateX(3px);
  border-color: var(--gia-accent);
  color: var(--gia-accent);
}
.theme-action {
  border-color: color-mix(in srgb, var(--gia-warm) 38%, var(--gia-line));
}
.theme-panel {
  padding: 1.1rem 1.2rem;
  min-height: 265px;
  background:
    linear-gradient(135deg, color-mix(in srgb, var(--gia-accent) 9%, transparent), transparent 38%),
    var(--gia-soft);
}
.theme-panel h2 {
  margin: 0 0 0.2rem;
}
.theme-kicker {
  color: var(--gia-muted);
  font-size: 0.9rem;
  margin-bottom: 0.65rem;
}
.theme-panel p {
  max-width: 76ch;
}
.theme-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 0.7rem;
  margin-top: 0.9rem;
}
.theme-stat {
  border: 1px solid var(--gia-line);
  border-radius: 8px;
  padding: 0.7rem;
  background: color-mix(in srgb, var(--gia-bg) 76%, transparent);
}
.theme-stat strong {
  display: block;
  font-size: 0.85rem;
  color: var(--gia-muted);
  margin-bottom: 0.25rem;
}
.theme-links {
  display: flex;
  flex-wrap: wrap;
  gap: 0.45rem;
  margin-top: 0.9rem;
}
.theme-links button,
.theme-links a {
  border: 1px solid var(--gia-line);
  border-radius: 999px;
  padding: 0.34rem 0.65rem;
  color: var(--gia-ink);
  background: var(--gia-bg);
  text-decoration: none;
  cursor: pointer;
  font: inherit;
}
.theme-links button:hover,
.theme-links a:hover {
  border-color: var(--gia-accent);
  color: var(--gia-accent);
}
.section-action {
  border: 1px solid var(--gia-line);
  border-radius: 999px;
  padding: 0.34rem 0.65rem;
  color: var(--gia-ink);
  background: var(--gia-soft);
  cursor: pointer;
  font: inherit;
}
.section-action:hover {
  border-color: var(--gia-accent);
  color: var(--gia-accent);
}
.flash-target {
  animation: flashTarget 900ms ease;
}
@keyframes flashTarget {
  0% { box-shadow: 0 0 0 0 color-mix(in srgb, var(--gia-accent) 42%, transparent); }
  45% { box-shadow: 0 0 0 8px color-mix(in srgb, var(--gia-accent) 16%, transparent); }
  100% { box-shadow: 0 0 0 0 transparent; }
}
.details-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 0.85rem;
}
details {
  border: 1px solid var(--gia-line);
  border-radius: 8px;
  padding: 0.85rem 1rem;
  margin: 0;
  background: var(--gia-soft);
  scroll-margin-top: 5rem;
}
details.full-width {
  grid-column: 1 / -1;
}
summary {
  cursor: pointer;
  font-weight: 700;
}
summary:hover {
  color: var(--gia-accent);
}
.cat-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 0.85rem;
  margin-top: 0.85rem;
}
.cat-card {
  margin: 0;
}
.cat-card img {
  width: 100%;
  aspect-ratio: 4 / 3;
  object-fit: cover;
  border-radius: 8px;
  border: 1px solid var(--gia-line);
}
.cat-card.portrait img {
  aspect-ratio: 3 / 4;
}
.section-rule {
  border: 0;
  border-top: 1px solid var(--gia-line);
  margin: 2rem 0 1.25rem;
}
section {
  scroll-margin-top: 5rem;
}
@media (max-width: 760px) {
  .quick-links {
    position: static;
    align-items: flex-start;
  }
  .intro-grid {
    grid-template-columns: 1fr;
  }
  .science-banner {
    grid-template-columns: 1fr;
  }
  .theme-lab {
    grid-template-columns: 1fr;
  }
  .theme-grid {
    grid-template-columns: 1fr;
  }
  .card-grid,
  .details-grid,
  .cat-grid {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="hero-name">Gia Valdez</div>

<div class="hero-subtitle">
Lab Manager, Bell Lab at DePaul University · Incoming Toxicology Ph.D. student at the University of Rochester · Environmental toxicology, neurodevelopment, and neuroimmune signaling
</div>

<div class="science-banner" aria-label="Research themes">
  <div class="banner-tile banner-microglia">
    <strong>Microglia and immune signaling</strong>
    <span>How brain resident immune cells respond to exposure and challenge.</span>
  </div>
  <div class="banner-tile banner-endo">
    <strong>Endocrine disruption</strong>
    <span>How chemical exposures may intersect with hormonal systems.</span>
  </div>
  <div class="banner-tile banner-window">
    <strong>Critical windows</strong>
    <span>Why timing may shape risk across development.</span>
  </div>
  <div class="banner-tile banner-germline">
    <strong>Gametogenesis and EDCs</strong>
    <span>How reproductive development may carry exposure sensitivity.</span>
  </div>
</div>

<div class="quick-links">
  <div class="nav-group" aria-label="Page sections">
    <span class="nav-label">Jump to</span>
    <a class="page-link" href="#work">Research</a>
    <a class="page-link" href="#education">Education</a>
    <a class="page-link" href="#details">CV Details</a>
    <a class="page-link" href="#cats">Cats</a>
    <a class="page-link" href="#contact">Contact</a>
  </div>
  <div class="nav-group" aria-label="Links and page controls">
    <span class="nav-label">Links</span>
    <a href="https://github.com/GVALDEZ9">GitHub</a>
    <a href="assets/Gia_Valdez_CV_2026.pdf">PDF CV</a>
    <a href="mailto:gvaldez9@depaul.edu">Email</a>
    <button type="button" id="theme-toggle">Dark mode</button>
  </div>
</div>

<div class="intro-grid">
  <div class="intro-copy">
    <h2>Hi there</h2>
    <p>I study how environmental contaminants shape the brain and immune system during sensitive windows of development.</p>
    <p>Right now, I am the lab manager for Dr. Margaret Bell's lab at DePaul and an incoming Toxicology Ph.D. student at the University of Rochester.</p>
  </div>
  <figure class="site-photo">
    <img src="assets/gia_pfas_presentation.jpg" alt="Gia Valdez with colleagues after her master's thesis defense">
    <figcaption>After my master's thesis defense on early life PFAS exposure and the adolescent brain.</figcaption>
  </figure>
</div>

<div class="card-grid">
  <div class="mini-card">
    <strong>Now</strong>
    <span>Lab manager in the Bell Lab at DePaul and incoming Toxicology Ph.D. student at Rochester.</span>
  </div>
  <div class="mini-card">
    <strong>Research home</strong>
    <span>PFAS, PCBs, microglia, sex differences, and developmental windows.</span>
  </div>
  <div class="mini-card">
    <strong>How I work</strong>
    <span>Wet lab experiments paired with RNA seq and biological interpretation.</span>
  </div>
</div>

<div class="theme-lab" aria-label="Focused research themes">
  <div class="theme-menu">
    <strong>Research directions</strong>
    <p>Choose a theme to see the questions I am interested in pursuing.</p>
    <button type="button" class="theme-button active-theme" data-theme="pfas"><span class="theme-icon icon-exposure" aria-hidden="true"></span><span>PFAS and PCBs</span></button>
    <button type="button" class="theme-button" data-theme="microglia"><span class="theme-icon icon-microglia" aria-hidden="true"></span><span>Microglia, immune, endocrine</span></button>
    <button type="button" class="theme-button" data-theme="windows"><span class="theme-icon icon-window" aria-hidden="true"></span><span>Critical windows</span></button>
    <button type="button" class="theme-button" data-theme="germline"><span class="theme-icon icon-germline" aria-hidden="true"></span><span>Gametogenesis and EDCs</span></button>
    <button type="button" class="theme-button" data-theme="rnaseq"><span class="theme-icon icon-rnaseq" aria-hidden="true"></span><span>RNA seq</span></button>
    <button type="button" class="theme-action" id="surprise-button">Surprise me</button>
    <button type="button" class="theme-action" id="cat-button">Cat break</button>
  </div>
  <div class="theme-panel" id="theme-panel">
    <div class="theme-kicker" id="theme-kicker">Working interest</div>
    <h2 id="theme-title">PFAS and PCBs</h2>
    <p id="theme-body">I am interested in how persistent and endocrine active contaminants may shape developmental risk across neural, immune, metabolic, and hormonal systems. A central question is whether exposure timing changes which systems remain vulnerable later in life.</p>
    <div class="theme-grid">
      <div class="theme-stat"><strong>Working question</strong><span id="theme-question">How does timing shape later vulnerability?</span></div>
      <div class="theme-stat"><strong>Biological context</strong><span id="theme-systems">Neural, immune, endocrine systems</span></div>
      <div class="theme-stat"><strong>Approach</strong><span id="theme-tools">Exposure models, molecular assays, RNA seq</span></div>
    </div>
    <div class="theme-links">
      <button type="button" id="theme-more" data-open-detail="exposures">More on this</button>
      <a href="assets/Gia_Valdez_CV_2026.pdf">Download CV</a>
    </div>
  </div>
</div>

<hr class="section-rule">

<section id="work">
<h2>What I Work On</h2>
</section>

At DePaul, I study how early life exposure to environmental contaminants affects neuroimmune and neuroendocrine development. My master's thesis, **Early Life Exposure to PFAS Affects Adolescent Neuroimmune Activity**, investigated how developmental PFOS exposure changes neural and immune responses following an adolescent inflammatory challenge.

I also manage and contribute to projects examining how perinatal PCB exposure affects neonatal and adolescent neuroimmune outcomes.

<div class="details-grid">
  <details open id="exposures">
    <summary>Environmental exposures</summary>
    <p>I am interested in contaminants that do not act like simple one time toxic insults. PFAS, PCBs, and other endocrine disrupting chemicals can interact with hormonal, immune, metabolic, and developmental systems. For me, the important question is not only whether an exposure changes an outcome, but when the exposure happens and which biological system is most vulnerable at that time.</p>
  </details>

  <details open id="immune">
    <summary>Brain and immune signaling</summary>
    <p>Microglia sit at the center of many questions I care about. They respond to immune challenge, shape brain development, and can behave differently depending on sex, age, and prior exposure history. I am especially interested in how environmental contaminants change the way microglia respond when the immune system is challenged later in life.</p>
  </details>

  <details id="windows">
    <summary>Developmental windows</summary>
    <p>Development is not one uniform window. Early life, adolescence, and reproductive development each have different vulnerabilities. I want to understand how exposure during one window can alter later neuroimmune or neuroendocrine responses, and whether some effects persist through epigenetic, reproductive, or long term immune mechanisms.</p>
  </details>

  <details id="programming">
    <summary>Programming languages and computational tools</summary>
    <p>I most often use R and Python for data analysis, visualization, and RNA seq interpretation. I also use Jupyter Notebooks, SQL, GraphPad Prism, SPSS, and Jamovi.</p>
    <p>I like computational work most when it stays close to the biology: checking model outputs, asking whether pathway results make biological sense, and turning complicated data into figures that collaborators can actually use.</p>
  </details>
</div>

<hr class="section-rule">

<section id="education">
<h2>Education And Experience</h2>
</section>

<div class="details-grid">
  <details open>
    <summary>Education</summary>
    <p><strong>University of Rochester</strong><br>Ph.D. in Toxicology, incoming</p>
    <p><strong>DePaul University</strong><br>M.S. in Biological Sciences<br>Thesis Advisor: Dr. Margaret Bell<br>Thesis: <em>Early Life Exposure to PFAS Affects Adolescent Neuroimmune Activity</em></p>
    <p><strong>DePaul University Honors College</strong><br>B.S. in Neuroscience and Psychology, 2023<br>Minors in Biology and Japanese Language</p>
  </details>

  <details open>
    <summary>Research experience</summary>
    <p><strong>Lab Manager, Bell Lab, DePaul University</strong><br>2025 to present<br>Effects of early life perinatal PCB exposure on neonatal and adolescent neuroimmune and neuroendocrine endpoints.</p>
    <p><strong>Graduate Research Assistant, Bell Lab, DePaul University</strong><br>2024 to present<br>Early life PFOS exposure and adolescent neural and neuroimmune responses following inflammatory challenge.</p>
    <p><strong>Undergraduate Research Assistant, Bell Lab, DePaul University</strong><br>2022 to 2024<br>Perinatal PCB exposure, adolescent ethanol challenge, and immediate early gene mapping.</p>
    <p><strong>Undergraduate Integrative Research Assistant, Field Museum</strong><br>2022 to 2024<br>Machine learning pipelines for bryophyte specimen image classification.</p>
  </details>
</div>

<hr class="section-rule">

<section id="details">
<h2>More About The Work</h2>
</section>

<p><button type="button" class="section-action" id="details-toggle">Open all CV sections</button> <a href="cv.md">Text CV</a></p>

<div class="details-grid">
  <details id="publications">
    <summary>Selected publications and presentations</summary>
    <ul>
      <li>Gia M Valdez, Jennifer Dinh, Simone Rhodes, Margaret R Bell. Effects of acute alcohol on adolescent rat brain responses after gestational Polychlorinated Biphenyls exposure. In preparation, 2026.</li>
      <li>Margaret R Bell, Katherine A Walker, Gia M Valdez, Carissa E Dressel. Advances and challenges in studying effects of EDCs on tissue resident macrophages in inflammation. <em>Journal of the Endocrine Society</em>, 2026. <a href="https://doi.org/10.1210/jendso/bvag044">https://doi.org/10.1210/jendso/bvag044</a></li>
      <li>Gia M Valdez, Jemimah Ross, Lidan Zhao, Robert Sargis, Margaret R Bell. Effects of Early Life Exposure to PFAS on Adolescent Neuroimmune Activity. <em>The Toxicologist</em>, abstract submitted for 2026.</li>
      <li>Gia M Valdez, Jennifer Dinh, Margaret R Bell. Gestational exposure to polychlorinated biphenyls alters adolescent neuroimmune responses to ethanol challenge in the limbic system. <em>The Toxicologist</em>, Abstract 4654, 2025.</li>
      <li>Gia M Valdez, Jemimah N Ross, Carissa E Dressel, Margaret R Bell. Effects of early life environmental contaminant exposure on hypothalamic responses to acute alcohol challenge in adolescence. Society for Neuroscience, 2024.</li>
    </ul>
  </details>

  <details id="teaching">
    <summary>Teaching and mentorship</summary>
    <p>At DePaul, I have taught and supported students in genetics, cell biology, physiology, anatomy, and summer research programming. I have also mentored undergraduate researchers through projects involving data interpretation, Python and R model outputs, and scientific presentations.</p>
  </details>

  <details id="wetlab">
    <summary>Wet lab and tissue skills</summary>
    <p><strong>Molecular and cellular techniques:</strong> qPCR, RNA isolation, cDNA synthesis, primary cell culture, MACS cell separation, immunohistochemistry, immunocytochemistry.</p>
    <p><strong>Animal and tissue work:</strong> in vivo chemical exposure, perfusion, targeted tissue collection, multi organ tissue collection, cryostat sectioning.</p>
    <p><strong>Imaging and analysis:</strong> confocal microscopy, ImageJ, cell quantification, figure preparation.</p>
  </details>

  <details id="awards">
    <summary>Honors and awards</summary>
    <ul>
      <li>Neuroscience Scholars Program Associate, Society for Neuroscience, 2024 to present</li>
      <li>Graduate Research Fund recipient, DePaul University, 2024</li>
      <li>Master's Undergraduate Scholarly Engagement Award, DePaul University, 2024</li>
      <li>Perry J. Gehring Diversity Student Travel Award, Society of Toxicology, 2024</li>
      <li>Undergraduate Diversity Travel Award, Society of Toxicology, 2023</li>
      <li>Organization for the Study of Sex Differences Undergraduate Attendee Award, 2023</li>
      <li>DOORS Scholarship recipient, Promega and BTCI Institute, 2022</li>
    </ul>
  </details>
</div>

<hr class="section-rule">

<section id="cats">
<h2>Killian And Girasol</h2>
</section>

This is the very serious non scientific section.

<div class="cat-grid">
  <figure class="cat-card">
    <img src="assets/killian.jpeg" alt="Killian, a gray and white cat sleeping">
    <figcaption><strong>Killian.</strong> Gray and white. Professional napper.</figcaption>
  </figure>
  <figure class="cat-card">
    <img src="assets/girasol.jpeg" alt="Girasol, an orange cat in a cardboard box">
    <figcaption><strong>Girasol.</strong> Orange. Box enthusiast.</figcaption>
  </figure>
  <figure class="cat-card portrait">
    <img src="assets/killian_girasol.jpeg" alt="Killian and Girasol sitting together">
    <figcaption><strong>Together.</strong> A rare diplomatic summit.</figcaption>
  </figure>
</div>

<hr class="section-rule">

<section id="contact">
<h2>Contact</h2>
</section>

Email: gvaldez9@depaul.edu  
GitHub: [GVALDEZ9](https://github.com/GVALDEZ9)

Last updated: June 8, 2026

<script>
const themeButton = document.getElementById("theme-toggle");
if (themeButton) {
  const savedTheme = localStorage.getItem("gia-theme");
  if (savedTheme === "dark") {
    document.body.classList.add("gia-dark");
    themeButton.textContent = "Light mode";
  }
  themeButton.addEventListener("click", () => {
    document.body.classList.toggle("gia-dark");
    const isDark = document.body.classList.contains("gia-dark");
    localStorage.setItem("gia-theme", isDark ? "dark" : "light");
    themeButton.textContent = isDark ? "Light mode" : "Dark mode";
  });
}

const detailsToggle = document.getElementById("details-toggle");
const allDetails = Array.from(document.querySelectorAll("details"));
function updateDetailsToggle() {
  if (!detailsToggle) return;
  const allOpen = allDetails.length > 0 && allDetails.every((item) => item.open);
  detailsToggle.textContent = allOpen ? "Close all CV sections" : "Open all CV sections";
}
if (detailsToggle) {
  detailsToggle.addEventListener("click", () => {
    const shouldOpen = !allDetails.every((item) => item.open);
    allDetails.forEach((item) => {
      item.open = shouldOpen;
    });
    updateDetailsToggle();
  });
  allDetails.forEach((item) => item.addEventListener("toggle", updateDetailsToggle));
  updateDetailsToggle();
}

document.querySelectorAll("[data-open-detail]").forEach((button) => {
  button.addEventListener("click", () => {
    const target = document.getElementById(button.dataset.openDetail);
    if (target) {
      target.open = true;
      target.classList.remove("flash-target");
      void target.offsetWidth;
      target.classList.add("flash-target");
      target.scrollIntoView({ behavior: "smooth", block: "center" });
    }
  });
});

const themeData = {
  pfas: {
    kicker: "Working interest",
    title: "PFAS and PCBs",
    body: "I am interested in how persistent and endocrine active contaminants may shape developmental risk across neural, immune, metabolic, and hormonal systems. A central question is whether exposure timing changes which systems remain vulnerable later in life.",
    question: "How does timing shape later vulnerability?",
    systems: "Neural, immune, endocrine systems",
    tools: "Exposure models, molecular assays, RNA seq",
    detail: "exposures"
  },
  microglia: {
    kicker: "Working interest",
    title: "Microglia, immune, endocrine",
    body: "I want to understand how microglia respond to inflammatory challenge after early exposure, and how that response may intersect with endocrine signaling and sex specific biology.",
    question: "Does early exposure alter later immune response?",
    systems: "Microglia, cytokines, hormones",
    tools: "Cell separation, qPCR, RNA isolation",
    detail: "immune"
  },
  windows: {
    kicker: "Working interest",
    title: "Critical windows",
    body: "I am interested in how early life, adolescence, and reproductive development differ as windows of susceptibility. The goal is to ask when an exposure is most likely to redirect later physiology.",
    question: "Which exposure window changes later outcomes?",
    systems: "Early life, adolescence, reproduction",
    tools: "Timed exposure, tissue collection, molecular endpoints",
    detail: "windows"
  },
  germline: {
    kicker: "Working interest",
    title: "Gametogenesis and EDCs",
    body: "I am curious about how endocrine disrupting chemicals may affect reproductive development and gamete formation. This is a future facing interest for thinking about exposure effects before conception.",
    question: "Can exposure history shape reproductive vulnerability?",
    systems: "Gonads, gametes, endocrine signaling",
    tools: "Developmental toxicology, epigenetic questions",
    detail: "windows"
  },
  rnaseq: {
    kicker: "Working interest",
    title: "RNA seq",
    body: "I use computational analysis to make transcriptomic results interpretable and biologically grounded. I am especially interested in connecting gene level models with pathway, transcription factor, and cell biology context.",
    question: "What does the model mean biologically?",
    systems: "Genes, pathways, transcriptional response",
    tools: "R, Python, DESeq2, GSVA",
    detail: "programming"
  }
};

const themeButtons = Array.from(document.querySelectorAll(".theme-button"));
const themeFields = {
  kicker: document.getElementById("theme-kicker"),
  title: document.getElementById("theme-title"),
  body: document.getElementById("theme-body"),
  question: document.getElementById("theme-question"),
  systems: document.getElementById("theme-systems"),
  tools: document.getElementById("theme-tools"),
  more: document.getElementById("theme-more"),
  panel: document.getElementById("theme-panel")
};
function setTheme(themeName) {
  const theme = themeData[themeName];
  if (!theme) return;
  themeButtons.forEach((button) => {
    button.classList.toggle("active-theme", button.dataset.theme === themeName);
  });
  themeFields.kicker.textContent = theme.kicker;
  themeFields.title.textContent = theme.title;
  themeFields.body.textContent = theme.body;
  themeFields.question.textContent = theme.question;
  themeFields.systems.textContent = theme.systems;
  themeFields.tools.textContent = theme.tools;
  themeFields.more.dataset.openDetail = theme.detail;
  themeFields.panel.classList.remove("flash-target");
  void themeFields.panel.offsetWidth;
  themeFields.panel.classList.add("flash-target");
}
themeButtons.forEach((button) => {
  button.addEventListener("click", () => setTheme(button.dataset.theme));
});

const surpriseButton = document.getElementById("surprise-button");
if (surpriseButton) {
  const surpriseTargets = Object.keys(themeData);
  surpriseButton.addEventListener("click", () => {
    const target = surpriseTargets[Math.floor(Math.random() * surpriseTargets.length)];
    setTheme(target);
  });
}

const catButton = document.getElementById("cat-button");
if (catButton) {
  catButton.addEventListener("click", () => {
    const cats = document.getElementById("cats");
    if (cats) cats.scrollIntoView({ behavior: "smooth", block: "start" });
  });
}

const navLinks = Array.from(document.querySelectorAll(".page-link"));
const sections = navLinks
  .map((link) => document.querySelector(link.getAttribute("href")))
  .filter(Boolean);
function setActiveSection() {
  let activeId = "";
  sections.forEach((section) => {
    const rect = section.getBoundingClientRect();
    if (rect.top <= 130) {
      activeId = section.id;
    }
  });
  navLinks.forEach((link) => {
    link.classList.toggle("active-section", link.getAttribute("href") === `#${activeId}`);
  });
}
window.addEventListener("scroll", setActiveSection, { passive: true });
setActiveSection();
</script>
