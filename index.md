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
.quick-links button#surprise-button,
.quick-links button#cat-button {
  border-color: color-mix(in srgb, var(--gia-warm) 38%, var(--gia-line));
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
.jump-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin: 0.8rem 0 1.1rem;
}
.jump-row button {
  border: 1px solid var(--gia-line);
  border-radius: 999px;
  padding: 0.32rem 0.65rem;
  color: var(--gia-ink);
  background: var(--gia-soft);
  font: inherit;
  cursor: pointer;
}
.jump-row button:hover {
  border-color: var(--gia-accent);
  color: var(--gia-accent);
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
.curiosity-board {
  display: grid;
  grid-template-columns: minmax(0, 0.95fr) minmax(360px, 1.05fr);
  gap: 1rem;
  align-items: stretch;
  margin: 1rem 0 1.45rem;
}
.field-note {
  border: 1px solid var(--gia-line);
  border-radius: 10px;
  padding: 1rem;
  background: var(--gia-soft);
}
.field-note strong {
  display: block;
  margin-bottom: 0.35rem;
}
.field-note p {
  margin: 0;
}
.research-map {
  position: relative;
  min-height: 230px;
  border: 1px solid var(--gia-line);
  border-radius: 10px;
  background:
    radial-gradient(circle at 25% 30%, color-mix(in srgb, var(--gia-accent) 14%, transparent), transparent 32%),
    radial-gradient(circle at 72% 68%, color-mix(in srgb, var(--gia-warm) 13%, transparent), transparent 35%),
    var(--gia-bg);
  overflow: hidden;
}
.research-map::before,
.research-map::after {
  content: "";
  position: absolute;
  inset: 22%;
  border: 1px solid color-mix(in srgb, var(--gia-line) 72%, transparent);
  border-radius: 999px;
  transform: rotate(-12deg);
}
.research-map::after {
  inset: 35%;
  transform: rotate(18deg);
}
.map-node {
  position: absolute;
  z-index: 1;
  border: 1px solid var(--gia-line);
  border-radius: 999px;
  padding: 0.42rem 0.7rem;
  color: var(--gia-ink);
  background: color-mix(in srgb, var(--gia-bg) 88%, transparent);
  box-shadow: 0 10px 22px rgba(23, 32, 38, 0.1);
  cursor: pointer;
  font: inherit;
  transition: transform 160ms ease, border-color 160ms ease, color 160ms ease;
}
.map-node:hover,
.map-node.active-node {
  transform: translateY(-3px) scale(1.03);
  border-color: var(--gia-accent);
  color: var(--gia-accent);
}
.node-pfas { top: 18%; left: 10%; }
.node-microglia { top: 38%; left: 38%; }
.node-sex { top: 15%; right: 10%; }
.node-window { bottom: 18%; left: 18%; }
.node-rnaseq { bottom: 17%; right: 12%; }
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
  .curiosity-board {
    grid-template-columns: 1fr;
  }
  .research-map {
    min-height: 320px;
  }
  .map-node {
    position: static;
    display: inline-block;
    margin: 0.45rem;
  }
  .research-map::before,
  .research-map::after {
    display: none;
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
    <a href="cv.md">Text CV</a>
    <a href="mailto:gvaldez9@depaul.edu">Email</a>
    <button type="button" id="surprise-button">Surprise me</button>
    <button type="button" id="cat-button">Cat break</button>
    <button type="button" id="details-toggle">Open all</button>
    <button type="button" id="theme-toggle">Dark mode</button>
  </div>
</div>

<div class="intro-grid">
  <div class="intro-copy">
    <h2>Hi there</h2>
    <p>I study how environmental contaminants shape the brain and immune system during sensitive windows of development. I am especially interested in PFAS, PCBs, microglia, sex differences, and why early exposures can keep mattering long after the exposure window has passed.</p>
    <p>I recently completed my M.S. in Biological Sciences at DePaul University. Right now, I am the lab manager for Dr. Margaret Bell's lab at DePaul and an incoming Toxicology Ph.D. student at the University of Rochester.</p>
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
    <span>Environmental toxicology, microglia, PFAS, PCBs, sex differences, and developmental windows.</span>
  </div>
  <div class="mini-card">
    <strong>How I work</strong>
    <span>Wet lab experiments paired with RNA seq, pathway analysis, and careful biological interpretation.</span>
  </div>
</div>

<div class="curiosity-board" aria-label="Research map">
  <div class="field-note">
    <strong>Research map</strong>
    <p id="curiosity-note">Pick a theme to see how I connect exposures, brain development, immune signaling, and computation.</p>
  </div>
  <div class="research-map">
    <button type="button" class="map-node node-pfas" data-open-detail="exposures" data-note="PFAS and PCBs are useful models for asking how long lasting chemicals interact with endocrine, immune, metabolic, and developmental systems.">PFAS and PCBs</button>
    <button type="button" class="map-node node-microglia" data-open-detail="immune" data-note="Microglia are where a lot of my questions meet: immune challenge, brain development, sex differences, and prior exposure history.">Microglia</button>
    <button type="button" class="map-node node-sex" data-open-detail="immune" data-note="Sex differences matter because the same exposure can change the magnitude, timing, or direction of a neuroimmune response.">Sex differences</button>
    <button type="button" class="map-node node-window" data-open-detail="windows" data-note="I think a lot about timing: early life, adolescence, and reproductive development are not interchangeable exposure windows.">Developmental windows</button>
    <button type="button" class="map-node node-rnaseq" data-open-detail="programming" data-note="I use R, Python, RNA seq, and pathway analysis to connect gene level results back to the biology collaborators actually care about.">RNA seq</button>
  </div>
</div>

<hr class="section-rule">

<section id="work">
<h2>What I Work On</h2>
</section>

At DePaul, I study how early life exposure to environmental contaminants affects neuroimmune and neuroendocrine development. My master's thesis, **Early Life Exposure to PFAS Affects Adolescent Neuroimmune Activity**, investigated how developmental PFOS exposure changes neural and immune responses following an adolescent inflammatory challenge.

I also manage and contribute to projects examining how perinatal PCB exposure affects neonatal and adolescent neuroimmune outcomes.

<div class="jump-row" aria-label="Research topic shortcuts">
  <button type="button" data-open-detail="exposures">PFAS and PCBs</button>
  <button type="button" data-open-detail="immune">Microglia</button>
  <button type="button" data-open-detail="windows">Developmental windows</button>
  <button type="button" data-open-detail="programming">R and Python</button>
</div>

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
  detailsToggle.textContent = allOpen ? "Close all" : "Open all";
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
    const note = document.getElementById("curiosity-note");
    document.querySelectorAll(".map-node").forEach((node) => {
      node.classList.toggle("active-node", node === button);
    });
    if (note && button.dataset.note) {
      note.textContent = button.dataset.note;
    }
    if (target) {
      target.open = true;
      target.classList.remove("flash-target");
      void target.offsetWidth;
      target.classList.add("flash-target");
      target.scrollIntoView({ behavior: "smooth", block: "center" });
    }
  });
});

const surpriseButton = document.getElementById("surprise-button");
if (surpriseButton) {
  const surpriseTargets = Array.from(document.querySelectorAll(".map-node"));
  surpriseButton.addEventListener("click", () => {
    const target = surpriseTargets[Math.floor(Math.random() * surpriseTargets.length)];
    if (target) target.click();
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
