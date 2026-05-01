<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Feed | Grownik Professional Network</title>
  <style>
    /* --- BASE VARIABLES --- */
    :root {
      --primary: #0a66c2;
      --primary-hover: #004182;
      --bg-color: #f3f2ef;
      --surface: #ffffff;
      --text-main: rgba(0, 0, 0, 0.9);
      --text-muted: rgba(0, 0, 0, 0.6);
      --border: #e0e0e0;
      --radius: 8px;
      --font-family: system-ui, -apple-system, sans-serif;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: var(--font-family);
      background-color: var(--bg-color);
      color: var(--text-main);
      padding-top: 60px; /* Space for fixed navbar */
    }

    a { text-decoration: none; color: inherit; }
    ul { list-style: none; }
    button { cursor: pointer; font-family: inherit; }

    /* --- NAVBAR --- */
    .navbar {
      position: fixed;
      top: 0; left: 0; right: 0;
      height: 60px;
      background-color: var(--surface);
      border-bottom: 1px solid var(--border);
      display: flex;
      justify-content: center;
      z-index: 1000;
    }

    .nav-container {
      width: 100%;
      max-width: 1128px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 15px;
    }

    .nav-left { display: flex; align-items: center; gap: 10px; }
    .brand { font-size: 24px; font-weight: 800; color: var(--primary); letter-spacing: -1px; }
    
    .search-box {
      background-color: #eef3f8;
      border-radius: 4px;
      padding: 0 10px;
      display: flex;
      align-items: center;
      height: 34px;
      width: 280px;
    }
    .search-box input {
      border: none; background: transparent; outline: none;
      width: 100%; font-size: 14px; margin-left: 8px;
    }

    .nav-right { display: flex; align-items: center; gap: 30px; }
    .nav-icon {
      display: flex; flex-direction: column; align-items: center;
      color: var(--text-muted); font-size: 12px; gap: 4px; transition: color 0.2s;
    }
    .nav-icon:hover, .nav-icon.active { color: var(--text-main); border-bottom: 2px solid var(--text-main); padding-bottom: 2px;}
    .nav-icon i { font-size: 18px; }

    /* --- MAIN LAYOUT GRID --- */
    .container {
      max-width: 1128px;
      margin: 24px auto;
      display: grid;
      grid-template-columns: 225px 1fr 300px;
      gap: 24px;
      padding: 0 15px;
    }

    /* Common Card Style */
    .card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      overflow: hidden;
      margin-bottom: 16px;
    }

    /* --- LEFT SIDEBAR (Profile Snapshot) --- */
    .profile-card { text-align: center; }
    .profile-banner { height: 60px; background: linear-gradient(135deg, #a0b4b7, #eef3f8); }
    .profile-pic {
      width: 72px; height: 72px; border-radius: 50%;
      border: 2px solid var(--surface);
      margin: -36px auto 12px; background: #fff;
      display: flex; justify-content: center; align-items: center;
      font-size: 30px;
    }
    .profile-info { padding: 0 16px 16px; border-bottom: 1px solid var(--border); }
    .profile-name { font-weight: 600; font-size: 16px; }
    .profile-name:hover { text-decoration: underline; cursor: pointer; }
    .profile-headline { font-size: 12px; color: var(--text-muted); margin-top: 4px; }
    
    .profile-stats { padding: 12px 0; font-size: 12px; font-weight: 600;}
    .stat-row { display: flex; justify-content: space-between; padding: 4px 16px; color: var(--text-muted); transition: background 0.2s; cursor: pointer;}
    .stat-row:hover { background: rgba(0,0,0,0.05); }
    .stat-num { color: var(--primary); }

    /* --- CENTER FEED --- */
    /* Create Post Box */
    .create-post { padding: 16px; }
    .create-input-area { display: flex; gap: 12px; margin-bottom: 12px; }
    .create-input-area .avatar {
      width: 48px; height: 48px; border-radius: 50%; background: #eef3f8;
      display: flex; justify-content: center; align-items: center; font-size: 20px;
    }
    .create-btn {
      flex: 1; border: 1px solid var(--text-muted); border-radius: 30px;
      background: transparent; text-align: left; padding: 0 16px;
      font-size: 14px; color: var(--text-muted); font-weight: 600; transition: background 0.2s;
    }
    .create-btn:hover { background: rgba(0,0,0,0.05); }
    .create-actions { display: flex; justify-content: space-between; padding: 0 8px; }
    .action-btn { 
      background: transparent; border: none; display: flex; align-items: center; gap: 8px;
      font-size: 14px; font-weight: 600; color: var(--text-muted); padding: 12px; border-radius: 4px; transition: background 0.2s;
    }
    .action-btn:hover { background: rgba(0,0,0,0.05); }
    .action-btn.photo { color: #378fe9; }
    .action-btn.video { color: #5f9b41; }
    .action-btn.article { color: #e16745; }

    /* Feed Post */
    .post { padding: 0; }
    .post-header { display: flex; gap: 12px; padding: 16px; }
    .post-avatar { width: 48px; height: 48px; border-radius: 50%; background: #eef3f8; display: flex; justify-content: center; align-items: center; font-size: 20px; }
    .post-meta { flex: 1; }
    .post-author { font-weight: 600; font-size: 14px; }
    .post-headline { font-size: 12px; color: var(--text-muted); }
    .post-time { font-size: 12px; color: var(--text-muted); }
    
    .post-content { padding: 0 16px 16px; font-size: 14px; }
    .post-image { width: 100%; height: auto; max-height: 400px; object-fit: cover; border-top: 1px solid var(--border); border-bottom: 1px solid var(--border); }
    
    .post-stats { padding: 8px 16px; font-size: 12px; color: var(--text-muted); border-bottom: 1px solid var(--border); }
    .post-actions { display: flex; justify-content: space-around; padding: 4px 8px; }
    .interact-btn { 
      background: transparent; border: none; display: flex; align-items: center; gap: 6px;
      font-size: 14px; font-weight: 600; color: var(--text-muted); padding: 12px 24px; border-radius: 4px;
    }
    .interact-btn:hover { background: rgba(0,0,0,0.05); }
    .interact-btn.liked { color: var(--primary); }

    /* --- RIGHT SIDEBAR (News & Recommendations) --- */
    .news-card { padding: 16px; }
    .news-header { font-size: 16px; font-weight: 600; margin-bottom: 12px; }
    .news-list li { margin-bottom: 12px; cursor: pointer; }
    .news-title { font-size: 14px; font-weight: 600; color: var(--text-main); }
    .news-title:hover { color: var(--primary); text-decoration: underline; }
    .news-meta { font-size: 12px; color: var(--text-muted); margin-top: 2px; }

    /* --- RESPONSIVE DESIGN --- */
    @media (max-width: 992px) {
      .container { grid-template-columns: 225px 1fr; }
      .sidebar-right { display: none; }
    }
    @media (max-width: 768px) {
      .container { grid-template-columns: 1fr; }
      .sidebar-left { display: none; }
      .search-box { width: 200px; }
      .nav-right span { display: none; } /* Hide text under icons on mobile */
    }
  </style>
</head>
<body>

  <nav class="navbar">
    <div class="nav-container">
      <div class="nav-left">
        <div class="brand">Grownik</div>
        <div class="search-box">
          <span>🔍</span>
          <input type="text" placeholder="Search">
        </div>
      </div>
      <div class="nav-right">
        <a href="#" class="nav-icon active"><span>🏠</span><span>Home</span></a>
        <a href="#" class="nav-icon"><span>👥</span><span>My Network</span></a>
        <a href="#" class="nav-icon"><span>💼</span><span>Jobs</span></a>
        <a href="#" class="nav-icon"><span>💬</span><span>Messaging</span></a>
        <a href="#" class="nav-icon"><span>🔔</span><span>Notifications</span></a>
      </div>
    </div>
  </nav>

  <main class="container">
    
    <aside class="sidebar-left">
      <div class="card profile-card">
        <div class="profile-banner"></div>
        <div class="profile-pic">👨‍💼</div>
        <div class="profile-info">
          <div class="profile-name">User Name</div>
          <div class="profile-headline">IT Talent Acquisition | HRMS Solutions Expert</div>
        </div>
        <div class="profile-stats">
          <div class="stat-row">
            <span>Profile viewers</span>
            <span class="stat-num">47</span>
          </div>
          <div class="stat-row">
            <span>Connections</span>
            <span class="stat-num">500+</span>
          </div>
        </div>
      </div>
    </aside>

    <section class="feed">
      <div class="card create-post">
        <div class="create-input-area">
          <div class="avatar">👨‍💼</div>
          <button class="create-btn">Start a post, share your IT roles...</button>
        </div>
        <div class="create-actions">
          <button class="action-btn photo"><span>📷</span> Media</button>
          <button class="action-btn video"><span>📅</span> Event</button>
          <button class="action-btn article"><span>📝</span> Write article</button>
        </div>
      </div>

      <div class="card post">
        <div class="post-header">
          <div class="post-avatar">🏢</div>
          <div class="post-meta">
            <div class="post-author">Global Tech Solutions</div>
            <div class="post-headline">Innovative HRMS Platforms | 100,000+ Followers</div>
            <div class="post-time">2h • 🌐</div>
          </div>
        </div>
        <div class="post-content">
          We are thrilled to announce our latest integration tools for global payroll management. Streamline your recruitment process today with Grownik's enterprise solutions. Let us know your thoughts below! #HRTech #Recruitment #Innovation
        </div>
        <div style="background: #eef3f8; height: 250px; display: flex; justify-content: center; align-items: center; color: var(--text-muted); border-top: 1px solid var(--border); border-bottom: 1px solid var(--border); margin-top: 12px;">
          [ Infographic on HR Technology Trends ]
        </div>
        <div class="post-stats">👍 142 • 28 comments</div>
        <div class="post-actions">
          <button class="interact-btn" onclick="this.classList.toggle('liked')"><span>👍</span> Like</button>
          <button class="interact-btn"><span>💬</span> Comment</button>
          <button class="interact-btn"><span>🔁</span> Repost</button>
          <button class="interact-btn"><span>↗️</span> Send</button>
        </div>
      </div>

      <div class="card post">
        <div class="post-header">
          <div class="post-avatar">👩‍💻</div>
          <div class="post-meta">
            <div class="post-author">Sarah Jenkins</div>
            <div class="post-headline">Senior Workday Consultant | Open to work</div>
            <div class="post-time">5h • 🌐</div>
          </div>
        </div>
        <div class="post-content">
          Just earned my new Workday certification! 🚀 Looking forward to connecting with recruiters in the EU and UK markets who are looking for HCM implementation specialists. 
        </div>
        <div class="post-stats">👍 89 • 12 comments</div>
        <div class="post-actions">
          <button class="interact-btn" onclick="this.classList.toggle('liked')"><span>👍</span> Like</button>
          <button class="interact-btn"><span>💬</span> Comment</button>
          <button class="interact-btn"><span>🔁</span> Repost</button>
          <button class="interact-btn"><span>↗️</span> Send</button>
        </div>
      </div>
    </section>

    <aside class="sidebar-right">
      <div class="card news-card">
        <div class="news-header">Grownik News</div>
        <ul class="news-list">
          <li>
            <div class="news-title">The rise of AI in recruitment</div>
            <div class="news-meta">Top news • 10,432 readers</div>
          </li>
          <li>
            <div class="news-title">Investment banking hiring trends</div>
            <div class="news-meta">14h ago • 5,210 readers</div>
          </li>
          <li>
            <div class="news-title">Managing global payroll via HRMS</div>
            <div class="news-meta">1d ago • 3,890 readers</div>
          </li>
          <li>
            <div class="news-title">Remote work in the IT sector</div>
            <div class="news-meta">2d ago • 12,045 readers</div>
          </li>
        </ul>
      </div>
    </aside>

  </main>

  <script>
    // Simple JavaScript to make the search bar interactive
    const searchInput = document.querySelector('.search-box input');
    const searchBox = document.querySelector('.search-box');
    
    searchInput.addEventListener('focus', () => {
      searchBox.style.border = '2px solid var(--primary)';
      searchBox.style.backgroundColor = '#fff';
    });
    
    searchInput.addEventListener('blur', () => {
      searchBox.style.border = 'none';
      searchBox.style.backgroundColor = '#eef3f8';
    });
  </script>
</body>
</html>
