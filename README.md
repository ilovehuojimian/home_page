<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Yiyun Shen - Portfolio</title>
  <style>
    :root {
      --columbia-blue: #9BDDFF;
      --columbia-blue-dark: #72B7DC;
      --columbia-blue-light: #EBF7FF;
      --text-main: #1A2B3C;
      --text-muted: #5A6E7F;
      --bg-color: #F4F9FC;
      --card-bg: #FFFFFF;
      --shadow: 0 4px 12px rgba(26, 43, 60, 0.08);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background-color: var(--bg-color);
      color: var(--text-main);
      line-height: 1.6;
      padding-top: 80px;
    }

    /* Streamlined Navigation */
    header {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(8px);
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
      z-index: 1000;
    }

    nav {
      max-width: 1100px;
      margin: 0 auto;
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .nav-logo {
      font-weight: 700;
      font-size: 1.2rem;
      color: var(--text-main);
      text-decoration: none;
      letter-spacing: 0.5px;
    }

    .nav-links {
      display: flex;
      list-style: none;
      gap: 1.5rem;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--text-muted);
      font-weight: 500;
      font-size: 0.95rem;
      transition: color 0.2s ease;
    }

    .nav-links a:hover {
      color: var(--columbia-blue-dark);
    }

    /* Layout & Hero */
    .container {
      max-width: 900px;
      margin: 0 auto;
      padding: 2rem 1.5rem;
    }

    .hero-card {
      background: var(--card-bg);
      border-radius: 12px;
      padding: 2.5rem;
      box-shadow: var(--shadow);
      border-top: 6px solid var(--columbia-blue);
      margin-bottom: 3rem;
      text-align: center;
    }

    .hero-card h1 {
      font-size: 2.5rem;
      color: var(--text-main);
      margin-bottom: 0.5rem;
      letter-spacing: 1px;
    }

    .contact-info {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      flex-wrap: wrap;
      margin-top: 1rem;
      font-size: 0.95rem;
      color: var(--text-muted);
    }

    .contact-info a {
      color: var(--text-main);
      text-decoration: none;
      border-bottom: 2px solid var(--columbia-blue);
      transition: background 0.2s ease;
    }

    .contact-info a:hover {
      background: var(--columbia-blue-light);
    }

    /* Interactive Filter Controls */
    .filter-container {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      margin-bottom: 1.5rem;
      flex-wrap: wrap;
    }

    .filter-label {
      font-size: 0.85rem;
      font-weight: 600;
      color: var(--text-muted);
      text-transform: uppercase;
      margin-right: 0.5rem;
    }

    .filter-btn {
      background: var(--card-bg);
      border: 1px solid var(--columbia-blue);
      color: var(--text-main);
      padding: 0.4rem 0.8rem;
      border-radius: 20px;
      font-size: 0.85rem;
      cursor: pointer;
      transition: all 0.2s ease;
    }

    .filter-btn:hover, .filter-btn.active {
      background: var(--columbia-blue);
      color: #000;
      font-weight: 600;
    }

    /* Sections & Tile Layout */
    .section-title {
      font-size: 1.5rem;
      margin-bottom: 1.5rem;
      color: var(--text-main);
      border-bottom: 2px solid var(--columbia-blue-light);
      padding-bottom: 0.5rem;
    }

    section {
      margin-bottom: 3.5rem;
      scroll-margin-top: 100px;
    }

    .tile-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }

    .tile {
      background: var(--card-bg);
      border-radius: 8px;
      padding: 1.5rem;
      box-shadow: var(--shadow);
      border-left: 4px solid var(--columbia-blue);
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .tile:hover {
      transform: translateY(-2px);
      box-shadow: 0 6px 16px rgba(26, 43, 60, 0.12);
    }

    .tile-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-bottom: 0.5rem;
    }

    .tile-title {
      font-size: 1.15rem;
      font-weight: 700;
    }

    .tile-subtitle {
      font-size: 1rem;
      color: var(--columbia-blue-dark);
      font-weight: 600;
    }

    .tile-meta {
      font-size: 0.85rem;
      color: var(--text-muted);
      text-align: right;
    }

    .tile-body {
      margin-top: 0.75rem;
      font-size: 0.95rem;
    }

    .tile-body ul {
      padding-left: 1.2rem;
    }

    .tile-body li {
      margin-bottom: 0.4rem;
    }

    .tag {
      display: inline-block;
      background: var(--columbia-blue-light);
      color: var(--text-main);
      font-size: 0.75rem;
      padding: 0.2rem 0.6rem;
      border-radius: 4px;
      margin-top: 0.5rem;
      margin-right: 0.3rem;
      font-weight: 500;
    }

    /* Skills & Info Layout */
    .info-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
    }

    .info-card {
      background: var(--card-bg);
      padding: 1.5rem;
      border-radius: 8px;
      box-shadow: var(--shadow);
    }

    .info-card h4 {
      margin-bottom: 0.75rem;
      color: var(--text-main);
      border-bottom: 1px solid var(--columbia-blue-light);
      padding-bottom: 0.25rem;
    }

    footer {
      text-align: center;
      padding: 2rem;
      color: var(--text-muted);
      font-size: 0.85rem;
      border-top: 1px solid var(--columbia-blue-light);
    }

    @media (max-width: 600px) {
      .tile-header {
        flex-direction: column;
      }
      .tile-meta {
        text-align: left;
      }
      .nav-links {
        gap: 0.8rem;
        font-size: 0.85rem;
      }
    }
  </style>
</head>
<body>

  <!-- Navigation Bar -->
  <header>
    <nav>
      <a href="#" class="nav-logo">YIYUN SHEN</a>
      <ul class="nav-links">
        <li><a href="#education">Education</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#additional">Additional Info</a></li>
      </ul>
    </nav>
  </header>

  <main class="container">

    <!-- Hero Card -->
    <div class="hero-card">
      <h1>YIYUN SHEN</h1>
      <div class="contact-info">
        <span>+1 6462699969</span>
        <a href="mailto:ys4081@gsb.columbia.edu">ys4081@gsb.columbia.edu</a>
        <a href="https://www.linkedin.com/in/yiyunshen0602/" target="_blank" rel="noopener">LinkedIn Profile</a>
      </div>
    </div>

    <!-- Education Section -->
    <section id="education">
      <h2 class="section-title">Education</h2>
      <div class="tile-grid">
        
        <div class="tile">
          <div class="tile-header">
            <div>
              <div class="tile-title">Columbia Business School</div>
              <div class="tile-subtitle">MS, Marketing Science</div>
            </div>
            <div class="tile-meta">
              <div>New York, NY</div>
              <div>Feb 2028 | GRE: 326</div>
            </div>
          </div>
          <div class="tile-body">
            <p>A highly selective, industry-oriented program which combines PhD and MBA courses to provide advanced statistical expertise and a strategic approach to marketing research and analytics.</p>
            <div style="margin-top: 0.5rem;">
              <strong>Related Coursework:</strong> Marketing Consulting Skills, Advanced Marketing Analytics, Python Programming for Data Science, Statistical Modeling and Decision Making, Generative AI for Business
            </div>
          </div>
        </div>

        <div class="tile">
          <div class="tile-header">
            <div>
              <div class="tile-title">East China Normal University</div>
              <div class="tile-subtitle">BA, English</div>
            </div>
            <div class="tile-meta">
              <div>Shanghai, China</div>
              <div>Jun 2026 | GPA: 3.88/4.00</div>
            </div>
          </div>
          <div class="tile-body">
            <p><strong>Minor:</strong> Finance</p>
            <p><strong>Honors:</strong> National Scholarship for 2024-2025 Academic Year</p>
          </div>
        </div>

      </div>
    </section>

    <!-- Experience Section -->
    <section id="experience">
      <h2 class="section-title">Experience</h2>
      
      <!-- Interactive Filter Controls -->
      <div class="filter-container">
        <span class="filter-label">Filter Focus:</span>
        <button class="filter-btn active" onclick="filterExperience('all')">Show All</button>
        <button class="filter-btn" onclick="filterExperience('strategy')">Strategy & Analytics</button>
        <button class="filter-btn" onclick="filterExperience('digital')">Digital Marketing & PR</button>
      </div>

      <div class="tile-grid">

        <div class="tile" data-category="strategy">
          <div class="tile-header">
            <div>
              <div class="tile-title">SHEIN</div>
              <div class="tile-subtitle">Strategy Analyst Intern</div>
            </div>
            <div class="tile-meta">
              <div>Shanghai, China</div>
              <div>2026.3 – 2026.7</div>
            </div>
          </div>
          <div class="tile-body">
            <ul>
              <li>Built a pricing monitoring framework for 5 European markets across 4 product categories; developed AI-assisted dashboards to track key business metrics, monitoring DAU and downloads of competitors across 15 markets.</li>
              <li>Conducted market research and strategic analysis on the e-commerce and digital advertising landscape, producing benchmarking reports to support business and investment decisions.</li>
              <li>Tracked competitors' platform features, merchant compliance, and logistics developments through expert interviews, seller training, and financial reports, delivering regular competitive intelligence reports.</li>
            </ul>
            <span class="tag">E-Commerce</span><span class="tag">Market Research</span><span class="tag">AI Dashboards</span>
          </div>
        </div>

        <div class="tile" data-category="strategy">
          <div class="tile-header">
            <div>
              <div class="tile-title">ByteDance</div>
              <div class="tile-subtitle">Strategic Operations Intern</div>
            </div>
            <div class="tile-meta">
              <div>Shanghai, China</div>
              <div>2025.6 – 2025.11</div>
            </div>
          </div>
          <div class="tile-body">
            <ul>
              <li>Conducted multi-dimensional index screening for merchants entering the TTS mall, maintained the database and product pool, configured homepage banners, and handled on-calls related to business operations.</li>
              <li>Tracked core store performance indicators through data analysis across multiple dimensions, offboarding merchants failing to meet standards for 3 consecutive months.</li>
              <li>Participated in reviewing the newly added brand tone in mid-July, collaborating with product and RD teams to run product tests and author feedback reports.</li>
            </ul>
            <span class="tag">Operations</span><span class="tag">Data Analysis</span><span class="tag">Cross-functional</span>
          </div>
        </div>

        <div class="tile" data-category="strategy">
          <div class="tile-header">
            <div>
              <div class="tile-title">Estée Lauder</div>
              <div class="tile-subtitle">Strategy Analyst Intern</div>
            </div>
            <div class="tile-meta">
              <div>Shanghai, China</div>
              <div>2025.1 – 2026.6</div>
            </div>
          </div>
          <div class="tile-body">
            <ul>
              <li>Analyzed and synthesized comprehensive Sephora channel sales data from online and offline sources; independently generated and delivered monthly brand performance reports to inform strategic decision-making.</li>
              <li>Conducted in-depth competitive analysis during key promotional campaigns (e.g., Chinese Valentine’s Day), tracking and comparing competitors across physical and online channels to guide marketing adjustments.</li>
            </ul>
            <span class="tag">Retail Analytics</span><span class="tag">Competitive Analysis</span><span class="tag">Reporting</span>
          </div>
        </div>

        <div class="tile" data-category="digital">
          <div class="tile-header">
            <div>
              <div class="tile-title">Bao Communications</div>
              <div class="tile-subtitle">Public Relations Intern</div>
            </div>
            <div class="tile-meta">
              <div>Remote from Shanghai (NYC Base)</div>
              <div>2025.4 – 2025.6</div>
            </div>
          </div>
          <div class="tile-body">
            <ul>
              <li>Identified and reached out to targeted influencers on Instagram, YouTube, and TikTok to complete assessments and promotions for over 100 top-tier creators.</li>
              <li>Partnered with Nongfu Spring influencers to edit 20 short videos, balancing individual creator styles with target brand messaging.</li>
            </ul>
            <span class="tag">Influencer Marketing</span><span class="tag">Content Strategy</span><span class="tag">Media Outreach</span>
          </div>
        </div>

        <div class="tile" data-category="digital">
          <div class="tile-header">
            <div>
              <div class="tile-title">Gusto Collective</div>
              <div class="tile-subtitle">Digital Marketing Intern</div>
            </div>
            <div class="tile-meta">
              <div>Shanghai, China</div>
              <div>2024.8 – 2024.12</div>
            </div>
          </div>
          <div class="tile-body">
            <ul>
              <li>Managed daily content publishing and community engagement on RED, Weibo, and WeChat; evaluated monthly advertising effectiveness and conversion efficiency via data-driven reports.</li>
              <li>Monitored competitor campaigns in personal care and luxury retail, researching celebrity endorsement strategies and promotional techniques to inform client proposals.</li>
            </ul>
            <span class="tag">Social Media</span><span class="tag">Luxury & Personal Care</span><span class="tag">Campaign Research</span>
          </div>
        </div>

      </div>
    </section>

    <!-- Additional Information Section -->
    <section id="additional">
      <h2 class="section-title">Additional Information</h2>
      <div class="info-grid">
        
        <div class="info-card">
          <h4>Technical Skills</h4>
          <p>Python, SQL, Office (Excel, PowerPoint, Word), Canva, CapCut</p>
        </div>

        <div class="info-card">
          <h4>Languages</h4>
          <p>English (TOEFL: 113, GRE: 326)</p>
          <p>Spanish (A2)</p>
        </div>

        <div class="info-card">
          <h4>Interests</h4>
          <p>Movies, Reading, Badminton, Yoga</p>
        </div>

      </div>
    </section>

  </main>

  <footer>
    <p>&copy; 2026 Yiyun Shen. Built for GitHub Pages.</p>
  </footer>

  <!-- Filter Functionality Script -->
  <script>
    function filterExperience(category) {
      const buttons = document.querySelectorAll('.filter-btn');
      const tiles = document.querySelectorAll('#experience .tile');

      buttons.forEach(btn => btn.classList.remove('active'));
      event.target.classList.add('active');

      tiles.forEach(tile => {
        if (category === 'all' || tile.getAttribute('data-category') === category) {
          tile.style.display = 'block';
        } else {
          tile.style.display = 'none';
        }
      });
    }
  </script>
</body>
</html>
