<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>HydroControl</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;800&display=swap" rel="stylesheet">

<style>
  :root {
    --bg: #050f0a;
    --surface: #0b1f13;
    --surface2: #112718;
    --border: #1e4029;
    --green: #00ff6a;
    --green-dim: #00cc54;
    --green-glow: rgba(0,255,106,0.15);
    --cyan: #00e5ff;
    --amber: #ffb700;
    --red: #ff3d3d;
    --text: #d4f0dc;
    --text-dim: #5a8c6a;
    --text-muted: #2e5038;
    --font-display: 'Syne', sans-serif;
    --font-mono: 'Space Mono', monospace;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--font-mono);
    min-height: 100vh;
    overflow-x: hidden;
    position: relative;
  }

  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background:
      radial-gradient(ellipse 60% 40% at 20% 10%, rgba(0,255,106,0.06) 0%, transparent 60%),
      radial-gradient(ellipse 40% 60% at 80% 80%, rgba(0,229,255,0.04) 0%, transparent 60%);
    pointer-events: none;
    z-index: 0;
  }

  /* Scanline effect */
  body::after {
    content: '';
    position: fixed;
    inset: 0;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 3px,
      rgba(0,0,0,0.08) 3px,
      rgba(0,0,0,0.08) 4px
    );
    pointer-events: none;
    z-index: 999;
  }

  .app {
    max-width: 480px;
    margin: 0 auto;
    padding: 0 0 100px;
    position: relative;
    z-index: 1;
  }

  /* ---- HEADER ---- */
  .header {
    padding: 20px 20px 16px;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: sticky;
    top: 0;
    background: rgba(5,15,10,0.92);
    backdrop-filter: blur(12px);
    z-index: 100;
  }

  .logo {
    font-family: var(--font-display);
    font-weight: 800;
    font-size: 22px;
    letter-spacing: -0.5px;
    color: var(--green);
    text-shadow: 0 0 20px rgba(0,255,106,0.5);
  }

  .logo span {
    color: var(--text-dim);
    font-weight: 400;
    font-size: 12px;
    display: block;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-top: -2px;
  }

  .conn-badge {
    display: flex;
    align-items: center;
    gap: 6px;
    font-size: 11px;
    color: var(--text-dim);
    letter-spacing: 1px;
  }

  .conn-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: var(--text-muted);
    transition: all 0.3s;
  }

  .conn-dot.live {
    background: var(--green);
    box-shadow: 0 0 8px var(--green);
    animation: pulse-dot 2s infinite;
  }

  .conn-dot.error { background: var(--red); box-shadow: 0 0 8px var(--red); }

  @keyframes pulse-dot {
    0%,100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  /* ---- SECTIONS ---- */
  .section { padding: 20px 16px 0; }

  .section-label {
    font-size: 10px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--text-muted);
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ---- LAST UPDATE ---- */
  .last-update {
    text-align: center;
    font-size: 10px;
    color: var(--text-muted);
    padding: 8px 16px 0;
    letter-spacing: 1px;
  }

  /* ---- MODE TOGGLE ---- */
  .mode-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 16px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
  }

  .mode-info { flex: 1; }
  .mode-title {
    font-family: var(--font-display);
    font-size: 14px;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 2px;
  }
  .mode-subtitle { font-size: 11px; color: var(--text-dim); }

  .mode-toggle {
    display: flex;
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: 8px;
    overflow: hidden;
  }

  .mode-btn {
    padding: 8px 16px;
    font-family: var(--font-mono);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 1px;
    border: none;
    cursor: pointer;
    transition: all 0.2s;
    background: transparent;
    color: var(--text-muted);
  }

  .mode-btn.active[data-mode="auto"] {
    background: var(--green);
    color: var(--bg);
  }
  .mode-btn.active[data-mode="manual"] {
    background: var(--amber);
    color: var(--bg);
  }

  /* ---- SENSOR CARDS ---- */
  .sensor-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
  }

  .sensor-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 14px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s;
  }

  .sensor-card.full-width { grid-column: 1 / -1; }

  .sensor-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: var(--green);
    opacity: 0;
    transition: opacity 0.3s;
  }

  .sensor-card.status-critical::before { opacity: 1; background: var(--red); }
  .sensor-card.status-low::before { opacity: 1; background: var(--amber); }
  .sensor-card.status-normal::before,
  .sensor-card.status-full::before { opacity: 1; background: var(--green); }

  .sensor-icon {
    font-size: 20px;
    margin-bottom: 8px;
    display: block;
  }

  .sensor-label {
    font-size: 9px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--text-muted);
    margin-bottom: 4px;
  }

  .sensor-value {
    font-family: var(--font-display);
    font-size: 28px;
    font-weight: 800;
    line-height: 1;
    color: var(--green);
    transition: color 0.3s;
  }

  .sensor-card.status-critical .sensor-value { color: var(--red); }
  .sensor-card.status-low .sensor-value { color: var(--amber); }

  .sensor-unit {
    font-size: 12px;
    color: var(--text-dim);
    font-weight: 400;
  }

  .sensor-status {
    margin-top: 6px;
    font-size: 10px;
    letter-spacing: 1px;
    text-transform: uppercase;
    padding: 3px 8px;
    border-radius: 4px;
    display: inline-block;
    background: var(--surface2);
    color: var(--text-dim);
  }

  .status-critical .sensor-status { background: rgba(255,61,61,0.15); color: var(--red); }
  .status-low .sensor-status { background: rgba(255,183,0,0.15); color: var(--amber); }
  .status-normal .sensor-status,
  .status-full .sensor-status { background: rgba(0,255,106,0.1); color: var(--green); }

  /* ---- TANK LEVEL BAR ---- */
  .tank-bar-wrap {
    margin-top: 10px;
  }
  .tank-bar-track {
    height: 8px;
    background: var(--surface2);
    border-radius: 4px;
    overflow: hidden;
    margin-bottom: 4px;
  }
  .tank-bar-fill {
    height: 100%;
    border-radius: 4px;
    background: var(--green);
    transition: width 0.8s cubic-bezier(.4,0,.2,1), background 0.3s;
    box-shadow: 0 0 8px rgba(0,255,106,0.4);
  }
  .tank-bar-fill.low { background: var(--amber); box-shadow: 0 0 8px rgba(255,183,0,0.4); }
  .tank-bar-fill.critical { background: var(--red); box-shadow: 0 0 8px rgba(255,61,61,0.4); }

  .tank-bar-labels {
    display: flex;
    justify-content: space-between;
    font-size: 9px;
    color: var(--text-muted);
    letter-spacing: 1px;
  }

  /* ---- ACTUATOR CONTROLS ---- */
  .actuator-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
  }

  .actuator-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 16px;
    display: flex;
    flex-direction: column;
    gap: 12px;
    transition: border-color 0.3s, background 0.3s;
  }

  .actuator-card.active {
    border-color: var(--green);
    background: rgba(0,255,106,0.04);
  }

  .actuator-header {
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .actuator-icon {
    font-size: 22px;
    width: 36px;
    height: 36px;
    background: var(--surface2);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .actuator-card.active .actuator-icon {
    background: rgba(0,255,106,0.12);
  }

  .actuator-name {
    font-family: var(--font-display);
    font-size: 13px;
    font-weight: 600;
    color: var(--text);
  }

  .actuator-state {
    font-size: 10px;
    letter-spacing: 1px;
    color: var(--text-muted);
  }

  .actuator-card.active .actuator-state { color: var(--green); }

  /* Big Toggle Switch */
  .toggle-switch {
    position: relative;
    display: block;
    width: 100%;
    height: 44px;
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.2s;
    user-select: none;
    -webkit-user-select: none;
    overflow: hidden;
  }

  .toggle-switch.on {
    background: rgba(0,255,106,0.1);
    border-color: var(--green);
  }

  .toggle-switch.disabled {
    opacity: 0.35;
    cursor: not-allowed;
    pointer-events: none;
  }

  .toggle-switch::before {
    content: attr(data-label);
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: var(--font-mono);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 2px;
    color: var(--text-muted);
    transition: all 0.2s;
  }

  .toggle-switch.on::before {
    color: var(--green);
    text-shadow: 0 0 10px rgba(0,255,106,0.5);
  }

  /* Active animation */
  @keyframes active-pulse {
    0%,100% { box-shadow: 0 0 0 0 rgba(0,255,106,0.3); }
    50% { box-shadow: 0 0 0 4px rgba(0,255,106,0); }
  }

  .actuator-card.active .toggle-switch.on {
    animation: active-pulse 2s infinite;
  }

  /* ---- EMERGENCY STOP ---- */
  .estop-wrap {
    padding: 16px;
  }

  .estop-btn {
    width: 100%;
    padding: 16px;
    background: rgba(255,61,61,0.08);
    border: 1px solid rgba(255,61,61,0.3);
    border-radius: 12px;
    color: var(--red);
    font-family: var(--font-mono);
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 3px;
    cursor: pointer;
    transition: all 0.2s;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
  }

  .estop-btn:active {
    background: rgba(255,61,61,0.2);
    transform: scale(0.98);
  }

  /* ---- LOADING OVERLAY ---- */
  .loading {
    position: fixed;
    inset: 0;
    background: var(--bg);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 16px;
    z-index: 9999;
    transition: opacity 0.5s;
  }

  .loading.hidden { opacity: 0; pointer-events: none; }

  .loading-logo {
    font-family: var(--font-display);
    font-weight: 800;
    font-size: 32px;
    color: var(--green);
    text-shadow: 0 0 30px rgba(0,255,106,0.6);
  }

  .loading-bar {
    width: 160px;
    height: 2px;
    background: var(--border);
    border-radius: 1px;
    overflow: hidden;
  }

  .loading-bar-fill {
    height: 100%;
    width: 0;
    background: var(--green);
    border-radius: 1px;
    animation: load-fill 1.5s ease forwards;
  }

  @keyframes load-fill {
    to { width: 100%; }
  }

  .loading-text {
    font-size: 10px;
    letter-spacing: 3px;
    color: var(--text-muted);
    text-transform: uppercase;
    animation: blink 1s infinite;
  }

  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0.3} }

  /* ---- TOAST ---- */
  .toast {
    position: fixed;
    bottom: 90px;
    left: 50%;
    transform: translateX(-50%) translateY(20px);
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 10px 18px;
    font-size: 12px;
    letter-spacing: 1px;
    color: var(--text);
    opacity: 0;
    transition: all 0.3s;
    pointer-events: none;
    white-space: nowrap;
    z-index: 500;
  }

  .toast.show {
    opacity: 1;
    transform: translateX(-50%) translateY(0);
  }

  .toast.success { border-color: var(--green); color: var(--green); }
  .toast.error { border-color: var(--red); color: var(--red); }

  /* ---- BOTTOM NAV ---- */
  .bottom-nav {
    position: fixed;
    bottom: 0; left: 0; right: 0;
    background: rgba(5,15,10,0.95);
    backdrop-filter: blur(12px);
    border-top: 1px solid var(--border);
    display: flex;
    justify-content: space-around;
    padding: 12px 0 max(12px, env(safe-area-inset-bottom));
    z-index: 200;
  }

  .nav-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 4px;
    font-size: 9px;
    letter-spacing: 1px;
    color: var(--text-muted);
    cursor: pointer;
    transition: color 0.2s;
    padding: 0 20px;
  }

  .nav-item.active { color: var(--green); }
  .nav-icon { font-size: 20px; line-height: 1; }

  /* ---- PAGES ---- */
  .page { display: none; }
  .page.active { display: block; animation: fade-in 0.3s ease; }

  @keyframes fade-in { from { opacity: 0; transform: translateY(6px); } to { opacity: 1; transform: none; } }

  /* ---- HISTORY LOG ---- */
  .log-list {
    padding: 0 16px;
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  .log-item {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 10px 12px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .log-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    flex-shrink: 0;
  }

  .log-dot.green { background: var(--green); }
  .log-dot.amber { background: var(--amber); }
  .log-dot.red { background: var(--red); }

  .log-msg { font-size: 11px; color: var(--text); flex: 1; }
  .log-time { font-size: 10px; color: var(--text-muted); flex-shrink: 0; }

  /* ---- SETTINGS ---- */
  .settings-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    margin: 0 16px 10px;
    overflow: hidden;
  }

  .setting-row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 14px 16px;
    border-bottom: 1px solid var(--border);
  }

  .setting-row:last-child { border-bottom: none; }

  .setting-label {
    font-size: 13px;
    color: var(--text);
    font-family: var(--font-display);
    font-weight: 600;
  }

  .setting-sub {
    font-size: 10px;
    color: var(--text-dim);
    margin-top: 1px;
    font-family: var(--font-mono);
  }

  .setting-value {
    font-size: 12px;
    color: var(--green);
    font-family: var(--font-mono);
    text-align: right;
  }

  .refresh-btn {
    width: calc(100% - 32px);
    margin: 0 16px;
    padding: 13px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    color: var(--text-dim);
    font-family: var(--font-mono);
    font-size: 11px;
    letter-spacing: 2px;
    cursor: pointer;
    transition: all 0.2s;
    text-transform: uppercase;
  }

  .refresh-btn:active { transform: scale(0.98); border-color: var(--green); color: var(--green); }
</style>
</head>
<body>

<!-- Loading -->
<div class="loading" id="loading">
  <div class="loading-logo">HYDRO</div>
  <div class="loading-bar"><div class="loading-bar-fill"></div></div>
  <div class="loading-text">Connecting to Firebase</div>
</div>

<!-- App -->
<div class="app" id="app" style="display:none">

  <!-- Header -->
  <div class="header">
    <div class="logo">HYDRO<span>CONTROL / DEVICE-001</span></div>
    <div class="conn-badge">
      <div class="conn-dot" id="connDot"></div>
      <span id="connLabel">OFFLINE</span>
    </div>
  </div>

  <!-- Dashboard Page -->
  <div class="page active" id="page-dash">

    <div class="section">
      <div class="section-label">Operating Mode</div>
      <div class="mode-card">
        <div class="mode-info">
          <div class="mode-title" id="modeTitle">AUTO MODE</div>
          <div class="mode-subtitle" id="modeSubtitle">System managing actuators</div>
        </div>
        <div class="mode-toggle">
          <button class="mode-btn active" data-mode="auto" id="btnAuto" onclick="setMode('auto')">AUTO</button>
          <button class="mode-btn" data-mode="manual" id="btnManual" onclick="setMode('manual')">MANUAL</button>
        </div>
      </div>
    </div>

    <div class="section">
      <div class="section-label">Storage Tank</div>
      <div class="sensor-grid">
        <div class="sensor-card" id="tankLevelCard">
          <span class="sensor-icon">💧</span>
          <div class="sensor-label">Level</div>
          <div class="sensor-value" id="tankLevelVal">—<span class="sensor-unit">%</span></div>
          <div class="sensor-status" id="tankLevelStatus">—</div>
          <div class="tank-bar-wrap">
            <div class="tank-bar-track">
              <div class="tank-bar-fill" id="tankBarFill" style="width:0%"></div>
            </div>
            <div class="tank-bar-labels"><span>0</span><span>50</span><span>100</span></div>
          </div>
        </div>
        <div class="sensor-card" id="tankDistCard">
          <span class="sensor-icon">📡</span>
          <div class="sensor-label">Distance</div>
          <div class="sensor-value" id="tankDistVal">—<span class="sensor-unit">cm</span></div>
          <div class="sensor-status" id="valveStatus">VALVE —</div>
        </div>
      </div>
    </div>

    <div class="section">
      <div class="section-label">Plant Tray</div>
      <div class="sensor-grid">
        <div class="sensor-card" id="plantCard">
          <span class="sensor-icon">🌱</span>
          <div class="sensor-label">Moisture</div>
          <div class="sensor-value" id="plantVal">—</div>
          <div class="sensor-status" id="plantStatus">—</div>
        </div>
        <div class="sensor-card" id="pumpCard">
          <span class="sensor-icon">⚙️</span>
          <div class="sensor-label">Pump</div>
          <div class="sensor-value" id="pumpVal">—</div>
          <div class="sensor-status" id="pumpStatus">—</div>
        </div>
      </div>
    </div>

    <div class="section">
      <div class="section-label">Actuator Control</div>
      <div class="actuator-grid">
        <div class="actuator-card" id="pumpCard2">
          <div class="actuator-header">
            <div class="actuator-icon">⚙️</div>
            <div>
              <div class="actuator-name">Pump</div>
              <div class="actuator-state" id="pumpStateLabel">OFF</div>
            </div>
          </div>
          <div class="toggle-switch disabled" id="pumpToggle" data-label="OFF" onclick="togglePump()"></div>
        </div>
        <div class="actuator-card" id="valveCard2">
          <div class="actuator-header">
            <div class="actuator-icon">🔧</div>
            <div>
              <div class="actuator-name">Valve</div>
              <div class="actuator-state" id="valveStateLabel">CLOSED</div>
            </div>
          </div>
          <div class="toggle-switch disabled" id="valveToggle" data-label="CLOSED" onclick="toggleValve()"></div>
        </div>
      </div>
    </div>

    <div class="estop-wrap">
      <button class="estop-btn" onclick="emergencyStop()">⛔ EMERGENCY STOP</button>
    </div>

    <div class="last-update" id="lastUpdateEl">LAST UPDATE: —</div>

  </div><!-- /page-dash -->

  <!-- Log Page -->
  <div class="page" id="page-log">
    <div class="section">
      <div class="section-label">Activity Log</div>
    </div>
    <div class="log-list" id="logList"></div>
  </div>

  <!-- Settings Page -->
  <div class="page" id="page-settings">
    <div class="section">
      <div class="section-label">Device Info</div>
    </div>
    <div class="settings-card">
      <div class="setting-row">
        <div><div class="setting-label">Device ID</div><div class="setting-sub">Firebase path</div></div>
        <div class="setting-value">device-001</div>
      </div>
      <div class="setting-row">
        <div><div class="setting-label">Project</div><div class="setting-sub">Firebase project</div></div>
        <div class="setting-value">hydrophonics-5a253</div>
      </div>
      <div class="setting-row">
        <div><div class="setting-label">WiFi Status</div><div class="setting-sub">Device connection</div></div>
        <div class="setting-value" id="wifiStatus">—</div>
      </div>
      <div class="setting-row">
        <div><div class="setting-label">Refresh Rate</div><div class="setting-sub">Sensor interval</div></div>
        <div class="setting-value">5 SEC</div>
      </div>
    </div>

    <div class="section">
      <div class="section-label">Thresholds</div>
    </div>
    <div class="settings-card">
      <div class="setting-row">
        <div><div class="setting-label">Plant Low</div><div class="setting-sub">Trigger pump ON</div></div>
        <div class="setting-value">&lt; 350</div>
      </div>
      <div class="setting-row">
        <div><div class="setting-label">Plant High</div><div class="setting-sub">Trigger pump OFF</div></div>
        <div class="setting-value">&gt; 600</div>
      </div>
      <div class="setting-row">
        <div><div class="setting-label">Tank Low</div><div class="setting-sub">Open valve</div></div>
        <div class="setting-value">≥ 20 cm</div>
      </div>
      <div class="setting-row">
        <div><div class="setting-label">Tank Full</div><div class="setting-sub">Close valve</div></div>
        <div class="setting-value">≤ 8 cm</div>
      </div>
    </div>

    <div style="height:12px"></div>
    <button class="refresh-btn" onclick="forceRefresh()">↺ Force Refresh</button>
  </div>

</div><!-- /app -->

<!-- Bottom Nav -->
<div class="bottom-nav">
  <div class="nav-item active" onclick="showPage('dash', this)">
    <div class="nav-icon">⬡</div>
    <span>DASH</span>
  </div>
  <div class="nav-item" onclick="showPage('log', this)">
    <div class="nav-icon">≡</div>
    <span>LOG</span>
  </div>
  <div class="nav-item" onclick="showPage('settings', this)">
    <div class="nav-icon">◈</div>
    <span>INFO</span>
  </div>
</div>

<!-- Toast -->
<div class="toast" id="toast"></div>

<!-- Firebase SDK -->
<script type="module">
  import { initializeApp } from "https://www.gstatic.com/firebasejs/10.12.0/firebase-app.js";
  import { getDatabase, ref, onValue, set, get } from "https://www.gstatic.com/firebasejs/10.12.0/firebase-database.js";

  const firebaseConfig = {
    apiKey: "AIzaSyBNgPoGqvhBzS1EjEVf5WQnqIM1xsMbcIo",
    authDomain: "hydrophonics-5a253.firebaseapp.com",
    databaseURL: "https://hydrophonics-5a253-default-rtdb.firebaseio.com",
    projectId: "hydrophonics-5a253",
    storageBucket: "hydrophonics-5a253.firebasestorage.app",
    messagingSenderId: "461957023892",
    appId: "1:461957023892:web:2cc6d1c82c9f8eae590c81",
    measurementId: "G-TX6MQ7Y10B"
  };

  const app = initializeApp(firebaseConfig);
  const db = getDatabase(app);
  const BASE = "devices/device-001";

  // ---- State ----
  let currentMode = 'auto';
  let pumpOn = false;
  let valveOn = false;
  const activityLog = [];

  // ---- Loading ----
  setTimeout(() => {
    document.getElementById('loading').classList.add('hidden');
    document.getElementById('app').style.display = 'block';
  }, 1800);

  // ---- Realtime Listener ----
  const deviceRef = ref(db, BASE);
  onValue(deviceRef, (snap) => {
    const data = snap.val();
    if (!data) return;

    setConnected(true);

    const sensors = data.sensors || {};
    const status = data.status || {};
    const control = data.control || {};

    // Tank
    const tank = sensors.tank || {};
    const levelPct = tank.levelPct != null ? tank.levelPct : null;
    const distCM = tank.distanceCM != null ? tank.distanceCM : null;
    const tankStatus = (tank.status || '').toUpperCase();

    updateTankLevel(levelPct, tankStatus);
    updateTankDist(distCM);

    // Plant
    const plant = sensors.plant || {};
    const plantVal = plant.sensorValue != null ? plant.sensorValue : null;
    const plantStatus = (plant.status || '').toUpperCase();
    updatePlant(plantVal, plantStatus);

    // Actuators from status
    pumpOn = !!status.pump;
    valveOn = !!status.valve;
    updatePumpUI(pumpOn);
    updateValveUI(valveOn);

    // Mode from status
    const modeStr = (status.mode || control.mode || 'auto').toLowerCase();
    currentMode = modeStr === 'manual' ? 'manual' : 'auto';
    syncModeUI(currentMode);

    // Last update
    if (data.lastUpdate) {
      const d = new Date(data.lastUpdate * 1000);
      document.getElementById('lastUpdateEl').textContent =
        'LAST UPDATE: ' + d.toLocaleTimeString('en-PH', {hour:'2-digit', minute:'2-digit', second:'2-digit'});
    }

    document.getElementById('wifiStatus').textContent = 'CONNECTED';

  }, (err) => {
    console.error(err);
    setConnected(false);
  });

  // ---- UI Updaters ----
  function setConnected(on) {
    const dot = document.getElementById('connDot');
    const lbl = document.getElementById('connLabel');
    if (on) {
      dot.className = 'conn-dot live';
      lbl.textContent = 'LIVE';
    } else {
      dot.className = 'conn-dot error';
      lbl.textContent = 'ERROR';
    }
  }

  function updateTankLevel(pct, status) {
    const card = document.getElementById('tankLevelCard');
    const val = document.getElementById('tankLevelVal');
    const st = document.getElementById('tankLevelStatus');
    const bar = document.getElementById('tankBarFill');

    if (pct != null) {
      val.innerHTML = Math.round(pct) + '<span class="sensor-unit">%</span>';
      bar.style.width = pct + '%';
    }

    card.className = 'sensor-card';
    bar.className = 'tank-bar-fill';

    if (status === 'CRITICAL') {
      card.classList.add('status-critical');
      bar.classList.add('critical');
    } else if (status === 'LOW') {
      card.classList.add('status-low');
      bar.classList.add('low');
    } else if (status === 'FULL' || status === 'NORMAL') {
      card.classList.add('status-' + status.toLowerCase());
    }

    st.textContent = status || '—';
  }

  function updateTankDist(distCM) {
    const val = document.getElementById('tankDistVal');
    const vs = document.getElementById('valveStatus');
    if (distCM != null) {
      val.innerHTML = (distCM < 0 ? 'ERR' : distCM.toFixed(1)) + '<span class="sensor-unit">cm</span>';
    }
    vs.textContent = 'VALVE ' + (valveOn ? 'OPEN' : 'CLOSED');
  }

  function updatePlant(v, status) {
    const card = document.getElementById('plantCard');
    const val = document.getElementById('plantVal');
    const st = document.getElementById('plantStatus');

    if (v != null) val.innerHTML = v;

    card.className = 'sensor-card';
    if (status === 'LOW') card.classList.add('status-critical');
    else if (status === 'NORMAL') card.classList.add('status-normal');
    else if (status === 'FULL') card.classList.add('status-full');

    st.textContent = status || '—';
  }

  function updatePumpUI(on) {
    const toggle = document.getElementById('pumpToggle');
    const card = document.getElementById('pumpCard2');
    const lbl = document.getElementById('pumpStateLabel');
    const sCard = document.getElementById('pumpCard');
    const sVal = document.getElementById('pumpVal');
    const sSt = document.getElementById('pumpStatus');

    toggle.className = 'toggle-switch' + (on ? ' on' : '') + (currentMode === 'manual' ? '' : ' disabled');
    toggle.dataset.label = on ? 'ON' : 'OFF';
    card.className = 'actuator-card' + (on ? ' active' : '');
    lbl.textContent = on ? 'RUNNING' : 'OFF';

    sVal.innerHTML = on ? '<span style="color:var(--green)">ON</span>' : 'OFF';
    sCard.className = 'sensor-card' + (on ? ' status-normal' : '');
    sSt.textContent = on ? 'RUNNING' : 'IDLE';

    // update valve status text too
    document.getElementById('valveStatus').textContent = 'VALVE ' + (valveOn ? 'OPEN' : 'CLOSED');
  }

  function updateValveUI(open) {
    const toggle = document.getElementById('valveToggle');
    const card = document.getElementById('valveCard2');
    const lbl = document.getElementById('valveStateLabel');

    toggle.className = 'toggle-switch' + (open ? ' on' : '') + (currentMode === 'manual' ? '' : ' disabled');
    toggle.dataset.label = open ? 'OPEN' : 'CLOSED';
    card.className = 'actuator-card' + (open ? ' active' : '');
    lbl.textContent = open ? 'OPEN' : 'CLOSED';
  }

  function syncModeUI(mode) {
    const btnAuto = document.getElementById('btnAuto');
    const btnManual = document.getElementById('btnManual');
    const modeTitle = document.getElementById('modeTitle');
    const modeSub = document.getElementById('modeSubtitle');

    btnAuto.className = 'mode-btn' + (mode === 'auto' ? ' active' : '');
    btnManual.className = 'mode-btn' + (mode === 'manual' ? ' active' : '');

    if (mode === 'auto') {
      modeTitle.textContent = 'AUTO MODE';
      modeSub.textContent = 'System managing actuators';
    } else {
      modeTitle.textContent = 'MANUAL MODE';
      modeSub.textContent = 'You control the actuators';
    }

    // Update toggle disabled states
    updatePumpUI(pumpOn);
    updateValveUI(valveOn);
  }

  // ---- Commands ----
  window.setMode = async function(mode) {
    try {
      await set(ref(db, BASE + '/control/mode'), mode);
      addLog(mode === 'auto' ? '⚡ Switched to AUTO mode' : '🎛 Switched to MANUAL mode', mode === 'auto' ? 'green' : 'amber');
      showToast('Mode: ' + mode.toUpperCase(), 'success');
    } catch(e) {
      showToast('Write failed', 'error');
    }
  };

  window.togglePump = async function() {
    if (currentMode !== 'manual') {
      showToast('Switch to MANUAL first', 'error');
      return;
    }
    try {
      const newState = !pumpOn;
      await set(ref(db, BASE + '/control/pumpOn'), newState);
      addLog((newState ? '⚙️ Pump turned ON' : '⚙️ Pump turned OFF'), newState ? 'green' : 'amber');
      showToast('Pump ' + (newState ? 'ON' : 'OFF'), 'success');
    } catch(e) {
      showToast('Write failed', 'error');
    }
  };

  window.toggleValve = async function() {
    if (currentMode !== 'manual') {
      showToast('Switch to MANUAL first', 'error');
      return;
    }
    try {
      const newState = !valveOn;
      await set(ref(db, BASE + '/control/valveOn'), newState);
      addLog((newState ? '🔧 Valve OPENED' : '🔧 Valve CLOSED'), newState ? 'green' : 'amber');
      showToast('Valve ' + (newState ? 'OPEN' : 'CLOSED'), 'success');
    } catch(e) {
      showToast('Write failed', 'error');
    }
  };

  window.emergencyStop = async function() {
    try {
      await set(ref(db, BASE + '/control/mode'), 'manual');
      await set(ref(db, BASE + '/control/pumpOn'), false);
      await set(ref(db, BASE + '/control/valveOn'), false);
      addLog('⛔ EMERGENCY STOP triggered', 'red');
      showToast('EMERGENCY STOP', 'error');
    } catch(e) {
      showToast('Write failed', 'error');
    }
  };

  window.forceRefresh = async function() {
    try {
      const snap = await get(ref(db, BASE));
      showToast('Refreshed', 'success');
    } catch(e) {
      showToast('Refresh failed', 'error');
    }
  };

  // ---- Log ----
  function addLog(msg, type) {
    const now = new Date();
    const time = now.toLocaleTimeString('en-PH', {hour:'2-digit', minute:'2-digit'});
    activityLog.unshift({ msg, type, time });
    if (activityLog.length > 50) activityLog.pop();
    renderLog();
  }

  function renderLog() {
    const list = document.getElementById('logList');
    list.innerHTML = activityLog.slice(0, 20).map(item => `
      <div class="log-item">
        <div class="log-dot ${item.type}"></div>
        <div class="log-msg">${item.msg}</div>
        <div class="log-time">${item.time}</div>
      </div>
    `).join('');
  }

  // ---- Toast ----
  function showToast(msg, type) {
    const t = document.getElementById('toast');
    t.textContent = msg;
    t.className = 'toast show ' + (type || '');
    setTimeout(() => t.className = 'toast', 2200);
  }
  window.showToast = showToast;

  // ---- Page Nav ----
  window.showPage = function(name, el) {
    document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
    document.getElementById('page-' + name).classList.add('active');
    document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
    el.classList.add('active');
  };

</script>
</body>
</html>
