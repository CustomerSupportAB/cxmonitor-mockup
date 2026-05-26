<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CXMonitor — Customer Support Operations</title>
<script src="https://cdn.tailwindcss.com"></script>
<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.1/dist/chart.umd.min.js"></script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg-base: #0a0a0b;
    --bg-surface: #111114;
    --bg-elevated: #18181d;
    --bg-hover: #1f1f25;
    --border-subtle: #1f1f25;
    --border-default: #2a2a32;
    --border-strong: #3a3a45;
    --text-primary: #f5f5f7;
    --text-secondary: #a1a1aa;
    --text-tertiary: #71717a;
    --accent: #6366f1;
    --accent-hover: #818cf8;
    --success: #10b981;
    --warning: #f59e0b;
    --danger: #ef4444;
    --info: #3b82f6;
    --brand-ledisa: #f59e0b;
    --brand-serabel: #8b5cf6;
    --brand-cleantra: #06b6d4;
  }
  * { box-sizing: border-box; }
  html, body {
    margin: 0;
    padding: 0;
    background: var(--bg-base);
    color: var(--text-primary);
    font-family: 'Inter Tight', -apple-system, BlinkMacSystemFont, sans-serif;
    font-feature-settings: "cv02", "cv03", "cv04", "cv11";
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow: hidden;
  }
  .mono { font-family: 'JetBrains Mono', monospace; font-feature-settings: "zero", "ss01"; }
  .app-shell { display: grid; grid-template-columns: 240px 1fr; height: 100vh; }
  .sidebar {
    background: var(--bg-surface);
    border-right: 1px solid var(--border-subtle);
    padding: 16px 12px;
    display: flex;
    flex-direction: column;
    gap: 2px;
    overflow-y: auto;
  }
  .main { overflow-y: auto; background: var(--bg-base); }
  .topbar {
    height: 56px;
    border-bottom: 1px solid var(--border-subtle);
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 24px;
    position: sticky;
    top: 0;
    z-index: 10;
    backdrop-filter: blur(8px);
    background: rgba(10, 10, 11, 0.85);
  }
  .nav-section { font-size: 10.5px; text-transform: uppercase; letter-spacing: 0.08em; color: var(--text-tertiary); padding: 14px 12px 6px; font-weight: 600; }
  .nav-item {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 7px 10px;
    border-radius: 6px;
    font-size: 13.5px;
    color: var(--text-secondary);
    cursor: pointer;
    transition: all 0.12s ease;
    user-select: none;
  }
  .nav-item:hover { background: var(--bg-hover); color: var(--text-primary); }
  .nav-item.active { background: var(--bg-elevated); color: var(--text-primary); font-weight: 500; }
  .nav-item .icon-svg { width: 16px; height: 16px; opacity: 0.85; flex-shrink: 0; }
  .nav-item .nav-badge { margin-left: auto; padding: 1px 6px; font-size: 10.5px; font-weight: 600; }
  .logo {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 4px 8px 16px;
    border-bottom: 1px solid var(--border-subtle);
    margin-bottom: 8px;
  }
  .logo-mark {
    width: 24px;
    height: 24px;
    background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
    border-radius: 6px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 700;
    font-size: 13px;
    color: white;
  }
  .logo-text { font-weight: 600; font-size: 14px; letter-spacing: -0.01em; }
  .content { padding: 24px 32px 48px; max-width: 1400px; margin: 0 auto; }
  .page-header { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 24px; gap: 16px; }
  .page-title { font-size: 22px; font-weight: 600; letter-spacing: -0.02em; margin: 0 0 4px; }
  .page-sub { font-size: 13px; color: var(--text-secondary); margin: 0; }
  .card {
    background: var(--bg-surface);
    border: 1px solid var(--border-subtle);
    border-radius: 10px;
    padding: 16px 18px;
  }
  .card-lg { padding: 20px 22px; }
  .stat-card { display: flex; flex-direction: column; gap: 6px; }
  .stat-label { font-size: 11.5px; color: var(--text-tertiary); font-weight: 500; text-transform: uppercase; letter-spacing: 0.04em; }
  .stat-value { font-size: 26px; font-weight: 600; letter-spacing: -0.02em; line-height: 1; }
  .stat-meta { display: flex; align-items: center; gap: 6px; font-size: 12px; margin-top: 4px; }
  .stat-meta.up { color: var(--success); }
  .stat-meta.down { color: var(--danger); }
  .stat-meta.neutral { color: var(--text-tertiary); }
  .grid { display: grid; gap: 16px; }
  .grid-4 { grid-template-columns: repeat(4, 1fr); }
  .grid-3 { grid-template-columns: repeat(3, 1fr); }
  .grid-2 { grid-template-columns: repeat(2, 1fr); }
  .grid-21 { grid-template-columns: 2fr 1fr; }
  .grid-12 { grid-template-columns: 1fr 2fr; }
  .grid-31 { grid-template-columns: 3fr 1fr; }
  .section-title { font-size: 12.5px; font-weight: 600; color: var(--text-secondary); margin: 0 0 12px; text-transform: uppercase; letter-spacing: 0.04em; }
  .chart-wrap { position: relative; height: 220px; }
  .chart-wrap-tall { position: relative; height: 280px; }
  .chart-wrap-sm { position: relative; height: 100px; }
  .badge {
    display: inline-flex;
    align-items: center;
    gap: 4px;
    padding: 2px 8px;
    border-radius: 4px;
    font-size: 11px;
    font-weight: 500;
    line-height: 1.6;
  }
  .badge-danger { background: rgba(239, 68, 68, 0.12); color: #fca5a5; }
  .badge-warning { background: rgba(245, 158, 11, 0.12); color: #fcd34d; }
  .badge-success { background: rgba(16, 185, 129, 0.12); color: #6ee7b7; }
  .badge-info { background: rgba(59, 130, 246, 0.12); color: #93c5fd; }
  .badge-neutral { background: rgba(161, 161, 170, 0.1); color: #d4d4d8; }
  .brand-ledisa { background: rgba(245, 158, 11, 0.15); color: #fcd34d; }
  .brand-serabel { background: rgba(139, 92, 246, 0.15); color: #c4b5fd; }
  .brand-cleantra { background: rgba(6, 182, 212, 0.15); color: #67e8f9; }
  .dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    display: inline-block;
  }
  .dot-success { background: var(--success); box-shadow: 0 0 0 3px rgba(16, 185, 129, 0.2); }
  .dot-warning { background: var(--warning); }
  .dot-danger { background: var(--danger); box-shadow: 0 0 0 3px rgba(239, 68, 68, 0.2); }
  .pulse {
    animation: pulse 2s ease-in-out infinite;
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.6; transform: scale(0.9); }
  }
  table { width: 100%; border-collapse: collapse; }
  th {
    text-align: left;
    font-size: 11px;
    font-weight: 600;
    color: var(--text-tertiary);
    text-transform: uppercase;
    letter-spacing: 0.04em;
    padding: 10px 12px;
    border-bottom: 1px solid var(--border-subtle);
    background: var(--bg-surface);
    position: sticky;
    top: 0;
  }
  td {
    padding: 12px;
    font-size: 13px;
    border-bottom: 1px solid var(--border-subtle);
    color: var(--text-primary);
  }
  tr:hover td { background: var(--bg-hover); }
  tr.clickable { cursor: pointer; }
  .avatar {
    width: 26px;
    height: 26px;
    border-radius: 50%;
    background: var(--bg-elevated);
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-size: 11px;
    font-weight: 600;
    color: var(--text-primary);
    border: 1px solid var(--border-default);
  }
  .agent-cell { display: flex; align-items: center; gap: 8px; }
  .progress {
    height: 4px;
    background: var(--bg-elevated);
    border-radius: 2px;
    overflow: hidden;
    width: 100%;
  }
  .progress-fill { height: 100%; border-radius: 2px; }
  .progress-fill.success { background: var(--success); }
  .progress-fill.warning { background: var(--warning); }
  .progress-fill.danger { background: var(--danger); }
  .progress-fill.info { background: var(--accent); }
  .btn {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 12px;
    border-radius: 6px;
    font-size: 12.5px;
    font-weight: 500;
    cursor: pointer;
    border: 1px solid var(--border-default);
    background: var(--bg-elevated);
    color: var(--text-primary);
    transition: all 0.12s;
  }
  .btn:hover { background: var(--bg-hover); border-color: var(--border-strong); }
  .btn-primary { background: var(--accent); border-color: var(--accent); color: white; }
  .btn-primary:hover { background: var(--accent-hover); border-color: var(--accent-hover); }
  .btn-ghost { background: transparent; border-color: transparent; color: var(--text-secondary); }
  .btn-ghost:hover { background: var(--bg-hover); color: var(--text-primary); }
  .btn-danger { background: rgba(239, 68, 68, 0.1); border-color: rgba(239, 68, 68, 0.3); color: #fca5a5; }
  .btn-danger:hover { background: rgba(239, 68, 68, 0.15); }
  .filter-bar { display: flex; align-items: center; gap: 8px; flex-wrap: wrap; }
  .pill {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 5px 10px;
    border-radius: 999px;
    font-size: 12px;
    background: var(--bg-elevated);
    border: 1px solid var(--border-default);
    color: var(--text-secondary);
    cursor: pointer;
  }
  .pill.active { background: var(--bg-hover); color: var(--text-primary); border-color: var(--border-strong); }
  .pill:hover { background: var(--bg-hover); color: var(--text-primary); }
  .qa-slider-row {
    display: grid;
    grid-template-columns: 180px 1fr 60px;
    align-items: center;
    gap: 16px;
    padding: 12px 0;
    border-bottom: 1px solid var(--border-subtle);
  }
  .qa-slider-row:last-child { border-bottom: 0; }
  .qa-cat-name { font-size: 13px; font-weight: 500; }
  .qa-cat-weight { font-size: 11px; color: var(--text-tertiary); margin-top: 2px; }
  input[type="range"] {
    -webkit-appearance: none;
    width: 100%;
    height: 4px;
    background: var(--bg-elevated);
    border-radius: 2px;
    outline: none;
  }
  input[type="range"]::-webkit-slider-thumb {
    -webkit-appearance: none;
    width: 16px;
    height: 16px;
    background: var(--accent);
    border-radius: 50%;
    cursor: pointer;
    border: 2px solid var(--bg-base);
  }
  .qa-score-display {
    background: var(--bg-elevated);
    border: 1px solid var(--border-default);
    border-radius: 10px;
    padding: 24px;
    text-align: center;
    margin-top: 20px;
  }
  .qa-total { font-size: 48px; font-weight: 700; letter-spacing: -0.03em; line-height: 1; }
  .qa-total-label { font-size: 12px; color: var(--text-tertiary); margin-top: 8px; text-transform: uppercase; letter-spacing: 0.05em; }
  .checkbox-row {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    padding: 10px 0;
    cursor: pointer;
  }
  .checkbox-row input[type="checkbox"] {
    margin-top: 2px;
    accent-color: var(--danger);
  }
  .checkbox-label { font-size: 13px; color: var(--text-primary); }
  .checkbox-desc { font-size: 11.5px; color: var(--text-tertiary); margin-top: 2px; }
  textarea {
    width: 100%;
    background: var(--bg-base);
    border: 1px solid var(--border-default);
    border-radius: 8px;
    color: var(--text-primary);
    padding: 10px 12px;
    font-family: inherit;
    font-size: 13px;
    resize: vertical;
    min-height: 80px;
  }
  textarea:focus { outline: none; border-color: var(--accent); }
  input[type="search"], input[type="text"], select {
    background: var(--bg-elevated);
    border: 1px solid var(--border-default);
    border-radius: 6px;
    color: var(--text-primary);
    padding: 6px 10px;
    font-family: inherit;
    font-size: 13px;
    outline: none;
  }
  .search-input {
    width: 280px;
    padding-left: 32px;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='14' height='14' viewBox='0 0 24 24' fill='none' stroke='%23a1a1aa' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Ccircle cx='11' cy='11' r='8'/%3E%3Cline x1='21' y1='21' x2='16.65' y2='16.65'/%3E%3C/svg%3E");
    background-repeat: no-repeat;
    background-position: 10px center;
  }
  .ticket-msg {
    border-left: 2px solid var(--border-default);
    padding: 10px 14px;
    margin: 12px 0;
    background: var(--bg-surface);
    border-radius: 0 8px 8px 0;
  }
  .ticket-msg.customer { border-left-color: var(--info); }
  .ticket-msg.agent { border-left-color: var(--success); }
  .ticket-msg.threat { border-left-color: var(--danger); background: rgba(239, 68, 68, 0.04); }
  .msg-header { display: flex; justify-content: space-between; font-size: 12px; color: var(--text-tertiary); margin-bottom: 6px; }
  .msg-body { font-size: 13.5px; color: var(--text-primary); line-height: 1.5; }
  .alert-banner {
    background: rgba(239, 68, 68, 0.08);
    border: 1px solid rgba(239, 68, 68, 0.2);
    border-radius: 10px;
    padding: 14px 16px;
    display: flex;
    align-items: flex-start;
    gap: 12px;
    margin-bottom: 20px;
  }
  .alert-banner.info { background: rgba(99, 102, 241, 0.06); border-color: rgba(99, 102, 241, 0.2); }
  .alert-banner.warning { background: rgba(245, 158, 11, 0.06); border-color: rgba(245, 158, 11, 0.2); }
  .alert-banner.success { background: rgba(16, 185, 129, 0.06); border-color: rgba(16, 185, 129, 0.2); }
  .demo-banner {
    background: linear-gradient(90deg, rgba(99, 102, 241, 0.1), rgba(139, 92, 246, 0.05));
    border-bottom: 1px solid rgba(99, 102, 241, 0.2);
    padding: 8px 24px;
    font-size: 12px;
    color: var(--text-secondary);
    display: flex;
    align-items: center;
    gap: 8px;
    justify-content: center;
  }
  .demo-banner strong { color: var(--text-primary); font-weight: 500; }
  .page { display: none; }
  .page.active { display: block; animation: fadeIn 0.2s ease; }
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(4px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes slideIn {
    from { opacity: 0; transform: translateX(-12px); max-height: 0; padding-top: 0; padding-bottom: 0; margin-bottom: 0; }
    to { opacity: 1; transform: translateX(0); max-height: 80px; }
  }
  .compare-bar { display: flex; align-items: center; gap: 12px; padding: 8px 0; }
  .compare-bar-label { font-size: 12px; color: var(--text-secondary); width: 100px; }
  .compare-bar-track {
    flex: 1;
    height: 22px;
    background: var(--bg-elevated);
    border-radius: 4px;
    position: relative;
    overflow: hidden;
  }
  .compare-bar-fill {
    height: 100%;
    display: flex;
    align-items: center;
    padding: 0 8px;
    font-size: 11px;
    font-weight: 500;
    color: white;
  }
  ::-webkit-scrollbar { width: 8px; height: 8px; }
  ::-webkit-scrollbar-track { background: transparent; }
  ::-webkit-scrollbar-thumb { background: var(--border-default); border-radius: 4px; }
  ::-webkit-scrollbar-thumb:hover { background: var(--border-strong); }
  .activity-feed {
    max-height: 380px;
    overflow-y: auto;
    padding-right: 4px;
  }
  .activity-item {
    display: flex;
    gap: 10px;
    padding: 10px 12px;
    border-radius: 8px;
    margin-bottom: 4px;
    font-size: 12.5px;
    border: 1px solid transparent;
    animation: slideIn 0.4s ease;
    overflow: hidden;
  }
  .activity-item:hover { background: var(--bg-hover); }
  .activity-item.new { background: rgba(99, 102, 241, 0.06); border-color: rgba(99, 102, 241, 0.2); }
  .activity-icon {
    width: 28px;
    height: 28px;
    border-radius: 6px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }
  .activity-icon.danger { background: rgba(239, 68, 68, 0.1); color: #fca5a5; }
  .activity-icon.warning { background: rgba(245, 158, 11, 0.1); color: #fcd34d; }
  .activity-icon.info { background: rgba(59, 130, 246, 0.1); color: #93c5fd; }
  .activity-icon.success { background: rgba(16, 185, 129, 0.1); color: #6ee7b7; }
  .activity-content { flex: 1; min-width: 0; }
  .activity-title { color: var(--text-primary); font-weight: 500; margin-bottom: 2px; }
  .activity-meta { color: var(--text-tertiary); font-size: 11px; }
  .insight-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; margin-bottom: 20px; }
  .insight-card {
    background: var(--bg-surface);
    border: 1px solid var(--border-subtle);
    border-radius: 10px;
    padding: 14px 16px;
    border-left: 3px solid var(--accent);
  }
  .insight-card.warning { border-left-color: var(--warning); }
  .insight-card.danger { border-left-color: var(--danger); }
  .insight-card.success { border-left-color: var(--success); }
  .insight-label { font-size: 11px; color: var(--text-tertiary); text-transform: uppercase; letter-spacing: 0.04em; font-weight: 600; margin-bottom: 6px; }
  .insight-text { font-size: 13.5px; color: var(--text-primary); line-height: 1.4; }
  .insight-text strong { font-weight: 600; }
  .sla-row {
    display: grid;
    grid-template-columns: 100px 1fr 80px 100px;
    align-items: center;
    gap: 12px;
    padding: 10px 12px;
    border-radius: 8px;
    background: var(--bg-elevated);
    margin-bottom: 6px;
    font-size: 13px;
  }
  .sla-row.critical { background: rgba(239, 68, 68, 0.06); border: 1px solid rgba(239, 68, 68, 0.2); }
  .sla-row.warning { background: rgba(245, 158, 11, 0.06); border: 1px solid rgba(245, 158, 11, 0.2); }
  .heatmap-row {
    display: grid;
    grid-template-columns: 100px repeat(7, 1fr);
    gap: 4px;
    margin-bottom: 4px;
    align-items: center;
  }
  .heatmap-cell {
    height: 32px;
    border-radius: 4px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 11px;
    font-weight: 600;
  }
  .empty-state { text-align: center; padding: 40px 20px; color: var(--text-tertiary); font-size: 13px; }
  .health-dot {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-size: 12px;
    color: var(--text-secondary);
  }
  .timestamp-row {
    display: flex;
    align-items: center;
    gap: 16px;
    font-size: 12px;
    color: var(--text-tertiary);
  }
  .icon-svg { width: 14px; height: 14px; stroke: currentColor; stroke-width: 2; fill: none; stroke-linecap: round; stroke-linejoin: round; }
  .tab-bar {
    display: flex;
    gap: 2px;
    border-bottom: 1px solid var(--border-subtle);
    margin-bottom: 20px;
  }
  .tab {
    padding: 8px 14px;
    font-size: 13px;
    color: var(--text-secondary);
    cursor: pointer;
    border-bottom: 2px solid transparent;
    margin-bottom: -1px;
  }
  .tab.active { color: var(--text-primary); border-bottom-color: var(--accent); font-weight: 500; }
  .tab:hover { color: var(--text-primary); }
  .csat-face {
    display: inline-flex;
    width: 36px;
    height: 36px;
    border-radius: 50%;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    margin-right: 6px;
  }
  .agent-profile-header {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 20px;
    background: var(--bg-surface);
    border: 1px solid var(--border-subtle);
    border-radius: 10px;
    margin-bottom: 20px;
  }
  .avatar-lg {
    width: 64px;
    height: 64px;
    border-radius: 50%;
    background: linear-gradient(135deg, #6366f1, #8b5cf6);
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-size: 22px;
    font-weight: 600;
    color: white;
  }
  .coaching-note {
    padding: 12px 14px;
    background: var(--bg-elevated);
    border-radius: 8px;
    margin-bottom: 8px;
    border-left: 3px solid var(--accent);
  }
  .coaching-note .note-meta { font-size: 11px; color: var(--text-tertiary); margin-bottom: 6px; display: flex; justify-content: space-between; }
  .coaching-note .note-body { font-size: 13px; color: var(--text-primary); line-height: 1.5; }
</style>
</head>
<body>

<div class="app-shell">

  <!-- SIDEBAR -->
  <aside class="sidebar">
    <div class="logo">
      <div class="logo-mark">CX</div>
      <div class="logo-text">CXMonitor</div>
    </div>

    <div class="nav-section">Mission control</div>
    <div class="nav-item" data-page="overview">
      <svg class="icon-svg" viewBox="0 0 24 24"><rect x="3" y="3" width="7" height="7"/><rect x="14" y="3" width="7" height="7"/><rect x="3" y="14" width="7" height="7"/><rect x="14" y="14" width="7" height="7"/></svg>
      Overview
    </div>
    <div class="nav-item" data-page="sla">
      <svg class="icon-svg" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
      SLA monitor
      <span class="badge badge-danger nav-badge">7</span>
    </div>
    <div class="nav-item" data-page="risk">
      <svg class="icon-svg" viewBox="0 0 24 24"><path d="M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"/><line x1="12" y1="9" x2="12" y2="13"/><line x1="12" y1="17" x2="12.01" y2="17"/></svg>
      Refund & risk
      <span class="badge badge-warning nav-badge">8</span>
    </div>

    <div class="nav-section">People</div>
    <div class="nav-item" data-page="agents">
      <svg class="icon-svg" viewBox="0 0 24 24"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M22 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
      Agent performance
    </div>
    <div class="nav-item" data-page="compare">
      <svg class="icon-svg" viewBox="0 0 24 24"><line x1="18" y1="20" x2="18" y2="10"/><line x1="12" y1="20" x2="12" y2="4"/><line x1="6" y1="20" x2="6" y2="14"/></svg>
      Brand comparison
    </div>

    <div class="nav-section">Conversations</div>
    <div class="nav-item" data-page="tickets">
      <svg class="icon-svg" viewBox="0 0 24 24"><path d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8v.5z"/></svg>
      Ticket explorer
    </div>

    <div class="nav-section">Quality</div>
    <div class="nav-item active" data-page="qa-queue">
      <svg class="icon-svg" viewBox="0 0 24 24"><polyline points="9 11 12 14 22 4"/><path d="M21 12v7a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11"/></svg>
      QA queue
      <span class="badge badge-danger nav-badge">14</span>
    </div>
    <div class="nav-item" data-page="qa-review">
      <svg class="icon-svg" viewBox="0 0 24 24"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="9" y1="15" x2="15" y2="15"/></svg>
      Score a ticket
    </div>
    <div class="nav-item" data-page="coaching">
      <svg class="icon-svg" viewBox="0 0 24 24"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><polyline points="22 4 12 14.01 9 11.01"/></svg>
      Coaching insights
    </div>
    <div class="nav-item" data-page="reports">
      <svg class="icon-svg" viewBox="0 0 24 24"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
      Reports & exports
    </div>

    <div style="margin-top: auto; padding-top: 16px; border-top: 1px solid var(--border-subtle);">
      <div class="nav-item" style="opacity: 0.9;">
        <div class="avatar" style="width: 24px; height: 24px; font-size: 10px;">AR</div>
        Aileen Reyes
      </div>
    </div>
  </aside>

  <!-- MAIN -->
  <main class="main">
    <div class="demo-banner">
      <svg class="icon-svg" style="width: 12px; height: 12px;" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><line x1="12" y1="16" x2="12" y2="12"/><line x1="12" y1="8" x2="12.01" y2="8"/></svg>
      <strong>Demo mode</strong> · Synthetic data structured against the live database schema · Real data plugs in via read-only Supabase connection
    </div>

    <div class="topbar">
      <div class="filter-bar">
        <div class="pill active" data-filter="all">All brands</div>
        <div class="pill" data-filter="ledisa"><span class="dot" style="background: var(--brand-ledisa);"></span>Ledisa</div>
        <div class="pill" data-filter="serabel"><span class="dot" style="background: var(--brand-serabel);"></span>Serabel</div>
        <div class="pill" data-filter="cleantra"><span class="dot" style="background: var(--brand-cleantra);"></span>Cleantra</div>
        <div style="width: 1px; height: 20px; background: var(--border-default); margin: 0 4px;"></div>
        <select id="date-range">
          <option value="7">Last 7 days</option>
          <option value="30" selected>Last 30 days</option>
          <option value="90">Last 90 days</option>
        </select>
      </div>
      <div class="timestamp-row">
        <span class="health-dot"><span class="dot dot-success pulse"></span>Live · Streaming events</span>
        <span id="last-updated">Last sync 4m ago</span>
        <button class="btn btn-ghost" onclick="manualRefresh()">
          <svg class="icon-svg" viewBox="0 0 24 24"><polyline points="23 4 23 10 17 10"/><polyline points="1 20 1 14 7 14"/><path d="M3.51 9a9 9 0 0 1 14.85-3.36L23 10M1 14l4.64 4.36A9 9 0 0 0 20.49 15"/></svg>
          Refresh
        </button>
      </div>
    </div>

    <!-- ============= QA QUEUE PAGE (default landing) ============= -->
    <div class="content page active" data-page="qa-queue">
      <div class="page-header">
        <div>
          <h1 class="page-title">QA review queue</h1>
          <p class="page-sub">14 conversations surfaced for review · Prioritized by AI threat classifier + agent risk signals + sampling logic</p>
        </div>
        <div style="display: flex; gap: 8px;">
          <button class="btn">Filter</button>
          <button class="btn btn-primary">Bulk export</button>
        </div>
      </div>

      <div class="grid grid-4" style="margin-bottom: 20px;">
        <div class="card stat-card" style="border-color: rgba(239, 68, 68, 0.3);">
          <span class="stat-label">Critical priority</span>
          <span class="stat-value" style="color: #fca5a5;">4</span>
          <span class="stat-meta down">Threats + escalations</span>
        </div>
        <div class="card stat-card" style="border-color: rgba(245, 158, 11, 0.3);">
          <span class="stat-label">High priority</span>
          <span class="stat-value" style="color: #fcd34d;">3</span>
          <span class="stat-meta neutral">Risk signals</span>
        </div>
        <div class="card stat-card">
          <span class="stat-label">Sample reviews</span>
          <span class="stat-value">7</span>
          <span class="stat-meta neutral">Weekly coverage</span>
        </div>
        <div class="card stat-card">
          <span class="stat-label">Reviewed this week</span>
          <span class="stat-value">23</span>
          <span class="stat-meta up">+5 vs last week</span>
        </div>
      </div>

      <div class="alert-banner info">
        <svg class="icon-svg" style="color: var(--accent); flex-shrink: 0; margin-top: 2px;" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><line x1="12" y1="16" x2="12" y2="12"/><line x1="12" y1="8" x2="12.01" y2="8"/></svg>
        <div>
          <div style="font-weight: 500; font-size: 13.5px; margin-bottom: 2px;">How this queue is built</div>
          <div style="font-size: 12.5px; color: var(--text-secondary);">Tickets are surfaced when the AI threat classifier flags them (BBB, chargeback, legal), refund/dispute keywords appear in customer messages, an agent's response time exceeds 2× their baseline, or random sampling ensures every agent gets reviewed weekly.</div>
        </div>
      </div>

      <div class="card">
        <table>
          <thead>
            <tr>
              <th>Priority</th>
              <th>Conv #</th>
              <th>Customer</th>
              <th>Brand</th>
              <th>Agent</th>
              <th>Why flagged</th>
              <th style="text-align: right;">Action</th>
            </tr>
          </thead>
          <tbody id="qaQueueBody"></tbody>
        </table>
      </div>
    </div>

    <!-- ============= OVERVIEW PAGE ============= -->
    <div class="content page" data-page="overview">
      <div class="page-header">
        <div>
          <h1 class="page-title">Operations overview</h1>
          <p class="page-sub">How healthy is our customer support operation right now?</p>
        </div>
        <button class="btn btn-primary">
          <svg class="icon-svg" viewBox="0 0 24 24"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
          Export report
        </button>
      </div>

      <!-- SMART INSIGHTS -->
      <div class="insight-grid">
        <div class="insight-card danger">
          <div class="insight-label">Risk alert</div>
          <div class="insight-text"><strong>3 BBB threats</strong> flagged in the last 24h. 2 on Cleantra, 1 on Ledisa.</div>
        </div>
        <div class="insight-card warning">
          <div class="insight-label">Trend</div>
          <div class="insight-text">Refund requests <strong>up 18%</strong> this week. Mostly subscription rebill confusion.</div>
        </div>
        <div class="insight-card success">
          <div class="insight-label">Improvement</div>
          <div class="insight-text">Avg first response <strong>improved 11min</strong> across all brands week-over-week.</div>
        </div>
      </div>

      <!-- STATS -->
      <div class="grid grid-4" style="margin-bottom: 20px;">
        <div class="card stat-card">
          <span class="stat-label">Open tickets</span>
          <span class="stat-value">147</span>
          <span class="stat-meta down"><svg class="icon-svg" viewBox="0 0 24 24"><polyline points="23 18 13.5 8.5 8.5 13.5 1 6"/><polyline points="17 18 23 18 23 12"/></svg>18% vs last week</span>
        </div>
        <div class="card stat-card">
          <span class="stat-label">Avg first response</span>
          <span class="stat-value">42<span style="font-size: 18px; color: var(--text-tertiary);">m</span></span>
          <span class="stat-meta up"><svg class="icon-svg" viewBox="0 0 24 24"><polyline points="23 6 13.5 15.5 8.5 10.5 1 18"/><polyline points="17 6 23 6 23 12"/></svg>11m faster</span>
        </div>
        <div class="card stat-card">
          <span class="stat-label">CSAT score</span>
          <span class="stat-value">4.2<span style="font-size: 18px; color: var(--text-tertiary);">/5</span></span>
          <span class="stat-meta up">+0.3 this month</span>
        </div>
        <div class="card stat-card" style="border-color: rgba(239, 68, 68, 0.3);">
          <span class="stat-label">Threat-flagged</span>
          <span class="stat-value" style="color: #fca5a5;">8</span>
          <span class="stat-meta down">3 chargeback · 4 BBB · 1 lawsuit</span>
        </div>
      </div>

      <div class="grid grid-4" style="margin-bottom: 20px;">
        <div class="card stat-card">
          <span class="stat-label">Solved today</span>
          <span class="stat-value">94</span>
          <span class="stat-meta neutral">7 by 4 PM</span>
        </div>
        <div class="card stat-card">
          <span class="stat-label">SLA breaches</span>
          <span class="stat-value" style="color: #fcd34d;">7</span>
          <span class="stat-meta down">3 critical</span>
        </div>
        <div class="card stat-card">
          <span class="stat-label">Refunds (7d)</span>
          <span class="stat-value">23</span>
          <span class="stat-meta neutral">$1,847 total</span>
        </div>
        <div class="card stat-card">
          <span class="stat-label">Active agents</span>
          <span class="stat-value">7<span style="font-size: 18px; color: var(--text-tertiary);">/8</span></span>
          <span class="stat-meta neutral"><span class="dot dot-success"></span>1 away</span>
        </div>
      </div>

      <!-- CHARTS + ACTIVITY FEED -->
      <div class="grid grid-21" style="margin-bottom: 20px;">
        <div class="card card-lg">
          <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 16px;">
            <h3 class="section-title" style="margin: 0;">Ticket volume by brand</h3>
            <div style="display: flex; gap: 12px; font-size: 11px;">
              <span style="color: var(--text-secondary);"><span class="dot" style="background: var(--brand-ledisa); margin-right: 6px;"></span>Ledisa</span>
              <span style="color: var(--text-secondary);"><span class="dot" style="background: var(--brand-serabel); margin-right: 6px;"></span>Serabel</span>
              <span style="color: var(--text-secondary);"><span class="dot" style="background: var(--brand-cleantra); margin-right: 6px;"></span>Cleantra</span>
            </div>
          </div>
          <div class="chart-wrap-tall"><canvas id="volumeChart" role="img" aria-label="Stacked bar chart of daily ticket volume by brand"></canvas></div>
        </div>

        <div class="card card-lg">
          <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 12px;">
            <h3 class="section-title" style="margin: 0;">Live activity</h3>
            <span class="health-dot"><span class="dot dot-success pulse"></span>Live</span>
          </div>
          <div class="activity-feed" id="activityFeed"></div>
        </div>
      </div>

      <div class="grid grid-2" style="margin-bottom: 20px;">
        <div class="card card-lg">
          <h3 class="section-title">First response time trend</h3>
          <div class="chart-wrap"><canvas id="responseChart" role="img" aria-label="Line chart of average first response time over time"></canvas></div>
        </div>
        <div class="card card-lg">
          <h3 class="section-title">CSAT trend</h3>
          <div class="chart-wrap"><canvas id="csatChart" role="img" aria-label="Line chart of CSAT score over time"></canvas></div>
        </div>
      </div>

      <div class="card card-lg">
        <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 16px;">
          <h3 class="section-title" style="margin: 0;">Today's top performing agents</h3>
          <button class="btn btn-ghost" onclick="showPage('agents')">View all →</button>
        </div>
        <table>
          <thead>
            <tr>
              <th>Agent</th>
              <th>Brand</th>
              <th style="text-align: right;">Solved</th>
              <th style="text-align: right;">First response</th>
              <th style="text-align: right;">CSAT</th>
              <th style="text-align: right;">Status</th>
            </tr>
          </thead>
          <tbody id="topAgentsBody"></tbody>
        </table>
      </div>
    </div>

    <!-- ============= SLA MONITOR PAGE ============= -->
    <div class="content page" data-page="sla">
      <div class="page-header">
        <div>
          <h1 class="page-title">SLA monitor</h1>
          <p class="page-sub">Overdue and at-risk tickets · Live queue health by agent and brand</p>
        </div>
      </div>

      <div class="alert-banner">
        <svg class="icon-svg" style="color: var(--danger); flex-shrink: 0; margin-top: 2px;" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
        <div>
          <div style="font-weight: 500; font-size: 13.5px; margin-bottom: 2px;">7 tickets currently in breach</div>
          <div style="font-size: 12.5px; color: var(--text-secondary);">3 critical (over 24h with no response), 4 at-risk (approaching SLA window). 5 are on Cleantra.</div>
        </div>
        <button class="btn btn-danger">Assign immediately</button>
      </div>

      <div class="grid grid-4" style="margin-bottom: 20px;">
        <div class="card stat-card" style="border-color: rgba(239, 68, 68, 0.3);">
          <span class="stat-label">In breach</span>
          <span class="stat-value" style="color: #fca5a5;">3</span>
          <span class="stat-meta down">>24h no response</span>
        </div>
        <div class="card stat-card" style="border-color: rgba(245, 158, 11, 0.3);">
          <span class="stat-label">At risk</span>
          <span class="stat-value" style="color: #fcd34d;">4</span>
          <span class="stat-meta neutral">>4h, <24h</span>
        </div>
        <div class="card stat-card">
          <span class="stat-label">On track</span>
          <span class="stat-value">133</span>
          <span class="stat-meta up">94% of queue</span>
        </div>
        <div class="card stat-card">
          <span class="stat-label">Avg time to first reply</span>
          <span class="stat-value">42<span style="font-size: 18px; color: var(--text-tertiary);">m</span></span>
          <span class="stat-meta neutral">SLA: 60m</span>
        </div>
      </div>

      <div class="card card-lg" style="margin-bottom: 20px;">
        <h3 class="section-title">Tickets currently in breach</h3>
        <div id="slaBreachList"></div>
      </div>

      <div class="grid grid-2">
        <div class="card card-lg">
          <h3 class="section-title">Response time by brand (7-day avg)</h3>
          <div class="compare-bar">
            <div class="compare-bar-label">Ledisa</div>
            <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 38%; background: var(--brand-ledisa);">38m · within SLA</div></div>
          </div>
          <div class="compare-bar">
            <div class="compare-bar-label">Serabel</div>
            <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 47%; background: var(--brand-serabel);">47m · within SLA</div></div>
          </div>
          <div class="compare-bar">
            <div class="compare-bar-label">Cleantra</div>
            <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 75%; background: var(--danger);">58m · near SLA</div></div>
          </div>
        </div>
        <div class="card card-lg">
          <h3 class="section-title">Queue depth by agent</h3>
          <div id="queueDepth"></div>
        </div>
      </div>
    </div>

    <!-- ============= REFUND & RISK PAGE ============= -->
    <div class="content page" data-page="risk">
      <div class="page-header">
        <div>
          <h1 class="page-title">Refund & dispute risk</h1>
          <p class="page-sub">Monitor refund trends, dispute language, and emerging risk patterns across brands</p>
        </div>
        <button class="btn">Export risk report</button>
      </div>

      <div class="grid grid-4" style="margin-bottom: 20px;">
        <div class="card stat-card">
          <span class="stat-label">Refunds (30d)</span>
          <span class="stat-value">87</span>
          <span class="stat-meta down">+18% vs prev</span>
        </div>
        <div class="card stat-card">
          <span class="stat-label">Refund $$ (30d)</span>
          <span class="stat-value">$7,243</span>
          <span class="stat-meta down">+22%</span>
        </div>
        <div class="card stat-card" style="border-color: rgba(239, 68, 68, 0.3);">
          <span class="stat-label">BBB threats</span>
          <span class="stat-value" style="color: #fca5a5;">4</span>
          <span class="stat-meta down">2 active</span>
        </div>
        <div class="card stat-card" style="border-color: rgba(239, 68, 68, 0.3);">
          <span class="stat-label">Chargeback mentions</span>
          <span class="stat-value" style="color: #fca5a5;">3</span>
          <span class="stat-meta down">All Cleantra</span>
        </div>
      </div>

      <div class="grid grid-2" style="margin-bottom: 20px;">
        <div class="card card-lg">
          <h3 class="section-title">Refund volume trend</h3>
          <div class="chart-wrap-tall"><canvas id="refundChart" role="img" aria-label="Line chart of daily refunds with reason breakdown"></canvas></div>
        </div>
        <div class="card card-lg">
          <h3 class="section-title">Refund reasons (30d)</h3>
          <div class="chart-wrap-tall"><canvas id="refundReasonChart" role="img" aria-label="Horizontal bar chart of refund reason breakdown"></canvas></div>
        </div>
      </div>

      <div class="card card-lg" style="margin-bottom: 20px;">
        <h3 class="section-title">Dispute language detected (last 7 days)</h3>
        <table>
          <thead><tr><th>Phrase pattern</th><th style="text-align: right;">Mentions</th><th style="text-align: right;">Brand</th><th style="text-align: right;">Risk level</th></tr></thead>
          <tbody>
            <tr><td>"file with BBB" / "Better Business Bureau"</td><td style="text-align: right;" class="mono">4</td><td style="text-align: right;">Mixed</td><td style="text-align: right;"><span class="badge badge-danger">Critical</span></td></tr>
            <tr><td>"dispute with credit card" / "chargeback"</td><td style="text-align: right;" class="mono">3</td><td style="text-align: right;">Cleantra</td><td style="text-align: right;"><span class="badge badge-danger">Critical</span></td></tr>
            <tr><td>"I never subscribed" / "unauthorized"</td><td style="text-align: right;" class="mono">12</td><td style="text-align: right;">Ledisa</td><td style="text-align: right;"><span class="badge badge-warning">High</span></td></tr>
            <tr><td>"never received" / "package lost"</td><td style="text-align: right;" class="mono">8</td><td style="text-align: right;">Mixed</td><td style="text-align: right;"><span class="badge badge-warning">High</span></td></tr>
            <tr><td>"allergic reaction" / "made me sick"</td><td style="text-align: right;" class="mono">3</td><td style="text-align: right;">Cleantra</td><td style="text-align: right;"><span class="badge badge-danger">Critical</span></td></tr>
            <tr><td>"lawyer" / "legal action"</td><td style="text-align: right;" class="mono">1</td><td style="text-align: right;">Cleantra</td><td style="text-align: right;"><span class="badge badge-danger">Critical</span></td></tr>
          </tbody>
        </table>
      </div>

      <div class="card card-lg">
        <h3 class="section-title">Top products driving refunds</h3>
        <div class="compare-bar">
          <div class="compare-bar-label">Cleantra Pro Bundle</div>
          <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 82%; background: var(--danger);">22 refunds · $1,876</div></div>
        </div>
        <div class="compare-bar">
          <div class="compare-bar-label">Ledisa Subscription</div>
          <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 60%; background: var(--brand-ledisa);">16 refunds · $1,247</div></div>
        </div>
        <div class="compare-bar">
          <div class="compare-bar-label">Cleantra Starter Kit</div>
          <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 48%; background: var(--brand-cleantra);">13 refunds · $872</div></div>
        </div>
        <div class="compare-bar">
          <div class="compare-bar-label">Serabel Premium</div>
          <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 35%; background: var(--brand-serabel);">9 refunds · $612</div></div>
        </div>
      </div>
    </div>

    <!-- ============= AGENT PERFORMANCE PAGE ============= -->
    <div class="content page" data-page="agents">
      <div class="page-header">
        <div>
          <h1 class="page-title">Agent performance</h1>
          <p class="page-sub">Ranked by composite performance score · Click an agent for detailed profile</p>
        </div>
        <div style="display: flex; gap: 8px;">
          <input type="search" placeholder="Search agents..." class="search-input">
          <button class="btn">Export CSV</button>
        </div>
      </div>

      <div class="grid grid-4" style="margin-bottom: 20px;">
        <div class="card stat-card"><span class="stat-label">Active agents</span><span class="stat-value">8</span><span class="stat-meta neutral">7 online now</span></div>
        <div class="card stat-card"><span class="stat-label">Tickets/agent/day</span><span class="stat-value">18.4</span><span class="stat-meta up">+2.1 vs last week</span></div>
        <div class="card stat-card"><span class="stat-label">Avg QA score</span><span class="stat-value">76</span><span class="stat-meta neutral">team median</span></div>
        <div class="card stat-card"><span class="stat-label">Avg reopen rate</span><span class="stat-value">7.2<span style="font-size: 18px; color: var(--text-tertiary);">%</span></span><span class="stat-meta down">+1.3pp</span></div>
      </div>

      <div class="card">
        <table>
          <thead>
            <tr>
              <th>Agent</th>
              <th>Brand</th>
              <th style="text-align: right;">Solved (30d)</th>
              <th style="text-align: right;">1st response</th>
              <th style="text-align: right;">Handling</th>
              <th style="text-align: right;">Reopen</th>
              <th style="text-align: right;">CSAT</th>
              <th style="text-align: right;">QA score</th>
            </tr>
          </thead>
          <tbody id="agentsTableBody"></tbody>
        </table>
      </div>
    </div>

    <!-- ============= AGENT PROFILE PAGE ============= -->
    <div class="content page" data-page="agent-profile">
      <div class="page-header">
        <div>
          <button class="btn btn-ghost" onclick="showPage('agents')" style="margin-bottom: 8px;">← Back to all agents</button>
          <h1 class="page-title">Agent profile</h1>
        </div>
        <div style="display: flex; gap: 8px;">
          <button class="btn">Schedule 1:1</button>
          <button class="btn btn-primary">Add coaching note</button>
        </div>
      </div>

      <div class="agent-profile-header">
        <div class="avatar-lg" id="profile-avatar">MT</div>
        <div style="flex: 1;">
          <h2 style="margin: 0 0 4px; font-size: 20px; font-weight: 600;" id="profile-name">María Tavarez</h2>
          <div style="font-size: 13px; color: var(--text-secondary);" id="profile-meta">Ledisa · Senior Agent · Online now</div>
        </div>
        <div style="display: flex; gap: 20px; text-align: right;">
          <div><div style="font-size: 11px; color: var(--text-tertiary); text-transform: uppercase;">Tenure</div><div style="font-size: 16px; font-weight: 600;">14 months</div></div>
          <div><div style="font-size: 11px; color: var(--text-tertiary); text-transform: uppercase;">Lifetime tickets</div><div style="font-size: 16px; font-weight: 600;">2,847</div></div>
          <div><div style="font-size: 11px; color: var(--text-tertiary); text-transform: uppercase;">Composite rank</div><div style="font-size: 16px; font-weight: 600; color: var(--success);">#1 of 8</div></div>
        </div>
      </div>

      <div class="grid grid-4" style="margin-bottom: 20px;">
        <div class="card stat-card"><span class="stat-label">Solved (30d)</span><span class="stat-value">184</span><span class="stat-meta up">+12%</span></div>
        <div class="card stat-card"><span class="stat-label">First response</span><span class="stat-value">32<span style="font-size: 16px; color: var(--text-tertiary);">m</span></span><span class="stat-meta up">-8m</span></div>
        <div class="card stat-card"><span class="stat-label">QA score</span><span class="stat-value" style="color: var(--success);">88</span><span class="stat-meta up">+4pts</span></div>
        <div class="card stat-card"><span class="stat-label">CSAT</span><span class="stat-value">4.7<span style="font-size: 16px; color: var(--text-tertiary);">/5</span></span><span class="stat-meta up">+0.2</span></div>
      </div>

      <div class="grid grid-2" style="margin-bottom: 20px;">
        <div class="card card-lg">
          <h3 class="section-title">90-day performance trend</h3>
          <div class="chart-wrap"><canvas id="agentTrendChart" role="img" aria-label="Multi-line chart of agent performance over 90 days"></canvas></div>
        </div>
        <div class="card card-lg">
          <h3 class="section-title">QA category breakdown</h3>
          <div class="chart-wrap"><canvas id="agentQAChart" role="img" aria-label="Radar chart of agent QA scores by category"></canvas></div>
        </div>
      </div>

      <div class="grid grid-2">
        <div class="card card-lg">
          <h3 class="section-title">Strengths & weaknesses</h3>
          <div style="margin-bottom: 14px;">
            <div style="font-size: 12px; color: var(--success); margin-bottom: 4px; font-weight: 500;">STRENGTHS</div>
            <div style="font-size: 13px; line-height: 1.6;">
              · Tone & empathy consistently 90+<br>
              · Subscription explanations clear<br>
              · Fast response on Ledisa brand
            </div>
          </div>
          <div>
            <div style="font-size: 12px; color: var(--warning); margin-bottom: 4px; font-weight: 500;">DEVELOPMENT AREAS</div>
            <div style="font-size: 13px; line-height: 1.6;">
              · Escalation recognition (missed BBB cue 1x)<br>
              · Refund timing communication
            </div>
          </div>
        </div>

        <div class="card card-lg">
          <h3 class="section-title">Recent coaching notes</h3>
          <div class="coaching-note">
            <div class="note-meta"><span>QA review · Conv #4827</span><span>2 days ago</span></div>
            <div class="note-body">Missed BBB escalation cue on Sandra K. ticket. Coaching focus: recognizing dispute language as immediate-action trigger.</div>
          </div>
          <div class="coaching-note" style="border-left-color: var(--success);">
            <div class="note-meta"><span>QA review · Conv #4801</span><span>1 week ago</span></div>
            <div class="note-body">Excellent recovery on subscription confusion ticket. Used 30% retention offer correctly per SOP. Example to share with team.</div>
          </div>
          <div class="coaching-note">
            <div class="note-meta"><span>1:1 notes</span><span>2 weeks ago</span></div>
            <div class="note-body">Discussed handling time on Ledisa brand. María agreed to use saved replies for top 5 FAQs to reduce time per ticket.</div>
          </div>
        </div>
      </div>
    </div>

    <!-- ============= TICKET EXPLORER PAGE ============= -->
    <div class="content page" data-page="tickets">
      <div class="page-header">
        <div>
          <h1 class="page-title">Ticket explorer</h1>
          <p class="page-sub">Search and filter conversations across all brands</p>
        </div>
        <input type="search" placeholder="Search by email, order #, or keyword..." class="search-input" style="width: 360px;">
      </div>

      <div class="filter-bar" style="margin-bottom: 16px;">
        <div class="pill active">All</div>
        <div class="pill">Open</div>
        <div class="pill">Need to reply</div>
        <div class="pill">Has refund</div>
        <div class="pill" style="border-color: rgba(239, 68, 68, 0.3); color: #fca5a5;">Threat-flagged</div>
        <div class="pill">Closed</div>
      </div>

      <div class="card">
        <table>
          <thead>
            <tr>
              <th>Conv #</th>
              <th>Customer</th>
              <th>Subject</th>
              <th>Brand</th>
              <th>Agent</th>
              <th>State</th>
              <th>Flags</th>
              <th style="text-align: right;">Last msg</th>
            </tr>
          </thead>
          <tbody id="ticketsTableBody"></tbody>
        </table>
      </div>
    </div>

    <!-- ============= BRAND COMPARISON PAGE ============= -->
    <div class="content page" data-page="compare">
      <div class="page-header">
        <div>
          <h1 class="page-title">Brand comparison</h1>
          <p class="page-sub">Side-by-side performance · Last 30 days</p>
        </div>
        <button class="btn">Export comparison</button>
      </div>

      <div class="grid grid-3" style="margin-bottom: 20px;">
        <div class="card card-lg" style="border-top: 3px solid var(--brand-ledisa);">
          <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 12px;">
            <h3 style="margin: 0; font-size: 15px; font-weight: 600;">Ledisa</h3>
            <span class="badge brand-ledisa">Best performer</span>
          </div>
          <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 12px;">
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Tickets</div><div style="font-size: 18px; font-weight: 600;">1,247</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Response</div><div style="font-size: 18px; font-weight: 600;">38m</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">CSAT</div><div style="font-size: 18px; font-weight: 600;">4.4</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Refund rate</div><div style="font-size: 18px; font-weight: 600;">2.1%</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">QA avg</div><div style="font-size: 18px; font-weight: 600;">82</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Disputes</div><div style="font-size: 18px; font-weight: 600;">3</div></div>
          </div>
        </div>
        <div class="card card-lg" style="border-top: 3px solid var(--brand-serabel);">
          <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 12px;">
            <h3 style="margin: 0; font-size: 15px; font-weight: 600;">Serabel</h3>
            <span class="badge badge-neutral">Stable</span>
          </div>
          <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 12px;">
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Tickets</div><div style="font-size: 18px; font-weight: 600;">982</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Response</div><div style="font-size: 18px; font-weight: 600;">47m</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">CSAT</div><div style="font-size: 18px; font-weight: 600;">4.1</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Refund rate</div><div style="font-size: 18px; font-weight: 600;">3.4%</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">QA avg</div><div style="font-size: 18px; font-weight: 600;">76</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Disputes</div><div style="font-size: 18px; font-weight: 600;">5</div></div>
          </div>
        </div>
        <div class="card card-lg" style="border-top: 3px solid var(--brand-cleantra);">
          <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 12px;">
            <h3 style="margin: 0; font-size: 15px; font-weight: 600;">Cleantra</h3>
            <span class="badge badge-danger">Needs attention</span>
          </div>
          <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 12px;">
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Tickets</div><div style="font-size: 18px; font-weight: 600;">1,103</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Response</div><div style="font-size: 18px; font-weight: 600;">58m</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">CSAT</div><div style="font-size: 18px; font-weight: 600; color: #fcd34d;">3.7</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Refund rate</div><div style="font-size: 18px; font-weight: 600; color: #fca5a5;">5.8%</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">QA avg</div><div style="font-size: 18px; font-weight: 600; color: #fcd34d;">68</div></div>
            <div><div style="font-size: 11px; color: var(--text-tertiary);">Disputes</div><div style="font-size: 18px; font-weight: 600; color: #fca5a5;">11</div></div>
          </div>
        </div>
      </div>

      <div class="card card-lg" style="margin-bottom: 20px;">
        <h3 class="section-title">Refund rate by brand</h3>
        <div class="compare-bar">
          <div class="compare-bar-label">Ledisa</div>
          <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 21%; background: var(--brand-ledisa);">2.1%</div></div>
        </div>
        <div class="compare-bar">
          <div class="compare-bar-label">Serabel</div>
          <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 34%; background: var(--brand-serabel);">3.4%</div></div>
        </div>
        <div class="compare-bar">
          <div class="compare-bar-label">Cleantra</div>
          <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 58%; background: var(--brand-cleantra);">5.8%</div></div>
        </div>
      </div>

      <div class="card card-lg">
        <h3 class="section-title">CSAT by brand</h3>
        <div class="compare-bar">
          <div class="compare-bar-label">Ledisa</div>
          <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 88%; background: var(--brand-ledisa);">4.4 / 5</div></div>
        </div>
        <div class="compare-bar">
          <div class="compare-bar-label">Serabel</div>
          <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 82%; background: var(--brand-serabel);">4.1 / 5</div></div>
        </div>
        <div class="compare-bar">
          <div class="compare-bar-label">Cleantra</div>
          <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 74%; background: var(--brand-cleantra);">3.7 / 5</div></div>
        </div>
      </div>
    </div>

    <!-- ============= QA SCORING PAGE ============= -->
    <div class="content page" data-page="qa-review">
      <div class="page-header">
        <div>
          <button class="btn btn-ghost" onclick="showPage('qa-queue')" style="margin-bottom: 8px;">← Back to queue</button>
          <h1 class="page-title">Score conversation</h1>
          <p class="page-sub">Conv #4827 · Ledisa · Agent: María Tavarez · BBB threat flagged</p>
        </div>
      </div>

      <div class="grid grid-12" style="gap: 20px;">
        <div class="card card-lg" style="height: fit-content; position: sticky; top: 80px;">
          <h3 class="section-title">Conversation</h3>
          <div style="background: var(--bg-elevated); border-radius: 8px; padding: 12px; margin-bottom: 16px; font-size: 12px;">
            <div style="display: flex; justify-content: space-between; margin-bottom: 6px;"><span style="color: var(--text-tertiary);">Subject</span><span>Order #LDS-58234</span></div>
            <div style="display: flex; justify-content: space-between; margin-bottom: 6px;"><span style="color: var(--text-tertiary);">Customer</span><span>sandra.k****@gmail.com</span></div>
            <div style="display: flex; justify-content: space-between; margin-bottom: 6px;"><span style="color: var(--text-tertiary);">Order value</span><span>$87.40</span></div>
            <div style="display: flex; justify-content: space-between;"><span style="color: var(--text-tertiary);">Threat flag</span><span class="badge badge-danger">BBB · high</span></div>
          </div>
          <div class="ticket-msg customer">
            <div class="msg-header"><span>Customer · 3 days ago</span></div>
            <div class="msg-body">It's been 8 days since I requested the refund. This is unacceptable. I want this resolved today or I will file with the BBB.</div>
          </div>
          <div class="ticket-msg agent">
            <div class="msg-header"><span>María Tavarez · 2 days ago</span></div>
            <div class="msg-body">Hi Sandra, sorry for the delay! Our refund processing usually takes 5-7 business days. Let me check on this for you.</div>
          </div>
          <div class="ticket-msg threat">
            <div class="msg-header"><span>Customer · 1 day ago</span><span class="badge badge-danger">BBB mention</span></div>
            <div class="msg-body">It's been over 10 days now. I'm filing the BBB complaint today. I want my $87.40 back immediately.</div>
          </div>
        </div>

        <div>
          <div class="card card-lg" style="margin-bottom: 16px;">
            <h3 class="section-title">QA scorecard</h3>
            <div class="qa-slider-row">
              <div><div class="qa-cat-name">SOP compliance</div><div class="qa-cat-weight">Weight: 40%</div></div>
              <input type="range" min="0" max="100" value="65" oninput="updateScore()" id="sop">
              <div style="font-size: 16px; font-weight: 600; text-align: right;" id="sop-val">65</div>
            </div>
            <div class="qa-slider-row">
              <div><div class="qa-cat-name">Tone & empathy</div><div class="qa-cat-weight">Weight: 20%</div></div>
              <input type="range" min="0" max="100" value="78" oninput="updateScore()" id="tone">
              <div style="font-size: 16px; font-weight: 600; text-align: right;" id="tone-val">78</div>
            </div>
            <div class="qa-slider-row">
              <div><div class="qa-cat-name">Resolution quality</div><div class="qa-cat-weight">Weight: 25%</div></div>
              <input type="range" min="0" max="100" value="45" oninput="updateScore()" id="resolution">
              <div style="font-size: 16px; font-weight: 600; text-align: right;" id="resolution-val">45</div>
            </div>
            <div class="qa-slider-row">
              <div><div class="qa-cat-name">Compliance & risk</div><div class="qa-cat-weight">Weight: 15%</div></div>
              <input type="range" min="0" max="100" value="40" oninput="updateScore()" id="compliance">
              <div style="font-size: 16px; font-weight: 600; text-align: right;" id="compliance-val">40</div>
            </div>
            <div class="qa-score-display">
              <div class="qa-total" id="total-score">58</div>
              <div class="qa-total-label">Weighted total · Below team avg (76)</div>
            </div>
          </div>

          <div class="card card-lg" style="margin-bottom: 16px;">
            <h3 class="section-title">Critical issue flags</h3>
            <label class="checkbox-row"><input type="checkbox" checked><div><div class="checkbox-label">Escalation handling failure</div><div class="checkbox-desc">Agent did not escalate after BBB threat was mentioned</div></div></label>
            <label class="checkbox-row"><input type="checkbox" checked><div><div class="checkbox-label">BBB / dispute risk</div><div class="checkbox-desc">Customer explicitly threatened BBB filing</div></div></label>
            <label class="checkbox-row"><input type="checkbox"><div><div class="checkbox-label">Refund policy inconsistency</div><div class="checkbox-desc">Stated timing different from policy</div></div></label>
            <label class="checkbox-row"><input type="checkbox"><div><div class="checkbox-label">Subscription explanation unclear</div><div class="checkbox-desc">Rebill or subscription terms miscommunicated</div></div></label>
            <label class="checkbox-row"><input type="checkbox"><div><div class="checkbox-label">Allergy / reaction handling</div><div class="checkbox-desc">Failed to follow safety protocol</div></div></label>
          </div>

          <div class="card card-lg">
            <h3 class="section-title">Coaching notes</h3>
            <textarea>María was friendly but missed the urgency. Two days between replies on a BBB-threatened ticket is too slow. She also gave a generic "5-7 business days" response instead of checking the actual refund status. Coaching focus: recognizing escalation language ("file with BBB", "chargeback") as immediate-action triggers.</textarea>
            <div style="display: flex; gap: 8px; margin-top: 16px;">
              <button class="btn" disabled style="opacity: 0.5; cursor: not-allowed;" title="Available when CXMonitor database is set up">Save review (Phase 2)</button>
              <button class="btn btn-primary" onclick="alert('In the real version, this exports the scorecard as formatted text to paste into a Google Doc or send to the agent.')">Copy to clipboard</button>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- ============= COACHING INSIGHTS PAGE ============= -->
    <div class="content page" data-page="coaching">
      <div class="page-header">
        <div>
          <h1 class="page-title">Coaching insights</h1>
          <p class="page-sub">Aggregate QA patterns · Identify the biggest training opportunities across the team</p>
        </div>
      </div>

      <div class="grid grid-4" style="margin-bottom: 20px;">
        <div class="card stat-card"><span class="stat-label">QA reviews (30d)</span><span class="stat-value">87</span><span class="stat-meta up">+23%</span></div>
        <div class="card stat-card"><span class="stat-label">Team avg QA</span><span class="stat-value">76</span><span class="stat-meta up">+4 vs last month</span></div>
        <div class="card stat-card" style="border-color: rgba(245, 158, 11, 0.3);"><span class="stat-label">Critical flags</span><span class="stat-value" style="color: #fcd34d;">14</span><span class="stat-meta down">+3</span></div>
        <div class="card stat-card"><span class="stat-label">Coaching sessions</span><span class="stat-value">12</span><span class="stat-meta neutral">scheduled</span></div>
      </div>

      <div class="grid grid-2" style="margin-bottom: 20px;">
        <div class="card card-lg">
          <h3 class="section-title">Most common critical flags</h3>
          <div class="compare-bar">
            <div class="compare-bar-label" style="width: 180px;">Escalation handling</div>
            <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 78%; background: var(--danger);">11 cases</div></div>
          </div>
          <div class="compare-bar">
            <div class="compare-bar-label" style="width: 180px;">Subscription unclear</div>
            <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 60%; background: var(--warning);">8 cases</div></div>
          </div>
          <div class="compare-bar">
            <div class="compare-bar-label" style="width: 180px;">Refund policy inconsistency</div>
            <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 50%; background: var(--warning);">7 cases</div></div>
          </div>
          <div class="compare-bar">
            <div class="compare-bar-label" style="width: 180px;">BBB / dispute risk</div>
            <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 35%; background: var(--warning);">5 cases</div></div>
          </div>
          <div class="compare-bar">
            <div class="compare-bar-label" style="width: 180px;">Allergy / reaction</div>
            <div class="compare-bar-track"><div class="compare-bar-fill" style="width: 14%; background: var(--accent);">2 cases</div></div>
          </div>
        </div>

        <div class="card card-lg">
          <h3 class="section-title">Weakest QA categories (team)</h3>
          <div class="chart-wrap"><canvas id="weakCatChart" role="img" aria-label="Bar chart of weakest QA categories across team"></canvas></div>
        </div>
      </div>

      <div class="card card-lg" style="margin-bottom: 20px;">
        <h3 class="section-title">Training opportunities — generated from QA patterns</h3>
        <div style="display: flex; flex-direction: column; gap: 10px;">
          <div style="padding: 14px 16px; background: var(--bg-elevated); border-radius: 8px; border-left: 3px solid var(--danger);">
            <div style="font-weight: 500; font-size: 13.5px; margin-bottom: 4px;">Recommended team training: Escalation recognition</div>
            <div style="font-size: 12.5px; color: var(--text-secondary);">11 critical flags this month involved missed BBB/dispute/chargeback language. Impact: 4 of 8 agents. Suggested format: 30-min team workshop with real examples.</div>
          </div>
          <div style="padding: 14px 16px; background: var(--bg-elevated); border-radius: 8px; border-left: 3px solid var(--warning);">
            <div style="font-weight: 500; font-size: 13.5px; margin-bottom: 4px;">1:1 focus area: Fernando Núñez & Elena García</div>
            <div style="font-size: 12.5px; color: var(--text-secondary);">Both flagged 4+ times for resolution quality on Cleantra. Shared pattern: not verifying refund processing status before responding to customer.</div>
          </div>
          <div style="padding: 14px 16px; background: var(--bg-elevated); border-radius: 8px; border-left: 3px solid var(--accent);">
            <div style="font-weight: 500; font-size: 13.5px; margin-bottom: 4px;">Process update: Subscription explanation script</div>
            <div style="font-size: 12.5px; color: var(--text-secondary);">8 subscription-confusion flags suggest the current saved-reply template is unclear. Consider updating with explicit rebill timing language.</div>
          </div>
        </div>
      </div>

      <div class="card card-lg">
        <h3 class="section-title">QA score trend by category (90 days)</h3>
        <div class="chart-wrap-tall"><canvas id="qaCatTrendChart" role="img" aria-label="Multi-line chart of QA scores by category over 90 days"></canvas></div>
      </div>
    </div>

    <!-- ============= REPORTS PAGE ============= -->
    <div class="content page" data-page="reports">
      <div class="page-header">
        <div>
          <h1 class="page-title">Reports & exports</h1>
          <p class="page-sub">Generate CSV reports for any date range and brand combination</p>
        </div>
      </div>
      <div class="grid grid-2">
        <div class="card card-lg"><h3 style="margin: 0 0 4px; font-size: 15px;">Agent performance report</h3><p style="margin: 0 0 16px; font-size: 12.5px; color: var(--text-secondary);">Tickets solved, response times, reopen rates, QA scores per agent.</p><button class="btn btn-primary">Generate CSV</button></div>
        <div class="card card-lg"><h3 style="margin: 0 0 4px; font-size: 15px;">Refund trend report</h3><p style="margin: 0 0 16px; font-size: 12.5px; color: var(--text-secondary);">All refunds with reason classification, agent, and brand breakdown.</p><button class="btn btn-primary">Generate CSV</button></div>
        <div class="card card-lg"><h3 style="margin: 0 0 4px; font-size: 15px;">Threat & dispute report</h3><p style="margin: 0 0 16px; font-size: 12.5px; color: var(--text-secondary);">All BBB, chargeback, and legal-threat flagged conversations.</p><button class="btn btn-primary">Generate CSV</button></div>
        <div class="card card-lg"><h3 style="margin: 0 0 4px; font-size: 15px;">QA & coaching report</h3><p style="margin: 0 0 16px; font-size: 12.5px; color: var(--text-secondary);">QA scores, critical flags, and coaching notes per agent.</p><button class="btn btn-primary">Generate CSV</button></div>
      </div>
    </div>

  </main>
</div>

<script>
// ============= DATA =============
const AGENTS = [
  { initials: 'MT', name: 'María Tavarez', brand: 'Ledisa', solved: 184, response: 32, handling: 9.2, reopen: 4.1, escalations: 2, qa: 88, csat: 4.7, status: 'online' },
  { initials: 'JR', name: 'Joselin Rodríguez', brand: 'Ledisa', solved: 171, response: 38, handling: 10.5, reopen: 5.8, escalations: 3, qa: 84, csat: 4.5, status: 'online' },
  { initials: 'CP', name: 'Carlos Peña', brand: 'Serabel', solved: 162, response: 41, handling: 11.1, reopen: 6.2, escalations: 4, qa: 81, csat: 4.3, status: 'online' },
  { initials: 'AS', name: 'Andrea Suárez', brand: 'Serabel', solved: 158, response: 44, handling: 11.8, reopen: 6.9, escalations: 3, qa: 79, csat: 4.2, status: 'online' },
  { initials: 'RD', name: 'Roberto Díaz', brand: 'Serabel', solved: 145, response: 47, handling: 12.4, reopen: 7.4, escalations: 5, qa: 76, csat: 4.1, status: 'online' },
  { initials: 'LM', name: 'Lucía Martínez', brand: 'Cleantra', solved: 152, response: 51, handling: 13.2, reopen: 8.1, escalations: 6, qa: 74, csat: 3.9, status: 'online' },
  { initials: 'FN', name: 'Fernando Núñez', brand: 'Cleantra', solved: 139, response: 58, handling: 14.5, reopen: 9.2, escalations: 8, qa: 68, csat: 3.7, status: 'away' },
  { initials: 'EG', name: 'Elena García', brand: 'Cleantra', solved: 128, response: 64, handling: 15.8, reopen: 11.3, escalations: 11, qa: 61, csat: 3.5, status: 'offline' },
];

const TICKETS = [
  { no: 4827, customer: 'sandra.k****@gmail.com', subject: 'Refund still not received — filing BBB', brand: 'Ledisa', agent: 'MT', state: 'need_to_reply', flags: ['BBB', 'refund'], last: '1d ago' },
  { no: 4826, customer: 'mike.t****@yahoo.com', subject: 'Cancelled order still charged', brand: 'Cleantra', agent: 'EG', state: 'need_to_reply', flags: ['chargeback'], last: '2h ago' },
  { no: 4825, customer: 'amanda.r****@hotmail.com', subject: 'Subscription confusion — auto-renewed', brand: 'Ledisa', agent: 'JR', state: 'waiting_customer', flags: ['subscription'], last: '4h ago' },
  { no: 4824, customer: 'thomas.b****@gmail.com', subject: 'Wrong product received', brand: 'Serabel', agent: 'AS', state: 'need_to_reply', flags: [], last: '6h ago' },
  { no: 4823, customer: 'jennifer.l****@outlook.com', subject: 'Allergic reaction — need urgent help', brand: 'Cleantra', agent: 'LM', state: 'need_to_reply', flags: ['allergy', 'priority'], last: '1h ago' },
  { no: 4822, customer: 'david.h****@gmail.com', subject: 'Will dispute with credit card company', brand: 'Cleantra', agent: 'FN', state: 'need_to_reply', flags: ['chargeback'], last: '3h ago' },
  { no: 4821, customer: 'rebecca.s****@yahoo.com', subject: 'Order tracking shows delivered, not received', brand: 'Serabel', agent: 'CP', state: 'waiting_customer', flags: [], last: '8h ago' },
  { no: 4820, customer: 'kevin.w****@gmail.com', subject: 'Cancel my subscription immediately', brand: 'Ledisa', agent: 'MT', state: 'closed', flags: ['subscription'], last: '1d ago' },
  { no: 4819, customer: 'patricia.m****@gmail.com', subject: 'Defective product — second one this month', brand: 'Cleantra', agent: 'EG', state: 'need_to_reply', flags: ['quality'], last: '5h ago' },
  { no: 4818, customer: 'james.b****@hotmail.com', subject: 'Refund processed wrong amount', brand: 'Ledisa', agent: 'JR', state: 'waiting_customer', flags: ['refund'], last: '12h ago' },
];

const QA_QUEUE = [
  { priority: 'critical', conv: 4827, customer: 'sandra.k****@gmail.com', brand: 'Ledisa', agent: 'MT', reason: 'BBB threat · slow agent response (48h)' },
  { priority: 'critical', conv: 4826, customer: 'mike.t****@yahoo.com', brand: 'Cleantra', agent: 'EG', reason: 'Chargeback mention · classifier confidence: high' },
  { priority: 'critical', conv: 4823, customer: 'jennifer.l****@outlook.com', brand: 'Cleantra', agent: 'LM', reason: 'Allergy complaint · escalation protocol' },
  { priority: 'critical', conv: 4822, customer: 'david.h****@gmail.com', brand: 'Cleantra', agent: 'FN', reason: 'Dispute language · credit card threat' },
  { priority: 'high', conv: 4825, customer: 'amanda.r****@hotmail.com', brand: 'Ledisa', agent: 'JR', reason: 'Subscription confusion · auto-rebill complaint' },
  { priority: 'high', conv: 4819, customer: 'patricia.m****@gmail.com', brand: 'Cleantra', agent: 'EG', reason: 'Repeat defective product · same customer' },
  { priority: 'high', conv: 4818, customer: 'james.b****@hotmail.com', brand: 'Ledisa', agent: 'JR', reason: 'Refund amount mismatch · accounting risk' },
  { priority: 'normal', conv: 4815, customer: 'laura.k****@gmail.com', brand: 'Serabel', agent: 'CP', reason: 'Random weekly sample · agent coverage' },
  { priority: 'normal', conv: 4812, customer: 'brian.t****@gmail.com', brand: 'Serabel', agent: 'AS', reason: 'Random weekly sample · agent coverage' },
  { priority: 'normal', conv: 4810, customer: 'nicole.r****@yahoo.com', brand: 'Ledisa', agent: 'MT', reason: 'Random weekly sample · agent coverage' },
  { priority: 'normal', conv: 4807, customer: 'gregory.h****@gmail.com', brand: 'Cleantra', agent: 'LM', reason: 'Random weekly sample · agent coverage' },
  { priority: 'normal', conv: 4805, customer: 'stephanie.b****@outlook.com', brand: 'Serabel', agent: 'RD', reason: 'Random weekly sample · agent coverage' },
  { priority: 'normal', conv: 4803, customer: 'andrew.l****@gmail.com', brand: 'Cleantra', agent: 'FN', reason: 'Response time dip · 2.4× agent baseline' },
  { priority: 'normal', conv: 4800, customer: 'michelle.s****@gmail.com', brand: 'Ledisa', agent: 'JR', reason: 'Long thread (12 messages) · resolution quality' },
];

const SLA_BREACHES = [
  { severity: 'critical', conv: 4823, customer: 'jennifer.l****', agent: 'LM', brand: 'Cleantra', overdue: '4h 22m past SLA', context: 'Allergy complaint · unanswered' },
  { severity: 'critical', conv: 4826, customer: 'mike.t****', agent: 'EG', brand: 'Cleantra', overdue: '2h 14m past SLA', context: 'Chargeback threat · unassigned' },
  { severity: 'critical', conv: 4822, customer: 'david.h****', agent: 'FN', brand: 'Cleantra', overdue: '1h 48m past SLA', context: 'Dispute language detected' },
  { severity: 'warning', conv: 4819, customer: 'patricia.m****', agent: 'EG', brand: 'Cleantra', overdue: '38m left', context: 'Repeat defective product complaint' },
  { severity: 'warning', conv: 4824, customer: 'thomas.b****', agent: 'AS', brand: 'Serabel', overdue: '52m left', context: 'Wrong product · awaiting reply' },
  { severity: 'warning', conv: 4830, customer: 'lisa.h****', agent: 'CP', brand: 'Serabel', overdue: '1h 12m left', context: 'Shipping delay inquiry' },
  { severity: 'warning', conv: 4831, customer: 'mark.j****', agent: 'JR', brand: 'Ledisa', overdue: '1h 47m left', context: 'Subscription update request' },
];

const ACTIVITY_TEMPLATES = [
  { type: 'danger', icon: 'M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z', title: 'BBB threat detected', meta: 'Conv #__CONV__ · __BRAND__ · Customer mentioned filing complaint' },
  { type: 'danger', icon: 'M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z', title: 'Chargeback language flagged', meta: 'Conv #__CONV__ · __BRAND__ · "dispute with credit card"' },
  { type: 'warning', icon: 'M12 8v4M12 16h.01 M21 12a9 9 0 11-18 0 9 9 0 0118 0z', title: 'SLA at risk', meta: 'Conv #__CONV__ · __BRAND__ · 30 min to first response deadline' },
  { type: 'warning', icon: 'M21 15v4a2 2 0 01-2 2H5a2 2 0 01-2-2v-4 M17 8l-5-5-5 5 M12 3v12', title: 'Refund requested', meta: 'Conv #__CONV__ · __BRAND__ · $__AMT__ on subscription order' },
  { type: 'info', icon: 'M21 11.5a8.38 8.38 0 01-.9 3.8 8.5 8.5 0 01-7.6 4.7 8.38 8.38 0 01-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 01-.9-3.8 8.5 8.5 0 014.7-7.6 8.38 8.38 0 013.8-.9h.5a8.48 8.48 0 018 8v.5z', title: 'New ticket received', meta: 'Conv #__CONV__ · __BRAND__ · Auto-assigned to __AGENT__' },
  { type: 'success', icon: 'M22 11.08V12a10 10 0 11-5.93-9.14 M22 4L12 14.01l-3-3', title: 'Ticket resolved', meta: 'Conv #__CONV__ · __BRAND__ · Closed by __AGENT__ · CSAT 5/5' },
  { type: 'success', icon: 'M22 11.08V12a10 10 0 11-5.93-9.14 M22 4L12 14.01l-3-3', title: 'Refund processed', meta: 'Conv #__CONV__ · __BRAND__ · $__AMT__ confirmed' },
  { type: 'info', icon: 'M16 21v-2a4 4 0 00-4-4H6a4 4 0 00-4 4v2 M12 7a4 4 0 110 8 4 4 0 010-8z', title: 'Agent went online', meta: '__AGENT_FULL__ started shift · __BRAND__' },
  { type: 'warning', icon: 'M12 8v4M12 16h.01 M21 12a9 9 0 11-18 0 9 9 0 0118 0z', title: 'Subscription confusion flag', meta: 'Conv #__CONV__ · __BRAND__ · Customer asking about unexpected rebill' },
  { type: 'danger', icon: 'M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z', title: 'Allergic reaction reported', meta: 'Conv #__CONV__ · __BRAND__ · Urgent escalation triggered' },
];

// ============= NAVIGATION =============
function showPage(pageId) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
  document.querySelector(`.page[data-page="${pageId}"]`).classList.add('active');
  const navEl = document.querySelector(`.nav-item[data-page="${pageId}"]`);
  if (navEl) navEl.classList.add('active');
  document.querySelector('.main').scrollTop = 0;
  if (pageId === 'overview') startActivityFeed();
}

document.querySelectorAll('.nav-item[data-page]').forEach(item => {
  item.addEventListener('click', () => showPage(item.dataset.page));
});

document.querySelectorAll('.pill[data-filter]').forEach(pill => {
  pill.addEventListener('click', () => {
    document.querySelectorAll('.pill[data-filter]').forEach(p => p.classList.remove('active'));
    pill.classList.add('active');
  });
});

function manualRefresh() {
  document.getElementById('last-updated').textContent = 'Last sync just now';
  setTimeout(() => { document.getElementById('last-updated').textContent = 'Last sync 1m ago'; }, 60000);
}

// ============= QA SCORING =============
function updateScore() {
  const sop = parseInt(document.getElementById('sop').value);
  const tone = parseInt(document.getElementById('tone').value);
  const resolution = parseInt(document.getElementById('resolution').value);
  const compliance = parseInt(document.getElementById('compliance').value);
  document.getElementById('sop-val').textContent = sop;
  document.getElementById('tone-val').textContent = tone;
  document.getElementById('resolution-val').textContent = resolution;
  document.getElementById('compliance-val').textContent = compliance;
  const total = Math.round(sop * 0.4 + tone * 0.2 + resolution * 0.25 + compliance * 0.15);
  document.getElementById('total-score').textContent = total;
  const totalEl = document.getElementById('total-score');
  if (total >= 85) totalEl.style.color = 'var(--success)';
  else if (total >= 70) totalEl.style.color = 'var(--text-primary)';
  else if (total >= 55) totalEl.style.color = 'var(--warning)';
  else totalEl.style.color = 'var(--danger)';
}

// ============= RENDERING =============
function brandBadge(brand) {
  return `<span class="badge brand-${brand.toLowerCase()}">${brand}</span>`;
}
function statusDot(status) {
  if (status === 'online') return '<span class="dot dot-success"></span>';
  if (status === 'away') return '<span class="dot dot-warning"></span>';
  return '<span class="dot" style="background: var(--text-tertiary);"></span>';
}

function renderTopAgents() {
  const top = [...AGENTS].sort((a, b) => b.qa - a.qa).slice(0, 5);
  document.getElementById('topAgentsBody').innerHTML = top.map(a => `
    <tr class="clickable" onclick="openAgentProfile('${a.initials}')">
      <td><div class="agent-cell"><div class="avatar">${a.initials}</div>${a.name}</div></td>
      <td>${brandBadge(a.brand)}</td>
      <td style="text-align: right;" class="mono">${a.solved}</td>
      <td style="text-align: right;" class="mono">${a.response}m</td>
      <td style="text-align: right;" class="mono">${a.csat}</td>
      <td style="text-align: right;">${statusDot(a.status)} ${a.status}</td>
    </tr>`).join('');
}

function renderAgentsTable() {
  document.getElementById('agentsTableBody').innerHTML = AGENTS.map(a => {
    const qaColor = a.qa >= 80 ? 'var(--success)' : a.qa >= 70 ? 'var(--text-primary)' : a.qa >= 60 ? 'var(--warning)' : 'var(--danger)';
    return `
      <tr class="clickable" onclick="openAgentProfile('${a.initials}')">
        <td><div class="agent-cell"><div class="avatar">${a.initials}</div>${a.name}${statusDot(a.status)}</div></td>
        <td>${brandBadge(a.brand)}</td>
        <td style="text-align: right;" class="mono">${a.solved}</td>
        <td style="text-align: right;" class="mono">${a.response}m</td>
        <td style="text-align: right;" class="mono">${a.handling}m</td>
        <td style="text-align: right;" class="mono">${a.reopen}%</td>
        <td style="text-align: right;" class="mono">${a.csat}</td>
        <td style="text-align: right;"><span class="mono" style="color: ${qaColor}; font-weight: 600;">${a.qa}</span></td>
      </tr>`;
  }).join('');
}

function openAgentProfile(initials) {
  const a = AGENTS.find(x => x.initials === initials);
  if (!a) return;
  document.getElementById('profile-avatar').textContent = a.initials;
  document.getElementById('profile-name').textContent = a.name;
  document.getElementById('profile-meta').textContent = `${a.brand} · ${a.status === 'online' ? 'Online now' : a.status}`;
  showPage('agent-profile');
  setTimeout(renderAgentCharts, 100);
}

function renderTickets() {
  document.getElementById('ticketsTableBody').innerHTML = TICKETS.map(t => {
    const stateCls = t.state === 'need_to_reply' ? 'badge-danger' : t.state === 'waiting_customer' ? 'badge-warning' : 'badge-neutral';
    const stateText = t.state.replace(/_/g, ' ');
    const flagsHtml = t.flags.map(f => {
      const cls = ['BBB', 'chargeback', 'allergy', 'priority'].includes(f) ? 'badge-danger' : 'badge-warning';
      return `<span class="badge ${cls}">${f}</span>`;
    }).join(' ');
    return `
      <tr class="clickable" onclick="showPage('qa-review')">
        <td class="mono" style="color: var(--text-tertiary);">#${t.no}</td>
        <td style="font-size: 12.5px;">${t.customer}</td>
        <td style="max-width: 240px; overflow: hidden; text-overflow: ellipsis; white-space: nowrap;">${t.subject}</td>
        <td>${brandBadge(t.brand)}</td>
        <td><div class="avatar" style="width: 22px; height: 22px; font-size: 9.5px;">${t.agent}</div></td>
        <td><span class="badge ${stateCls}">${stateText}</span></td>
        <td>${flagsHtml || '<span style="color: var(--text-tertiary); font-size: 12px;">—</span>'}</td>
        <td style="text-align: right; color: var(--text-tertiary); font-size: 12px;">${t.last}</td>
      </tr>`;
  }).join('');
}

function renderQAQueue() {
  document.getElementById('qaQueueBody').innerHTML = QA_QUEUE.map(q => {
    const pCls = q.priority === 'critical' ? 'badge-danger' : q.priority === 'high' ? 'badge-warning' : 'badge-neutral';
    return `
      <tr class="clickable">
        <td><span class="badge ${pCls}">${q.priority}</span></td>
        <td class="mono" style="color: var(--text-tertiary);">#${q.conv}</td>
        <td style="font-size: 12.5px;">${q.customer}</td>
        <td>${brandBadge(q.brand)}</td>
        <td><div class="avatar" style="width: 22px; height: 22px; font-size: 9.5px;">${q.agent}</div></td>
        <td style="font-size: 12.5px; color: var(--text-secondary);">${q.reason}</td>
        <td style="text-align: right;"><button class="btn btn-primary" onclick="event.stopPropagation(); showPage('qa-review');">Review</button></td>
      </tr>`;
  }).join('');
}

function renderSLABreaches() {
  document.getElementById('slaBreachList').innerHTML = SLA_BREACHES.map(s => {
    const cls = s.severity === 'critical' ? 'critical' : 'warning';
    const timeColor = s.severity === 'critical' ? '#fca5a5' : '#fcd34d';
    return `
      <div class="sla-row ${cls}">
        <span class="mono" style="color: var(--text-tertiary);">#${s.conv}</span>
        <span><strong>${s.customer}</strong> · ${s.context}</span>
        <span>${brandBadge(s.brand)} <div class="avatar" style="width: 20px; height: 20px; font-size: 9px;">${s.agent}</div></span>
        <span style="color: ${timeColor}; font-weight: 500; text-align: right; font-size: 12px;">${s.overdue}</span>
      </div>`;
  }).join('');

  document.getElementById('queueDepth').innerHTML = AGENTS.slice(0, 6).map(a => {
    const depth = Math.round(8 + Math.random() * 18);
    const cls = depth > 20 ? 'danger' : depth > 14 ? 'warning' : 'success';
    return `
      <div style="display: grid; grid-template-columns: 140px 1fr 40px; align-items: center; gap: 12px; padding: 6px 0;">
        <div class="agent-cell"><div class="avatar" style="width: 22px; height: 22px; font-size: 9.5px;">${a.initials}</div>${a.name.split(' ')[0]}</div>
        <div class="progress"><div class="progress-fill ${cls}" style="width: ${(depth/25*100)}%;"></div></div>
        <span class="mono" style="text-align: right; font-size: 12px;">${depth}</span>
      </div>`;
  }).join('');
}

// ============= LIVE ACTIVITY FEED =============
function generateActivity() {
  const tpl = ACTIVITY_TEMPLATES[Math.floor(Math.random() * ACTIVITY_TEMPLATES.length)];
  const brands = ['Ledisa', 'Serabel', 'Cleantra'];
  const brand = brands[Math.floor(Math.random() * 3)];
  const agent = AGENTS[Math.floor(Math.random() * AGENTS.length)];
  const conv = 4832 + Math.floor(Math.random() * 50);
  const amt = (Math.floor(Math.random() * 200) + 30) + '.' + String(Math.floor(Math.random() * 99)).padStart(2, '0');
  const meta = tpl.meta
    .replace('__CONV__', conv)
    .replace('__BRAND__', brand)
    .replace('__AGENT__', agent.initials)
    .replace('__AGENT_FULL__', agent.name)
    .replace('__AMT__', amt);

  return { type: tpl.type, icon: tpl.icon, title: tpl.title, meta };
}

function pushActivity(initial = false) {
  const feed = document.getElementById('activityFeed');
  if (!feed) return;
  const a = generateActivity();
  const item = document.createElement('div');
  item.className = 'activity-item' + (initial ? '' : ' new');
  item.innerHTML = `
    <div class="activity-icon ${a.type}">
      <svg class="icon-svg" viewBox="0 0 24 24"><path d="${a.icon}"/></svg>
    </div>
    <div class="activity-content">
      <div class="activity-title">${a.title}</div>
      <div class="activity-meta">${a.meta} · just now</div>
    </div>`;
  feed.insertBefore(item, feed.firstChild);
  while (feed.children.length > 12) feed.removeChild(feed.lastChild);
  setTimeout(() => item.classList.remove('new'), 3000);
}

let activityInterval = null;
function startActivityFeed() {
  const feed = document.getElementById('activityFeed');
  if (!feed) return;
  if (feed.children.length === 0) {
    for (let i = 0; i < 8; i++) pushActivity(true);
  }
  if (activityInterval) clearInterval(activityInterval);
  activityInterval = setInterval(() => pushActivity(false), 4500);
}

// ============= CHARTS =============
Chart.defaults.color = '#a1a1aa';
Chart.defaults.borderColor = '#1f1f25';
Chart.defaults.font.family = "'Inter Tight', sans-serif";
Chart.defaults.font.size = 11;

function makeLabels(days) {
  const labels = [];
  const now = new Date();
  for (let i = days - 1; i >= 0; i--) {
    const d = new Date(now);
    d.setDate(d.getDate() - i);
    labels.push(d.toLocaleDateString('en-US', { month: 'short', day: 'numeric' }));
  }
  return labels;
}

function seedRandom(seed) {
  let s = seed;
  return () => { s = (s * 9301 + 49297) % 233280; return s / 233280; };
}

let chartsRendered = false;
function renderCharts() {
  if (chartsRendered) return;
  chartsRendered = true;
  const days = 30;
  const labels = makeLabels(days);
  const rnd = seedRandom(42);

  new Chart(document.getElementById('volumeChart'), {
    type: 'bar',
    data: {
      labels,
      datasets: [
        { label: 'Ledisa', data: labels.map(() => Math.round(28 + rnd() * 18)), backgroundColor: '#f59e0b', borderRadius: 3 },
        { label: 'Serabel', data: labels.map(() => Math.round(22 + rnd() * 14)), backgroundColor: '#8b5cf6', borderRadius: 3 },
        { label: 'Cleantra', data: labels.map(() => Math.round(25 + rnd() * 16)), backgroundColor: '#06b6d4', borderRadius: 3 },
      ]
    },
    options: {
      responsive: true, maintainAspectRatio: false,
      plugins: { legend: { display: false } },
      scales: { x: { stacked: true, grid: { display: false }, ticks: { maxRotation: 0, autoSkipPadding: 20 } }, y: { stacked: true, grid: { color: '#1f1f25' }, beginAtZero: true } }
    }
  });

  const rnd2 = seedRandom(7);
  new Chart(document.getElementById('responseChart'), {
    type: 'line',
    data: {
      labels,
      datasets: [{ label: 'Response time (min)', data: labels.map((_, i) => Math.round(70 - i * 0.8 + rnd2() * 12)), borderColor: '#6366f1', backgroundColor: 'rgba(99, 102, 241, 0.08)', fill: true, tension: 0.35, borderWidth: 2, pointRadius: 0 }]
    },
    options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { x: { grid: { display: false }, ticks: { maxRotation: 0, autoSkipPadding: 30 } }, y: { grid: { color: '#1f1f25' }, beginAtZero: true } } }
  });

  const rnd3 = seedRandom(99);
  new Chart(document.getElementById('csatChart'), {
    type: 'line',
    data: {
      labels,
      datasets: [{ label: 'CSAT', data: labels.map((_, i) => (3.7 + i * 0.015 + rnd3() * 0.3).toFixed(2)), borderColor: '#10b981', backgroundColor: 'rgba(16, 185, 129, 0.08)', fill: true, tension: 0.35, borderWidth: 2, pointRadius: 0 }]
    },
    options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { x: { grid: { display: false }, ticks: { maxRotation: 0, autoSkipPadding: 30 } }, y: { grid: { color: '#1f1f25' }, min: 3, max: 5 } } }
  });

  // Risk page charts
  const rnd4 = seedRandom(13);
  new Chart(document.getElementById('refundChart'), {
    type: 'line',
    data: {
      labels,
      datasets: [{ label: 'Daily refunds', data: labels.map(() => Math.round(3 + rnd4() * 8)), borderColor: '#ef4444', backgroundColor: 'rgba(239, 68, 68, 0.08)', fill: true, tension: 0.35, borderWidth: 2, pointRadius: 0 }]
    },
    options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { x: { grid: { display: false }, ticks: { maxRotation: 0, autoSkipPadding: 30 } }, y: { grid: { color: '#1f1f25' }, beginAtZero: true } } }
  });

  new Chart(document.getElementById('refundReasonChart'), {
    type: 'bar',
    data: {
      labels: ['Subscription rebill confusion', 'Product defect', 'Never received', 'Wrong product', 'Allergic reaction', 'Late delivery'],
      datasets: [{ data: [28, 19, 14, 12, 8, 6], backgroundColor: ['#ef4444', '#f59e0b', '#6366f1', '#8b5cf6', '#ef4444', '#06b6d4'], borderRadius: 3 }]
    },
    options: { indexAxis: 'y', responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { x: { grid: { color: '#1f1f25' }, beginAtZero: true }, y: { grid: { display: false } } } }
  });

  // Coaching page charts
  new Chart(document.getElementById('weakCatChart'), {
    type: 'bar',
    data: {
      labels: ['SOP', 'Tone', 'Resolution', 'Compliance'],
      datasets: [{ label: 'Team avg', data: [76, 84, 68, 72], backgroundColor: ['#6366f1', '#10b981', '#ef4444', '#f59e0b'], borderRadius: 4 }]
    },
    options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { x: { grid: { display: false } }, y: { grid: { color: '#1f1f25' }, beginAtZero: true, max: 100 } } }
  });

  const days90 = makeLabels(90);
  const rnd5 = seedRandom(33);
  new Chart(document.getElementById('qaCatTrendChart'), {
    type: 'line',
    data: {
      labels: days90,
      datasets: [
        { label: 'SOP', data: days90.map((_, i) => Math.round(70 + i * 0.08 + rnd5() * 8)), borderColor: '#6366f1', borderWidth: 2, pointRadius: 0, tension: 0.4 },
        { label: 'Tone', data: days90.map((_, i) => Math.round(82 + rnd5() * 6)), borderColor: '#10b981', borderWidth: 2, pointRadius: 0, tension: 0.4 },
        { label: 'Resolution', data: days90.map((_, i) => Math.round(64 + i * 0.05 + rnd5() * 9)), borderColor: '#ef4444', borderWidth: 2, pointRadius: 0, tension: 0.4 },
        { label: 'Compliance', data: days90.map((_, i) => Math.round(70 + i * 0.04 + rnd5() * 8)), borderColor: '#f59e0b', borderWidth: 2, pointRadius: 0, tension: 0.4 },
      ]
    },
    options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: true, position: 'top', labels: { boxWidth: 10, boxHeight: 10, padding: 12, font: { size: 11 } } } }, scales: { x: { grid: { display: false }, ticks: { maxRotation: 0, autoSkipPadding: 40 } }, y: { grid: { color: '#1f1f25' }, min: 50, max: 100 } } }
  });
}

let agentChartsRendered = false;
function renderAgentCharts() {
  if (agentChartsRendered) return;
  agentChartsRendered = true;

  const labels = makeLabels(90);
  const rnd = seedRandom(5);
  new Chart(document.getElementById('agentTrendChart'), {
    type: 'line',
    data: {
      labels,
      datasets: [
        { label: 'Solved/day', data: labels.map((_, i) => Math.round(4 + i * 0.04 + rnd() * 3)), borderColor: '#6366f1', backgroundColor: 'rgba(99, 102, 241, 0.05)', borderWidth: 2, pointRadius: 0, tension: 0.4, yAxisID: 'y' },
        { label: 'QA score', data: labels.map((_, i) => Math.round(80 + i * 0.08 + rnd() * 6)), borderColor: '#10b981', borderWidth: 2, pointRadius: 0, tension: 0.4, yAxisID: 'y1' }
      ]
    },
    options: {
      responsive: true, maintainAspectRatio: false,
      plugins: { legend: { display: true, position: 'top', labels: { boxWidth: 10, boxHeight: 10, padding: 12, font: { size: 11 } } } },
      scales: {
        x: { grid: { display: false }, ticks: { maxRotation: 0, autoSkipPadding: 50 } },
        y: { type: 'linear', position: 'left', grid: { color: '#1f1f25' }, beginAtZero: true },
        y1: { type: 'linear', position: 'right', grid: { display: false }, min: 60, max: 100 }
      }
    }
  });

  new Chart(document.getElementById('agentQAChart'), {
    type: 'radar',
    data: {
      labels: ['SOP', 'Tone', 'Resolution', 'Compliance', 'Speed', 'Recovery'],
      datasets: [{ label: 'María', data: [86, 94, 82, 88, 91, 85], borderColor: '#6366f1', backgroundColor: 'rgba(99, 102, 241, 0.15)', borderWidth: 2, pointRadius: 3 }]
    },
    options: {
      responsive: true, maintainAspectRatio: false,
      plugins: { legend: { display: false } },
      scales: { r: { angleLines: { color: '#1f1f25' }, grid: { color: '#1f1f25' }, pointLabels: { color: '#a1a1aa', font: { size: 11 } }, ticks: { display: false }, min: 0, max: 100 } }
    }
  });
}

// ============= INIT =============
renderQAQueue();
renderAgentsTable();
renderTopAgents();
renderTickets();
renderSLABreaches();
renderCharts();
// Pre-populate activity feed so it's ready when user navigates to Overview
startActivityFeed();
</script>
</body>
</html>
