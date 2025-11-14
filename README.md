/<!DOCTYPE html>
/<html>
/  <head>
/    <title>Your Name</title>
/  </head>
/  <body>
/    <h1>Hello, world!</h1>
/    <p>Welcome to my personal site.</p>
/  </body>
/</html>

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<title>Diogo Pereira - Academic Site</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
<style>
  :root {
    --bg-color: #001F44;        /* Rich Navy Blue background */
    --card-bg: #0A2240;         /* Darker softer navy for cards */
    --highlight: #00BFA6;       /* Bright teal accent */
    --text-light: #D9E4F5;      /* Light gray text */
    --text-medium: #A8BDD9;     /* Softer medium gray text */
    --shadow: rgba(0, 0, 0, 0.6);
  }

  html {
    scroll-behavior: smooth;
  }

  body {
    margin: 0;
    font-family: 'Segoe UI', Arial, sans-serif;
    background: var(--bg-color);
    color: var(--text-light);
    line-height: 1.75;
    letter-spacing: 0.02em;
  }

  header {
    background: #003166;
    padding: 24px 48px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    box-shadow: 0 4px 12px var(--shadow);
  }

  .site-title {
    font-size: 1.8em;
    font-weight: bold;
    color: var(--text-light);
    text-shadow: 0 1px 2px rgba(0,0,0,0.6);
  }

  nav {
    display: flex;
    gap: 32px;
  }

  nav a {
    color: var(--text-medium);
    text-decoration: none;
    font-size: 1.05em;
    transition: color 0.3s, border-bottom 0.3s;
    padding: 6px 0;
    cursor: pointer;
    outline-offset: 2px;
  }

  nav a:hover,
  nav a:focus {
    color: var(--highlight);
    border-bottom: 2px solid var(--highlight);
    outline: none;
  }

  nav a:focus-visible {
    outline: 2px solid var(--highlight);
    border-bottom: none;
    outline-offset: 2px;
  }

  .container {
    display: flex;
    max-width: 1100px;
    margin: 40px auto 0;
    gap: 40px;
  }

  aside {
    width: 280px;
    background: var(--card-bg);
    border-radius: 16px;
    padding: 32px 24px;
    box-shadow: 0 8px 24px var(--shadow);
    text-align: center;
    transition: box-shadow 0.3s;
  }

  aside:hover {
    box-shadow: 0 12px 30px var(--highlight);
  }

  aside img {
    width: 160px;
    height: 160px;
    border-radius: 50%;
    margin: 0 auto 20px;
    border: 4px solid var(--highlight);
    object-fit: cover;
    background-color: #fff;
    transition: transform 0.3s;
  }

  aside img:hover {
    transform: scale(1.05);
  }

  .sidebar-info strong {
    font-size: 1.3em;
    color: var(--text-light);
  }

  .area-white {
    margin-top: 6px;
    color: var(--text-light);
    font-style: normal;
    margin-bottom: 20px;
  }

  .contacts-intro {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 12px;
    color: var(--text-light);
    font-style: italic;
    font-size: 0.95em;
  }

  .contacts-intro i {
    color: var(--highlight);
    font-size: 1.3em;
  }

  .contacts {
    text-align: left;
    margin-top: 16px;
  }

  .contacts a {
    color: var(--highlight);
    text-decoration: none;
    word-break: break-word;
    transition: color 0.3s;
  }

  .contacts a:hover,
  .contacts a:focus {
    color: #00FFE7;
    outline: none;
  }

  .contacts i {
    color: var(--highlight);
    margin-right: 8px;
  }

  main {
    flex: 1;
    padding: 30px 40px;
    background: var(--card-bg);
    border-radius: 16px;
    box-shadow: 0 12px 30px var(--shadow);
    color: var(--text-medium);
    transition: box-shadow 0.3s;
  }

  main:hover {
    box-shadow: 0 18px 36px var(--highlight);
  }

  /* Section and Subsection Titles */
  section h2, .subsection-title {
    font-weight: 700;
    color: var(--highlight);
    margin-top: 30px;
    margin-bottom: 18px;
    border-bottom: none;
    padding-bottom: 0;
    letter-spacing: 0.04em;
    text-shadow: 0 1px 2px rgba(0,0,0,0.5);
  }

  section h2 {
    font-size: 1.75em;
  }

  .subsection-title {
    font-size: 1.4em;
  }

  p, ul, li {
    line-height: 1.9;
    margin-bottom: 16px;
  }

  ul li {
    padding-left: 6px;
  }

  .edu-card, .award-card, .research-box {
    background: rgba(0, 191, 166, 0.12);
    border-left: 4px solid var(--highlight);
    padding: 20px 24px;
    border-radius: 16px;
    margin-bottom: 28px;
    color: var(--text-light);
    transition: background-color 0.3s, box-shadow 0.3s;
  }

  .edu-card:hover, .award-card:hover, .research-box:hover {
    background: rgba(0, 191, 166, 0.22);
    box-shadow: 0 0 15px var(--highlight);
  }

  .edu-card h3, .award-card h3, .research-box h3 {
    margin: 0 0 10px 0;
    color: var(--text-light);
  }

  .award-card a, .edu-card a, .research-box a {
    display: inline-block;
    color: var(--highlight);
    font-weight: 700;
    text-decoration: none;
    padding: 8px 16px;
    border-radius: 8px;
    background-color: rgba(0, 191, 166, 0.15);
    transition: background-color 0.3s;
  }

  .award-card a:hover, .edu-card a:hover, .research-box a:hover,
  .award-card a:focus, .edu-card a:focus, .research-box a:focus {
    background-color: var(--highlight);
    color: var(--bg-color);
    outline: none;
  }

  /* Graphical abstract centered wide */
  .graphical-abstract {
    max-width: 90%;
    margin: 45px auto;
    display: flex;
    justify-content: center;
  }

  .graphical-abstract img {
    width: 100%;
    max-width: 700px;
    height: auto;
    border-radius: 16px;
    box-shadow: 0 6px 18px rgba(0,0,0,0.75);
  }

  /* Responsive layout */
  @media (max-width: 900px) {
    .container {
      flex-direction: column;
      max-width: 90%;
      margin: 20px auto 0;
    }
    aside {
      width: 100%;
      margin-bottom: 30px;
    }
    main {
      width: 100%;
      padding: 25px 20px;
    }

    nav {
      gap: 12px;
    }
  }
</style>
</head>
<body>

<header>
  <div class="site-title">Diogo Pereira</div>
  <nav>
    <a onclick="showSection('about')">About Me</a>
    <a onclick="showSection('research')">Research</a>
    <a onclick="showSection('publications')">Publications</a>
  </nav>
</header>

<div class="container">
  <aside>
    <img src="Imagem1.png" alt="Diogo Pereira Photo" />
    <div class="sidebar-info">
      <strong>Diogo Pereira</strong><br>
      PhD Student at Instituto Superior Técnico
      <div class="area-white">Area: Materials Engineering</div>

      <div class="contacts-intro">
        <i class="fa-solid fa-handshake-angle"></i>
        <span>Let's join forces to advance materials science and bring fusion energy closer to reality!</span>
      </div>

      <div class="contacts">
        <p><i class="fa-solid fa-envelope"></i> 
          <a href="mailto:diogosampaiopereira@tecnico.ulisboa.pt" target="_blank">diogosampaiopereira@tecnico.ulisboa.pt</a>
        </p>
        <p><i class="fa-brands fa-linkedin"></i>          
          <a href="https://www.linkedin.com/in/diogosampaiopereira/" target="_blank">linkedin.com/in/diogosampaiopereira/</a>
        </p>
        <p><i class="fa-brands fa-orcid"></i> 
          <a href="https://orcid.org/0009-0006-3506-8795" target="_blank">orcid.org/0009-0006-3506-8795</a>
        </p>
      </div>
    </div>
  </aside>

  <main>
    <section id="about" class="active">
      <div class="subsection-title">About Me</div>
      <p>
        Hi! My name is <strong>Diogo Pereira</strong> and I am a PhD student in 
        Materials Engineering at 
        <a href="https://tecnico.ulisboa.pt" target="_blank">Instituto Superior Técnico</a>.
        I am part of the Materials Processing and Characterisation group at the 
        <a href="https://www.ipfn.tecnico.ulisboa.pt" target="_blank">Instituto de Plasma e Fusão Nuclear (IPFN)</a>,
        under the supervision of 
        <a href="https://scholar.tecnico.ulisboa.pt/authors/ist24807/records" target="_blank">Rodrigo Mateus</a>
        and 
        <a href="https://scholar.tecnico.ulisboa.pt/authors/ist25572/bio?lang=pt" target="_blank">Norberto Catarino</a>.
      </p>
      <p>
        In collaboration with the 
        <a href="https://www.inflpr.ro" target="_blank">National Institute for Laser, Plasma and Radiation Physics (INFLPR)</a>
        in Romania, my research focuses on the oxidation behaviour of boron
        coatings for nuclear fusion applications.
      </p>

      <div class="subsection-title">Education</div>
      <div class="edu-card">
        <h3>BSc in Materials Engineering</h3>
        <p><a href="https://tecnico.ulisboa.pt" target="_blank">Instituto Superior Técnico</a></p>
        <p>[2019–2022]</p>
      </div>
      <div class="edu-card">
        <h3>MSc in Materials Engineering</h3>
        <p><a href="https://tecnico.ulisboa.pt" target="_blank">Instituto Superior Técnico</a></p>
        <p>[2022–2024]</p>
      </div>
      <div class="edu-card">
        <h3>PhD in Materials Engineering</h3>
        <p><a href="https://tecnico.ulisboa.pt" target="_blank">Instituto Superior Técnico</a></p>
        <p>[Starting 2025]</p>
      </div>

      <div class="subsection-title">Acknowledgements and Awards</div>
      <p><strong>Awarded by the Pedagogical Council of IST:</strong></p>

      <div class="award-card">
        <h3>Academic Excellence Diploma 2020/2021</h3>
        <a href="diplomas/A-EN-Mestrados-integrados_ist196115.pdf" target="_blank">Download Diploma (PDF)</a>
      </div>

      <div class="award-card">
        <h3>Academic Excellence Diploma 2021/2022</h3>
        <a href="diplomas/A-licenciaturas-EN (2).pdf" target="_blank">Download Diploma (PDF)</a>
      </div>

      <div class="award-card">
        <h3>Academic Excellence Diploma 2022/2023</h3>
        <a href="diplomas/A-EN-2024-diplomas-mestrado.pdf" target="_blank">Download Diploma (PDF)</a>
      </div>

      <div class="award-card">
        <h3>Academic Excellence Diploma 2023/2024</h3>
        <a href="diplomas/Academic Excellence_2024.pdf" target="_blank">Download Diploma (PDF)</a>
      </div>

      <div class="award-card">
        <h3>Academic Merit Diploma 2019/2020</h3>
        <a href="diplomas/PUof6m4sCqOR5xRG-2021-diplomas-merito-EN-B_ist196115.pdf" target="_blank">Download Diploma (PDF)</a>
      </div>
    </section>

    <section id="research" style="display:none">
      <h2>Research</h2>

      <div class="research-box">
        <h3>Research Interests</h3>
        <ul>
          <li>Materials for nuclear fusion</li>
          <li>Surface modification</li>
          <li>Ion implantation</li>
          <li>Coating deposition techniques</li>
        </ul>
      </div>

      <div class="research-box">
        <h3>Ongoing Projects</h3>
        <p><strong>PhD project:</strong> Oxidation behaviour of boron coatings for nuclear fusion applications</p>

        <p>
          The new International Thermonuclear Experimental Reactor (ITER) baseline includes the change of first wall material from beryllium (Be) to tungsten (W) due to Be’s toxicity 
          and concerns regarding high erosion and tritium (T) retention rates. However, tungsten introduces the risk of high-Z impurity release into the core plasma reducing reactor efficiency.
        </p>
        <p>
          To mitigate this issue and facilitate plasma startup after maintenance periods by reducing oxygen impurity levels, ITER will implement a boronisation system. 
          This process involves deposition of thin boron (B) layers onto W surfaces, leveraging B’s low atomic number to minimise radiative losses and its excellent oxygen-gettering properties.
        </p>

        <div class="graphical-abstract">
          <img src="bbb.png" alt="Graphical abstract of oxidation behaviour study" />
        </div>

        <p>Currently, little is known about the oxidation behaviour of boron under reactor conditions, including:</p>
        <ul>
          <li>What reactions can occur in the presence of humidity?</li>
          <li>How do these reactions affect the oxygen-gettering ability of boron?</li>
          <li>How do they affect fuel retention on the walls (deuterium and tritium)?</li>
          <li>How thick should the coatings be?</li>
        </ul>

        <p><strong>My goal is to answer some of these questions!</strong></p>
      </div>
    </section>

    <section id="publications" style="display:none">
      <h2>Publications</h2>
      <p>I'm just starting my PhD journey, so I don't have any publications yet 😅, but stay tuned—they are coming soon!</p>
      <div style="text-align:center; margin: 20px 0;">
        <img src="workinprogresss.png" alt="Work in Progress" style="max-width: 300px; height: auto;">
      </div>
      <div class="edu-card" style="max-width: 600px; margin: 0 auto;">
        <h3>Master Thesis</h3>
        <p><em>Enhancing Tungsten’s Nitride Formation with Ion Implantation Technique</em></p>
        <p>
          <a href="https://fenix.tecnico.ulisboa.pt/cursos/memat/dissertacao/1691203502344976" target="_blank" style="color: var(--highlight); font-weight: 700; text-decoration: none;">
            View Master Thesis
          </a>
        </p>
      </div>
    </section>
  </main>
</div>

<script>
  function showSection(id) {
    document.querySelectorAll('main section').forEach(section => {
      section.style.display = 'none';
    });
    document.getElementById(id).style.display = 'block';
  }
</script>

</body>
</html>
