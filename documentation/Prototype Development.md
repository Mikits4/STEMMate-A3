<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>STEMMate — Find & Save an Activity</title>
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>

  <!-- SCREEN: HOME -->
  <section id="screen-home" class="screen active">
    <header class="app-header">
      <h1>Welcome, Facilitator</h1>
      <p>Find practical STEM activities and prepare your next session.</p>
    </header>

    <main class="menu">
      <button class="menu-card" data-goto="screen-browser">
        <span class="icon">🔍</span>
        <div>
          <strong>Find Activities</strong>
          <small>Search and filter STEM activities.</small>
        </div>
        <span class="chevron">›</span>
      </button>

      <button class="menu-card" data-goto="screen-saved">
        <span class="icon">🔖</span>
        <div>
          <strong>Saved Activities</strong>
          <small>Open activities saved on this device.</small>
        </div>
        <span class="chevron">›</span>
      </button>

      <button class="menu-card" data-goto="screen-plans">
        <span class="icon">🗓️</span>
        <div>
          <strong>Session Plans</strong>
          <small>Create or view a session plan.</small>
        </div>
        <span class="chevron">›</span>
      </button>
    </main>

    <button class="offline-pill" id="offlineToggle">View offline screen</button>

    <nav class="bottom-nav">
      <button class="nav-item active" data-goto="screen-home">🏠<span>Home</span></button>
      <button class="nav-item" data-goto="screen-browser">🔍<span>Activities</span></button>
      <button class="nav-item" data-goto="screen-saved">🔖<span>Saved</span></button>
      <button class="nav-item" data-goto="screen-plans">🗓️<span>Plans</span></button>
    </nav>
  </section>

  <!-- SCREEN: ACTIVITY BROWSER -->
  <section id="screen-browser" class="screen">
    <header class="app-header small">
      <button class="back" data-goto="screen-home">‹</button>
      <h2>Activity Browser</h2>
    </header>

    <div class="search-bar">
      <input type="text" id="searchInput" placeholder="Search activities…" />
    </div>

    <main id="activityList" class="card-list"></main>
  </section>

  <!-- SCREEN: ACTIVITY DETAILS -->
  <section id="screen-details" class="screen">
    <header class="app-header small">
      <button class="back" data-goto="screen-browser">‹</button>
      <h2 id="detailTitle">Activity</h2>
    </header>

    <main class="detail-body">
      <p id="detailDescription" class="detail-desc"></p>

      <h3>Instructions</h3>
      <ol id="detailSteps"></ol>

      <h3>Requirements</h3>
      <ul id="detailReqs"></ul>

      <button id="saveBtn" class="primary-btn">Save Activity</button>
      <p id="saveFeedback" class="feedback" aria-live="polite"></p>
    </main>
  </section>

  <!-- SCREEN: SAVED ACTIVITIES -->
  <section id="screen-saved" class="screen">
    <header class="app-header small">
      <button class="back" data-goto="screen-home">‹</button>
      <h2>Saved Activities</h2>
    </header>
    <main id="savedList" class="card-list"></main>
  </section>

  <!-- SCREEN: SESSION PLANS -->
  <section id="screen-plans" class="screen">
    <header class="app-header small">
      <button class="back" data-goto="screen-home">‹</button>
      <h2>Session Plans</h2>
    </header>
    <main class="card-list">
      <p class="placeholder">No session plans yet.</p>
    </main>
  </section>

  <script src="js/app.js"></script>
</body>
</html>
