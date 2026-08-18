# 24bda90001-fullstack-24bds-4b-exp1.4.2
<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap');

.cc-root {
  --bg: #12151a;
  --surface: #1a1f26;
  --surface-2: #1e242c;
  --surface-2-hover: #262e37;
  --border: #2c343d;
  --border-soft: #232a32;
  --text-1: #ece9e1;
  --text-2: #9aa3ac;
  --text-3: #626b74;
  --accent: #8c7cf0;
  --accent-strong: #a796ff;
  --accent-ink: #1c1730;
  --draft: #f0b429;
  --scheduled: #4fb0e0;
  --published: #6fbf8b;
  --danger: #e2685f;

  font-family: 'IBM Plex Sans', sans-serif;
  background: var(--bg);
  color: var(--text-1);
  border-radius: 14px;
  border: 1px solid var(--border);
  overflow: hidden;
  position: relative;
  min-height: 640px;
  background-image:
    radial-gradient(var(--border-soft) 1px, transparent 1px);
  background-size: 22px 22px;
}

.cc-root * { box-sizing: border-box; }
.cc-root button { font-family: inherit; cursor: pointer; }
.cc-root input, .cc-root select, .cc-root textarea { font-family: inherit; }

.cc-mono { font-family: 'IBM Plex Mono', monospace; }
.cc-display { font-family: 'Space Grotesk', sans-serif; }

.cc-root :focus-visible {
  outline: 2px solid var(--accent-strong);
  outline-offset: 2px;
}

/* ---------- Toolbar ---------- */
.cc-toolbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
  padding: 22px 26px 14px;
  flex-wrap: wrap;
}
.cc-title-block { display: flex; flex-direction: column; gap: 4px; }
.cc-eyebrow {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 11px;
  letter-spacing: 0.14em;
  color: var(--accent-strong);
  text-transform: uppercase;
}
.cc-title-row { display:flex; align-items:center; gap:10px; flex-wrap: wrap; }
.cc-title {
  font-family: 'Space Grotesk', sans-serif;
  font-weight: 700;
  font-size: 26px;
  letter-spacing: -0.01em;
}
.cc-info-btn {
  width: 22px; height: 22px; border-radius: 50%;
  border: 1px solid var(--border);
  background: var(--surface-2);
  color: var(--text-2);
  font-family: 'IBM Plex Mono', monospace;
  font-size: 12px;
  display: flex; align-items: center; justify-content: center;
  transition: all .15s ease;
}
.cc-info-btn:hover { color: var(--text-1); border-color: var(--accent); }

.cc-toolbar-actions { display: flex; align-items: center; gap: 10px; }
.cc-search {
  display: flex; align-items: center; gap: 8px;
  background: var(--surface-2);
  border: 1px solid var(--border);
  border-radius: 9px;
  padding: 8px 12px;
  min-width: 190px;
}
.cc-search input {
  background: transparent; border: none; outline: none;
  color: var(--text-1); font-size: 13px; width: 100%;
}
.cc-search input::placeholder { color: var(--text-3); }
.cc-search svg { flex-shrink: 0; }

.cc-btn-primary {
  background: var(--accent);
  color: #16121f;
  border: none;
  border-radius: 9px;
  padding: 10px 16px;
  font-weight: 600;
  font-size: 13px;
  display: flex; align-items: center; gap: 6px;
  transition: background .15s ease, transform .1s ease;
}
.cc-btn-primary:hover { background: var(--accent-strong); }
.cc-btn-primary:active { transform: scale(0.97); }

/* ---------- Filters ---------- */
.cc-filters {
  display: flex; align-items: center; gap: 18px;
  padding: 4px 26px 16px;
  flex-wrap: wrap;
  border-bottom: 1px solid var(--border-soft);
}
.cc-filter-group { display: flex; align-items: center; gap: 6px; flex-wrap: wrap; }
.cc-filter-label {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10.5px;
  color: var(--text-3);
  letter-spacing: 0.08em;
  text-transform: uppercase;
  margin-right: 4px;
}
.cc-chip-toggle {
  background: var(--surface-2);
  border: 1px solid var(--border);
  color: var(--text-2);
  border-radius: 20px;
  padding: 5px 12px;
  font-size: 12px;
  display: flex; align-items: center; gap: 6px;
  transition: all .15s ease;
}
.cc-chip-toggle .cc-dot { width: 7px; height: 7px; border-radius: 50%; background: var(--dot, var(--text-3)); }
.cc-chip-toggle.active {
  background: rgba(140,124,240,0.14);
  border-color: var(--accent);
  color: var(--text-1);
}
.cc-chip-toggle:hover { color: var(--text-1); }

/* ---------- Stats ---------- */
.cc-stats {
  display: flex; gap: 22px;
  flex-wrap: wrap;
  padding: 12px 26px;
  font-family: 'IBM Plex Mono', monospace;
  font-size: 12px;
  color: var(--text-2);
  border-bottom: 1px solid var(--border-soft);
}
.cc-stats b { color: var(--text-1); font-weight: 500; }
.cc-stats .cc-stat-dot { width: 7px; height: 7px; border-radius: 50%; display:inline-block; margin-right:5px; }

/* ---------- Calendar header ---------- */
.cc-cal-header {
  display: flex; align-items: center; justify-content: space-between;
  padding: 16px 26px 8px;
}
.cc-month-nav { display: flex; align-items: center; gap: 10px; }
.cc-nav-btn {
  width: 30px; height: 30px; border-radius: 8px;
  border: 1px solid var(--border);
  background: var(--surface-2);
  color: var(--text-2);
  display: flex; align-items: center; justify-content: center;
  transition: all .15s ease;
}
.cc-nav-btn:hover { color: var(--text-1); border-color: var(--accent); }
.cc-month-label {
  font-family: 'Space Grotesk', sans-serif;
  font-weight: 600;
  font-size: 17px;
  min-width: 165px;
  text-align: center;
}
.cc-today-btn {
  background: none; border: 1px solid var(--border); color: var(--text-2);
  border-radius: 8px; padding: 7px 12px; font-size: 12px;
  font-family: 'IBM Plex Mono', monospace;
  transition: all .15s ease;
}
.cc-today-btn:hover { color: var(--text-1); border-color: var(--accent); }

/* ---------- Grid ---------- */
.cc-weekdays {
  display: grid; grid-template-columns: repeat(7, 1fr);
  padding: 6px 26px 0;
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10.5px;
  letter-spacing: 0.08em;
  color: var(--text-3);
}
.cc-weekdays span { padding: 6px 4px; text-transform: uppercase; }

.cc-grid {
  display: grid; grid-template-columns: repeat(7, 1fr);
  gap: 8px;
  padding: 8px 26px 26px;
}
.cc-cell {
  background: var(--surface-2);
  border: 1px solid var(--border-soft);
  border-radius: 10px;
  min-height: 92px;
  padding: 8px;
  display: flex; flex-direction: column; gap: 5px;
  position: relative;
  transition: background .15s ease, border-color .15s ease;
  cursor: pointer;
}
.cc-cell:hover { background: var(--surface-2-hover); border-color: var(--border); }
.cc-cell.cc-other-month { opacity: 0.38; }
.cc-cell.cc-today {
  border-color: var(--accent);
  box-shadow: inset 0 0 0 1px var(--accent);
}
.cc-cell.cc-today::after {
  content: "";
  position: absolute; top: 0; right: 0;
  width: 0; height: 0;
  border-style: solid;
  border-width: 0 16px 16px 0;
  border-color: transparent var(--accent) transparent transparent;
  border-top-right-radius: 9px;
  opacity: 0.9;
}
.cc-cell-head { display: flex; align-items: center; justify-content: space-between; }
.cc-date-num {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 12px;
  color: var(--text-2);
}
.cc-cell.cc-today .cc-date-num { color: var(--accent-strong); font-weight: 600; }
.cc-add-btn {
  width: 18px; height: 18px; border-radius: 5px;
  border: 1px solid var(--border);
  background: transparent;
  color: var(--text-3);
  font-size: 12px; line-height: 1;
  display: flex; align-items: center; justify-content: center;
  opacity: 0; transition: opacity .12s ease, color .12s ease, border-color .12s ease;
}
.cc-cell:hover .cc-add-btn { opacity: 1; }
.cc-add-btn:hover { color: var(--accent-strong); border-color: var(--accent); }

.cc-chip {
  --chip-color: var(--accent);
  background: color-mix(in srgb, var(--chip-color) 16%, var(--surface));
  border-left: 3px solid var(--chip-color);
  border-radius: 5px;
  padding: 3px 7px;
  font-size: 11px;
  display: flex; align-items: center; gap: 5px;
  overflow: hidden;
  transition: transform .12s ease, background .12s ease;
}
.cc-chip:hover { transform: translateX(1px); background: color-mix(in srgb, var(--chip-color) 26%, var(--surface)); }
.cc-chip .cc-chip-time { font-family: 'IBM Plex Mono', monospace; color: var(--text-2); flex-shrink: 0; font-size: 10px; }
.cc-chip .cc-chip-title { color: var(--text-1); overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
.cc-more-btn {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10.5px;
  color: var(--text-3);
  background: none; border: none; text-align: left; padding: 1px 2px;
}
.cc-more-btn:hover { color: var(--accent-strong); }

/* ---------- Agenda (mobile) ---------- */
.cc-agenda-day {
  display: none;
}

/* ---------- Overlay / Drawer ---------- */
.cc-overlay {
  position: absolute; inset: 0;
  background: rgba(8,10,13,0.6);
  opacity: 0; pointer-events: none;
  transition: opacity .18s ease;
  z-index: 20;
}
.cc-overlay.cc-open { opacity: 1; pointer-events: auto; }

.cc-drawer {
  position: absolute; top: 0; right: 0; bottom: 0;
  width: 340px; max-width: 88%;
  background: var(--surface);
  border-left: 1px solid var(--border);
  transform: translateX(100%);
  transition: transform .22s ease;
  z-index: 21;
  display: flex; flex-direction: column;
  padding: 22px;
  overflow-y: auto;
}
.cc-drawer.cc-open { transform: translateX(0); }
.cc-drawer-head { display: flex; align-items: center; justify-content: space-between; margin-bottom: 4px; }
.cc-drawer-title { font-family: 'Space Grotesk', sans-serif; font-weight: 600; font-size: 16px; }
.cc-drawer-date { font-family:'IBM Plex Mono', monospace; font-size: 11px; color: var(--text-3); margin-bottom: 16px; }
.cc-close-btn {
  width: 26px; height: 26px; border-radius: 7px; border: 1px solid var(--border);
  background: var(--surface-2); color: var(--text-2);
  display: flex; align-items: center; justify-content: center;
}
.cc-close-btn:hover { color: var(--text-1); }

.cc-day-list { display: flex; flex-direction: column; gap: 8px; margin-bottom: 16px; }
.cc-day-item {
  background: var(--surface-2); border: 1px solid var(--border-soft);
  border-left: 3px solid var(--item-color, var(--accent));
  border-radius: 8px; padding: 9px 10px;
  display: flex; flex-direction: column; gap: 4px;
}
.cc-day-item-top { display: flex; justify-content: space-between; align-items: flex-start; gap: 8px; }
.cc-day-item-title { font-size: 13px; font-weight: 500; }
.cc-day-item-meta { font-family:'IBM Plex Mono', monospace; font-size: 10.5px; color: var(--text-3); display:flex; gap:8px; }
.cc-day-item-actions { display: flex; gap: 6px; }
.cc-icon-btn {
  background: none; border: none; color: var(--text-3); font-size: 12px;
  padding: 2px 4px; border-radius: 4px;
}
.cc-icon-btn:hover { color: var(--accent-strong); }
.cc-icon-btn.cc-danger:hover { color: var(--danger); }
.cc-empty-note { font-size: 12.5px; color: var(--text-3); padding: 10px 0 4px; }

.cc-field { display: flex; flex-direction: column; gap: 5px; margin-bottom: 14px; }
.cc-field label {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10.5px; letter-spacing: 0.06em; text-transform: uppercase; color: var(--text-3);
}
.cc-field input[type=text], .cc-field input[type=date], .cc-field input[type=time], .cc-field select, .cc-field textarea {
  background: var(--surface-2); border: 1px solid var(--border);
  border-radius: 7px; padding: 8px 10px; color: var(--text-1); font-size: 13px; outline: none;
}
.cc-field textarea { resize: vertical; min-height: 56px; }
.cc-field input:focus, .cc-field select:focus, .cc-field textarea:focus { border-color: var(--accent); }

.cc-radio-row { display: flex; gap: 6px; flex-wrap: wrap; }
.cc-radio-pill {
  border: 1px solid var(--border); background: var(--surface-2); color: var(--text-2);
  border-radius: 20px; padding: 6px 11px; font-size: 12px; display:flex; align-items:center; gap:6px;
}
.cc-radio-pill.active { border-color: var(--pill-color); color: var(--text-1); background: color-mix(in srgb, var(--pill-color) 18%, var(--surface-2)); }

.cc-drawer-actions { display: flex; gap: 8px; margin-top: 4px; }
.cc-btn-secondary {
  flex: 1; background: var(--surface-2); border: 1px solid var(--border); color: var(--text-2);
  border-radius: 8px; padding: 9px; font-size: 13px; font-weight: 500;
}
.cc-btn-secondary:hover { color: var(--text-1); }
.cc-btn-save {
  flex: 1; background: var(--accent); border: none; color: #16121f;
  border-radius: 8px; padding: 9px; font-size: 13px; font-weight: 600;
}
.cc-btn-save:hover { background: var(--accent-strong); }
.cc-back-link {
  background: none; border: none; color: var(--text-3); font-size: 11.5px;
  font-family: 'IBM Plex Mono', monospace; padding: 0 0 14px; text-align: left; align-self: flex-start;
}
.cc-back-link:hover { color: var(--accent-strong); }

/* ---------- About panel ---------- */
.cc-about {
  position: absolute; top: 60px; left: 26px; right: 26px;
  max-width: 480px;
  background: var(--surface); border: 1px solid var(--border);
  border-radius: 12px; padding: 20px 22px;
  z-index: 22; box-shadow: 0 18px 40px rgba(0,0,0,0.4);
  transform: translateY(-8px); opacity: 0; pointer-events: none;
  transition: all .16s ease;
}
.cc-about.cc-open { transform: translateY(0); opacity: 1; pointer-events: auto; }
.cc-about h3 { font-family: 'Space Grotesk', sans-serif; font-size: 15px; margin: 0 0 10px; }
.cc-about p, .cc-about li { font-size: 12.5px; color: var(--text-2); line-height: 1.55; }
.cc-about ul { margin: 6px 0 14px; padding-left: 18px; }
.cc-about .cc-about-label {
  font-family: 'IBM Plex Mono', monospace; font-size: 10px; letter-spacing: 0.08em;
  color: var(--accent-strong); text-transform: uppercase; margin: 12px 0 4px;
}

@media (max-width: 720px) {
  .cc-weekdays { display: none; }
  .cc-grid { display: block; padding: 8px 16px 22px; }
  .cc-cell { display: none; }
  .cc-agenda-day { display: block; margin-bottom: 10px; }
  .cc-agenda-date {
    font-family: 'IBM Plex Mono', monospace; font-size: 11px; color: var(--text-3);
    display: flex; align-items: center; justify-content: space-between;
    padding: 6px 2px;
  }
  .cc-agenda-date.cc-today-label { color: var(--accent-strong); }
  .cc-agenda-items { display: flex; flex-direction: column; gap: 6px; margin-bottom: 4px; }
  .cc-toolbar, .cc-filters { padding-left: 16px; padding-right: 16px; }
  .cc-cal-header { padding-left: 16px; padding-right: 16px; }
  .cc-drawer { width: 100%; max-width: 100%; }
  .cc-about { left: 16px; right: 16px; }
}
</style>

<div class="cc-root" id="ccRoot">

  <div class="cc-toolbar">
    <div class="cc-title-block">
      <span class="cc-eyebrow">Post Schedule</span>
      <div class="cc-title-row">
        <span class="cc-title cc-display">Content Calendar</span>
        <button class="cc-info-btn" id="ccInfoBtn" aria-label="About this project">i</button>
        <button class="cc-today-btn" id="ccResetBtn" style="padding:4px 10px;font-size:10.5px;">Reset data</button>
        <button class="cc-today-btn" id="ccTestBtn" style="padding:4px 10px;font-size:10.5px;">Run tests</button>
      </div>
    </div>
    <div class="cc-toolbar-actions">
      <div class="cc-search">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#626b74" stroke-width="2"><circle cx="11" cy="11" r="7"/><path d="M21 21l-4.3-4.3"/></svg>
        <input type="text" id="ccSearch" placeholder="Search posts…">
      </div>
      <button class="cc-btn-primary" id="ccNewPostBtn">
        <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="#16121f" stroke-width="2.6"><path d="M12 5v14M5 12h14"/></svg>
        New Post
      </button>
    </div>
  </div>

  <div class="cc-about" id="ccAbout">
    <h3>Aim &amp; Project Notes</h3>
    <p><b>Aim:</b> To optimize rendering performance and implement testing strategies for interactive UI components.</p>
    <div class="cc-about-label">Component under test</div>
    <p>The interactive calendar UI from the earlier lab (scheduling &amp; managing posts) — reused here as the subject for performance profiling and test coverage.</p>
    <div class="cc-about-label">Performance objectives</div>
    <ul>
      <li>Measure render cost with <code>performance.now()</code> on every render pass.</li>
      <li>Replace repeated O(cells × posts) filtering with a single O(n) grouping pass per render.</li>
      <li>Debounce the search input (150ms) so rapid typing doesn't trigger a re-render per keystroke.</li>
      <li>Batch DOM writes with a <code>DocumentFragment</code> for the agenda view instead of per-node reflows.</li>
    </ul>
    <div class="cc-about-label">Testing objectives</div>
    <ul>
      <li>Separate pure logic (filtering, grouping, CRUD) from DOM code so it can be unit tested without a browser test runner.</li>
      <li>Cover date formatting, filter/search logic, and add/update/delete behaviour with unit tests.</li>
      <li>Surface pass/fail results directly in the UI via "Run tests".</li>
    </ul>
    <div class="cc-about-label">Built with</div>
    <p>HTML, CSS and vanilla JavaScript; a small self-written assertion-based test runner (no external test framework or build step needed).</p>
  </div>

  <div class="cc-about" id="ccTestPanel"></div>

  <div class="cc-filters">
    <div class="cc-filter-group">
      <span class="cc-filter-label">Platform</span>
      <div id="ccPlatformFilters"></div>
    </div>
    <div class="cc-filter-group">
      <span class="cc-filter-label">Status</span>
      <div id="ccStatusFilters"></div>
    </div>
  </div>

  <div class="cc-stats" id="ccStats"></div>

  <div class="cc-cal-header">
    <div class="cc-month-nav">
      <button class="cc-nav-btn" id="ccPrevBtn" aria-label="Previous month">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#9aa3ac" stroke-width="2.2"><path d="M15 18l-6-6 6-6"/></svg>
      </button>
      <span class="cc-month-label cc-display" id="ccMonthLabel"></span>
      <button class="cc-nav-btn" id="ccNextBtn" aria-label="Next month">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#9aa3ac" stroke-width="2.2"><path d="M9 18l6-6-6-6"/></svg>
      </button>
    </div>
    <button class="cc-today-btn" id="ccTodayBtn">Today</button>
  </div>

  <div class="cc-weekdays">
    <span>Mon</span><span>Tue</span><span>Wed</span><span>Thu</span><span>Fri</span><span>Sat</span><span>Sun</span>
  </div>
  <div class="cc-grid" id="ccGrid"></div>

  <div class="cc-overlay" id="ccOverlay"></div>
  <div class="cc-drawer" id="ccDrawer"></div>
</div>

<script>
(function() {
  const root = document.getElementById('ccRoot');

  const PLATFORMS = [
    { id: 'instagram', label: 'Instagram', color: '#e8577a' },
    { id: 'x',         label: 'X / Twitter', color: '#7fa8c9' },
    { id: 'linkedin',  label: 'LinkedIn',   color: '#5b93d6' },
    { id: 'blog',      label: 'Blog',       color: '#c98a4b' },
    { id: 'youtube',   label: 'YouTube',    color: '#e0665a' },
  ];
  const STATUSES = [
    { id: 'draft',     label: 'Draft',     color: 'var(--draft)' },
    { id: 'scheduled', label: 'Scheduled', color: 'var(--scheduled)' },
    { id: 'published', label: 'Published', color: 'var(--published)' },
  ];
  const platColor = id => (PLATFORMS.find(p => p.id === id) || {}).color || '#8c7cf0';
  const statusColor = id => id === 'draft' ? '#f0b429' : id === 'scheduled' ? '#4fb0e0' : '#6fbf8b';

  const pad = n => String(n).padStart(2, '0');
  const dstr = (y, m, d) => `${y}-${pad(m + 1)}-${pad(d)}`;
  const todayObj = new Date(2026, 6, 29); // demo "today" = 29 Jul 2026
  const todayStr = dstr(todayObj.getFullYear(), todayObj.getMonth(), todayObj.getDate());

  const STORAGE_KEY = 'cc_content_calendar_posts_v1';
  const SEED_POSTS = [
    { id: 100, date: '2026-07-03', time: '09:30', title: 'Product teaser reel', platform: 'instagram', status: 'published', notes: 'Short vertical clip, 15s.' },
    { id: 101, date: '2026-07-06', time: '14:00', title: 'Weekly roundup thread', platform: 'x', status: 'published', notes: '' },
    { id: 102, date: '2026-07-09', time: '11:00', title: 'Case study: campus rollout', platform: 'linkedin', status: 'scheduled', notes: 'Tag partner org.' },
    { id: 103, date: '2026-07-09', time: '18:00', title: 'Behind the scenes story', platform: 'instagram', status: 'draft', notes: '' },
    { id: 104, date: '2026-07-14', time: '10:00', title: 'How we built the scheduler', platform: 'blog', status: 'scheduled', notes: 'Draft link in Drive.' },
    { id: 105, date: '2026-07-17', time: '16:30', title: 'Feature walkthrough video', platform: 'youtube', status: 'draft', notes: '' },
    { id: 106, date: '2026-07-21', time: '09:00', title: 'Poll: next feature vote', platform: 'x', status: 'scheduled', notes: '' },
    { id: 107, date: '2026-07-24', time: '13:15', title: 'Hiring announcement', platform: 'linkedin', status: 'draft', notes: '' },
    { id: 108, date: '2026-07-29', time: '12:00', title: 'Milestone announcement', platform: 'instagram', status: 'scheduled', notes: '' },
    { id: 109, date: '2026-07-29', time: '17:00', title: 'Monthly newsletter', platform: 'blog', status: 'draft', notes: '' },
    { id: 110, date: '2026-08-02', time: '10:00', title: 'August kickoff post', platform: 'x', status: 'draft', notes: '' },
  ];

  let storageOk = true;
  function loadPosts() {
    try {
      const raw = localStorage.getItem(STORAGE_KEY);
      if (raw) return JSON.parse(raw);
      localStorage.setItem(STORAGE_KEY, JSON.stringify(SEED_POSTS));
      return JSON.parse(JSON.stringify(SEED_POSTS));
    } catch (e) {
      storageOk = false;
      return JSON.parse(JSON.stringify(SEED_POSTS));
    }
  }
  function savePosts() {
    if (!storageOk) return;
    try { localStorage.setItem(STORAGE_KEY, JSON.stringify(posts)); }
    catch (e) { storageOk = false; showSaveWarning(); }
  }
  function showSaveWarning() {
    if (document.getElementById('ccSaveWarn')) return;
    const w = document.createElement('div');
    w.id = 'ccSaveWarn';
    w.style.cssText = 'position:absolute;bottom:10px;left:50%;transform:translateX(-50%);background:#e2685f;color:#fff;font-family:"IBM Plex Mono",monospace;font-size:11px;padding:6px 12px;border-radius:6px;z-index:30;';
    w.textContent = "Couldn't save — changes may not persist after reload.";
    root.appendChild(w);
    setTimeout(() => w.remove(), 4000);
  }

  let posts = loadPosts();
  let idSeq = posts.reduce((max, p) => Math.max(max, p.id), 100) + 1;
  let searchDebounceTimer = null;

  let view = { year: 2026, month: 6 }; // 0-indexed month, starts July 2026
  let filters = { platforms: new Set(PLATFORMS.map(p => p.id)), statuses: new Set(STATUSES.map(s => s.id)), search: '' };
  let perfSamples = [];
  let drawerMode = null; // 'day' | 'edit' | 'new'
  let drawerDate = null;
  let drawerPostId = null;

  const monthLabel = document.getElementById('ccMonthLabel');
  const grid = document.getElementById('ccGrid');
  const statsEl = document.getElementById('ccStats');
  const platformFiltersEl = document.getElementById('ccPlatformFilters');
  const statusFiltersEl = document.getElementById('ccStatusFilters');
  const overlay = document.getElementById('ccOverlay');
  const drawer = document.getElementById('ccDrawer');
  const aboutPanel = document.getElementById('ccAbout');

  function buildFilterChips() {
    platformFiltersEl.innerHTML = '';
    PLATFORMS.forEach(p => {
      const b = document.createElement('button');
      b.className = 'cc-chip-toggle active';
      b.style.setProperty('--dot', p.color);
      b.innerHTML = `<span class="cc-dot"></span>${p.label}`;
      b.addEventListener('click', () => {
        if (filters.platforms.has(p.id)) filters.platforms.delete(p.id); else filters.platforms.add(p.id);
        b.classList.toggle('active');
        render();
      });
      platformFiltersEl.appendChild(b);
    });
    statusFiltersEl.innerHTML = '';
    STATUSES.forEach(s => {
      const b = document.createElement('button');
      b.className = 'cc-chip-toggle active';
      b.style.setProperty('--dot', s.color);
      b.innerHTML = `<span class="cc-dot"></span>${s.label}`;
      b.addEventListener('click', () => {
        if (filters.statuses.has(s.id)) filters.statuses.delete(s.id); else filters.statuses.add(s.id);
        b.classList.toggle('active');
        render();
      });
      statusFiltersEl.appendChild(b);
    });
  }

  // Pure logic layer — no DOM access, so these can be unit tested in isolation
  // and are the same functions the UI calls, not a parallel copy.
  function addPostPure(list, post) { return [...list, post]; }
  function updatePostPure(list, id, patch) { return list.map(p => p.id === id ? { ...p, ...patch } : p); }
  function deletePostPure(list, id) { return list.filter(p => p.id !== id); }

  function filterPosts(list, f) {
    const q = f.search.trim().toLowerCase();
    return list.filter(p =>
      f.platforms.has(p.platform) &&
      f.statuses.has(p.status) &&
      (!q || p.title.toLowerCase().includes(q))
    );
  }

  function groupPostsByDate(list) {
    const map = new Map();
    for (const p of list) {
      if (!map.has(p.date)) map.set(p.date, []);
      map.get(p.date).push(p);
    }
    for (const arr of map.values()) arr.sort((a, b) => a.time.localeCompare(b.time));
    return map;
  }

  function visiblePosts() { return filterPosts(posts, filters); }
  function postsForDate(dateStr) { return groupPostsByDate(visiblePosts()).get(dateStr) || []; }

  function renderStats() {
    const vp = visiblePosts().filter(p => p.date.slice(0, 7) === `${view.year}-${pad(view.month + 1)}`);
    const counts = { draft: 0, scheduled: 0, published: 0 };
    vp.forEach(p => counts[p.status]++);
    statsEl.innerHTML = `
      <span><b>${vp.length}</b> post${vp.length === 1 ? '' : 's'} this month</span>
      <span><span class="cc-stat-dot" style="background:${statusColor('draft')}"></span><b>${counts.draft}</b> draft</span>
      <span><span class="cc-stat-dot" style="background:${statusColor('scheduled')}"></span><b>${counts.scheduled}</b> scheduled</span>
      <span><span class="cc-stat-dot" style="background:${statusColor('published')}"></span><b>${counts.published}</b> published</span>
      <span id="ccPerfReadout" class="cc-mono" style="margin-left:auto;color:var(--text-3);"></span>
    `;
  }

  const MONTH_NAMES = ['January','February','March','April','May','June','July','August','September','October','November','December'];

  function render() {
    const t0 = performance.now();
    monthLabel.textContent = `${MONTH_NAMES[view.month]} ${view.year}`;
    grid.innerHTML = '';

    const firstOfMonth = new Date(view.year, view.month, 1);
    const startOffset = (firstOfMonth.getDay() + 6) % 7; // Monday = 0
    const daysInMonth = new Date(view.year, view.month + 1, 0).getDate();
    const prevMonthDays = new Date(view.year, view.month, 0).getDate();

    const cells = [];
    for (let i = startOffset - 1; i >= 0; i--) {
      cells.push({ day: prevMonthDays - i, other: true, y: view.month === 0 ? view.year - 1 : view.year, m: (view.month + 11) % 12 });
    }
    for (let d = 1; d <= daysInMonth; d++) {
      cells.push({ day: d, other: false, y: view.year, m: view.month });
    }
    while (cells.length % 7 !== 0 || cells.length < 35) {
      const last = cells[cells.length - 1];
      const nd = last.other && last.m !== view.month ? 1 : (cells.length - (startOffset + daysInMonth)) + 1;
      cells.push({ day: nd, other: true, y: view.month === 11 ? view.year + 1 : view.year, m: (view.month + 1) % 12 });
    }

    // Group once per render (O(n)) instead of re-filtering the full post list for every cell (was O(cells * n)).
    const grouped = groupPostsByDate(visiblePosts());

    // agenda (mobile) container built alongside grid cells
    const agendaWrap = document.createDocumentFragment();

    cells.forEach(c => {
      const dateStr = dstr(c.y, c.m, c.day);
      const dayPosts = grouped.get(dateStr) || [];
      const isToday = dateStr === todayStr;

      const cell = document.createElement('div');
      cell.className = 'cc-cell' + (c.other ? ' cc-other-month' : '') + (isToday ? ' cc-today' : '');
      cell.addEventListener('click', () => openDayDrawer(dateStr));

      const head = document.createElement('div');
      head.className = 'cc-cell-head';
      head.innerHTML = `<span class="cc-date-num">${c.day}</span>`;
      const addBtn = document.createElement('button');
      addBtn.className = 'cc-add-btn';
      addBtn.setAttribute('aria-label', 'Add post on this day');
      addBtn.textContent = '+';
      addBtn.addEventListener('click', (e) => { e.stopPropagation(); openNewDrawer(dateStr); });
      head.appendChild(addBtn);
      cell.appendChild(head);

      const shown = dayPosts.slice(0, 3);
      shown.forEach(p => cell.appendChild(makeChip(p)));
      if (dayPosts.length > 3) {
        const more = document.createElement('button');
        more.className = 'cc-more-btn';
        more.textContent = `+${dayPosts.length - 3} more`;
        more.addEventListener('click', (e) => { e.stopPropagation(); openDayDrawer(dateStr); });
        cell.appendChild(more);
      }
      grid.appendChild(cell);

      // agenda row (only meaningful for current month, non-empty or today)
      if (!c.other) {
        const aDay = document.createElement('div');
        aDay.className = 'cc-agenda-day';
        const aHead = document.createElement('div');
        aHead.className = 'cc-agenda-date' + (isToday ? ' cc-today-label' : '');
        aHead.innerHTML = `<span>${MONTH_NAMES[c.m].slice(0,3)} ${c.day}${isToday ? ' · Today' : ''}</span>`;
        const addA = document.createElement('button');
        addA.className = 'cc-add-btn';
        addA.style.opacity = '1';
        addA.textContent = '+';
        addA.setAttribute('aria-label', 'Add post on this day');
        addA.addEventListener('click', () => openNewDrawer(dateStr));
        aHead.appendChild(addA);
        aDay.appendChild(aHead);
        const items = document.createElement('div');
        items.className = 'cc-agenda-items';
        dayPosts.forEach(p => items.appendChild(makeChip(p)));
        if (dayPosts.length) aDay.appendChild(items);
        agendaWrap.appendChild(aDay);
      }
    });

    grid.appendChild(agendaWrap);
    renderStats();

    const dt = performance.now() - t0;
    perfSamples.push(dt);
    if (perfSamples.length > 20) perfSamples.shift();
    const avg = perfSamples.reduce((a, b) => a + b, 0) / perfSamples.length;
    const readout = document.getElementById('ccPerfReadout');
    if (readout) readout.textContent = `render ${dt.toFixed(1)}ms · avg ${avg.toFixed(1)}ms`;
  }

  function makeChip(p) {
    const chip = document.createElement('div');
    chip.className = 'cc-chip';
    chip.style.setProperty('--chip-color', platColor(p.platform));
    chip.innerHTML = `<span class="cc-chip-time cc-mono">${p.time}</span><span class="cc-chip-title">${escapeHtml(p.title)}</span>`;
    chip.addEventListener('click', (e) => { e.stopPropagation(); openEditDrawer(p.id); });
    return chip;
  }

  function escapeHtml(s) {
    return s.replace(/[&<>"']/g, ch => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[ch]));
  }

  /* ---------------- Drawer ---------------- */
  function openOverlay() { overlay.classList.add('cc-open'); drawer.classList.add('cc-open'); }
  function closeAll() {
    overlay.classList.remove('cc-open');
    drawer.classList.remove('cc-open');
    aboutPanel.classList.remove('cc-open');
    document.getElementById('ccTestPanel').classList.remove('cc-open');
    drawerMode = null; drawerDate = null; drawerPostId = null;
  }

  function openDayDrawer(dateStr) {
    drawerMode = 'day'; drawerDate = dateStr; drawerPostId = null;
    renderDrawer(); openOverlay();
  }
  function openNewDrawer(dateStr) {
    drawerMode = 'new'; drawerDate = dateStr; drawerPostId = null;
    renderDrawer(); openOverlay();
  }
  function openEditDrawer(postId) {
    const p = posts.find(x => x.id === postId);
    drawerMode = 'edit'; drawerDate = p.date; drawerPostId = postId;
    renderDrawer(); openOverlay();
  }

  function fmtDateHuman(dateStr) {
    const [y, m, d] = dateStr.split('-').map(Number);
    const dt = new Date(y, m - 1, d);
    return dt.toLocaleDateString('en-GB', { weekday: 'long', day: 'numeric', month: 'long', year: 'numeric' });
  }

  function renderDrawer() {
    if (drawerMode === 'day') {
      const dayPosts = postsForDate(drawerDate);
      drawer.innerHTML = `
        <div class="cc-drawer-head">
          <span class="cc-drawer-title cc-display">Posts</span>
          <button class="cc-close-btn" id="ccCloseBtn" aria-label="Close">✕</button>
        </div>
        <div class="cc-drawer-date cc-mono">${fmtDateHuman(drawerDate)}</div>
        <div class="cc-day-list" id="ccDayList"></div>
        <button class="cc-btn-primary" id="ccAddFromDay" style="justify-content:center;">+ Add post</button>
      `;
      const list = drawer.querySelector('#ccDayList');
      if (!dayPosts.length) {
        list.innerHTML = `<div class="cc-empty-note">Nothing scheduled yet — this day is open.</div>`;
      } else {
        dayPosts.forEach(p => {
          const item = document.createElement('div');
          item.className = 'cc-day-item';
          item.style.setProperty('--item-color', platColor(p.platform));
          item.innerHTML = `
            <div class="cc-day-item-top">
              <div>
                <div class="cc-day-item-title">${escapeHtml(p.title)}</div>
                <div class="cc-day-item-meta">
                  <span>${p.time}</span>
                  <span>${PLATFORMS.find(pl=>pl.id===p.platform).label}</span>
                  <span style="color:${statusColor(p.status)}">${p.status}</span>
                </div>
              </div>
              <div class="cc-day-item-actions">
                <button class="cc-icon-btn" data-edit="${p.id}" aria-label="Edit">✎</button>
                <button class="cc-icon-btn cc-danger" data-del="${p.id}" aria-label="Delete">🗑</button>
              </div>
            </div>
          `;
          list.appendChild(item);
        });
        list.querySelectorAll('[data-edit]').forEach(b => b.addEventListener('click', () => openEditDrawer(Number(b.dataset.edit))));
        list.querySelectorAll('[data-del]').forEach(b => b.addEventListener('click', () => {
          posts = deletePostPure(posts, Number(b.dataset.del));
          savePosts();
          render(); renderDrawer();
        }));
      }
      drawer.querySelector('#ccCloseBtn').addEventListener('click', closeAll);
      drawer.querySelector('#ccAddFromDay').addEventListener('click', () => openNewDrawer(drawerDate));
    } else {
      const editing = drawerMode === 'edit';
      const p = editing ? posts.find(x => x.id === drawerPostId) : { date: drawerDate, time: '09:00', title: '', platform: 'instagram', status: 'draft', notes: '' };
      drawer.innerHTML = `
        <button class="cc-back-link" id="ccBackBtn">← back to day</button>
        <div class="cc-drawer-head">
          <span class="cc-drawer-title cc-display">${editing ? 'Edit post' : 'New post'}</span>
          <button class="cc-close-btn" id="ccCloseBtn" aria-label="Close">✕</button>
        </div>
        <div class="cc-drawer-date cc-mono">${fmtDateHuman(p.date)}</div>
        <form id="ccForm">
          <div class="cc-field">
            <label for="ccTitle">Title</label>
            <input type="text" id="ccTitle" required value="${escapeHtml(p.title)}" placeholder="e.g. Product teaser reel">
          </div>
          <div class="cc-field">
            <label for="ccDate">Date</label>
            <input type="date" id="ccDate" required value="${p.date}">
          </div>
          <div class="cc-field">
            <label for="ccTime">Time</label>
            <input type="time" id="ccTime" required value="${p.time}">
          </div>
          <div class="cc-field">
            <label>Platform</label>
            <div class="cc-radio-row" id="ccPlatformRow"></div>
          </div>
          <div class="cc-field">
            <label>Status</label>
            <div class="cc-radio-row" id="ccStatusRow"></div>
          </div>
          <div class="cc-field">
            <label for="ccNotes">Notes</label>
            <textarea id="ccNotes" placeholder="Optional notes…">${escapeHtml(p.notes || '')}</textarea>
          </div>
          <div class="cc-drawer-actions">
            ${editing ? '<button type="button" class="cc-btn-secondary" id="ccDeleteBtn">Delete</button>' : '<button type="button" class="cc-btn-secondary" id="ccCancelBtn">Cancel</button>'}
            <button type="submit" class="cc-btn-save">${editing ? 'Save changes' : 'Add post'}</button>
          </div>
        </form>
      `;
      let selPlatform = p.platform, selStatus = p.status;
      const platRow = drawer.querySelector('#ccPlatformRow');
      PLATFORMS.forEach(pl => {
        const b = document.createElement('button');
        b.type = 'button';
        b.className = 'cc-radio-pill' + (pl.id === selPlatform ? ' active' : '');
        b.style.setProperty('--pill-color', pl.color);
        b.textContent = pl.label;
        b.addEventListener('click', () => {
          selPlatform = pl.id;
          [...platRow.children].forEach(ch => ch.classList.remove('active'));
          b.classList.add('active');
        });
        platRow.appendChild(b);
      });
      const statRow = drawer.querySelector('#ccStatusRow');
      STATUSES.forEach(st => {
        const b = document.createElement('button');
        b.type = 'button';
        b.className = 'cc-radio-pill' + (st.id === selStatus ? ' active' : '');
        b.style.setProperty('--pill-color', statusColor(st.id));
        b.textContent = st.label;
        b.addEventListener('click', () => {
          selStatus = st.id;
          [...statRow.children].forEach(ch => ch.classList.remove('active'));
          b.classList.add('active');
        });
        statRow.appendChild(b);
      });

      drawer.querySelector('#ccCloseBtn').addEventListener('click', closeAll);
      drawer.querySelector('#ccBackBtn').addEventListener('click', () => openDayDrawer(p.date));
      const cancelBtn = drawer.querySelector('#ccCancelBtn');
      if (cancelBtn) cancelBtn.addEventListener('click', () => openDayDrawer(drawerDate));
      const delBtn = drawer.querySelector('#ccDeleteBtn');
      if (delBtn) delBtn.addEventListener('click', () => {
        posts = deletePostPure(posts, p.id);
        savePosts();
        render();
        openDayDrawer(p.date);
      });

      drawer.querySelector('#ccForm').addEventListener('submit', (e) => {
        e.preventDefault();
        const title = drawer.querySelector('#ccTitle').value.trim();
        const date = drawer.querySelector('#ccDate').value;
        const time = drawer.querySelector('#ccTime').value;
        const notes = drawer.querySelector('#ccNotes').value.trim();
        if (!title || !date || !time) return;
        if (editing) {
          posts = updatePostPure(posts, p.id, { title, date, time, platform: selPlatform, status: selStatus, notes });
        } else {
          posts = addPostPure(posts, { id: idSeq++, title, date, time, platform: selPlatform, status: selStatus, notes });
        }
        savePosts();
        render();
        openDayDrawer(date);
      });
    }
  }

  /* ---------------- Lightweight test runner ---------------- */
  function runTests() {
    const results = [];
    function test(name, fn) {
      try { fn(); results.push({ name, pass: true }); }
      catch (e) { results.push({ name, pass: false, error: e.message }); }
    }
    function assertEqual(actual, expected, label) {
      const a = JSON.stringify(actual), b = JSON.stringify(expected);
      if (a !== b) throw new Error(`${label || 'assertEqual'}: expected ${b}, got ${a}`);
    }
    function assertTrue(cond, label) {
      if (!cond) throw new Error(label || 'expected condition to be true');
    }

    const sample = [
      { id: 1, date: '2026-07-05', time: '10:00', title: 'Alpha post', platform: 'instagram', status: 'draft', notes: '' },
      { id: 2, date: '2026-07-05', time: '08:00', title: 'Beta post', platform: 'x', status: 'scheduled', notes: '' },
      { id: 3, date: '2026-07-09', time: '12:00', title: 'Gamma launch', platform: 'blog', status: 'published', notes: '' },
    ];
    const allFilters = { platforms: new Set(['instagram','x','blog','linkedin','youtube']), statuses: new Set(['draft','scheduled','published']), search: '' };

    test('dstr() pads month and day to two digits', () => {
      assertEqual(dstr(2026, 0, 5), '2026-01-05');
    });

    test('groupPostsByDate() groups by date and sorts each group by time', () => {
      const g = groupPostsByDate(sample);
      assertEqual(g.get('2026-07-05').map(p => p.id), [2, 1], 'sort by time ascending');
      assertEqual(g.get('2026-07-09').map(p => p.id), [3]);
      assertTrue(!g.has('2026-07-01'), 'no entry for a date with no posts');
    });

    test('filterPosts() with no filters narrowed returns everything', () => {
      assertEqual(filterPosts(sample, allFilters).length, 3);
    });

    test('filterPosts() narrows by platform', () => {
      const f = { ...allFilters, platforms: new Set(['instagram']) };
      assertEqual(filterPosts(sample, f).map(p => p.id), [1]);
    });

    test('filterPosts() narrows by status', () => {
      const f = { ...allFilters, statuses: new Set(['published']) };
      assertEqual(filterPosts(sample, f).map(p => p.id), [3]);
    });

    test('filterPosts() matches search text case-insensitively', () => {
      const f = { ...allFilters, search: 'LAUNCH' };
      assertEqual(filterPosts(sample, f).map(p => p.id), [3]);
    });

    test('filterPosts() combines platform, status and search', () => {
      const f = { platforms: new Set(['x']), statuses: new Set(['scheduled']), search: 'beta' };
      assertEqual(filterPosts(sample, f).map(p => p.id), [2]);
    });

    test('addPostPure() appends without mutating the original array', () => {
      const next = addPostPure(sample, { id: 4, date: '2026-07-10', time: '09:00', title: 'Delta', platform: 'blog', status: 'draft', notes: '' });
      assertEqual(sample.length, 3, 'original untouched');
      assertEqual(next.length, 4);
      assertEqual(next[3].title, 'Delta');
    });

    test('updatePostPure() patches the matching post only', () => {
      const next = updatePostPure(sample, 2, { status: 'published' });
      assertEqual(next.find(p => p.id === 2).status, 'published');
      assertEqual(next.find(p => p.id === 1).status, 'draft', 'other posts unaffected');
      assertEqual(sample.find(p => p.id === 2).status, 'scheduled', 'original untouched');
    });

    test('deletePostPure() removes only the targeted post', () => {
      const next = deletePostPure(sample, 1);
      assertEqual(next.map(p => p.id), [2, 3]);
      assertEqual(sample.length, 3, 'original untouched');
    });

    test('deletePostPure() is a no-op for an id that does not exist', () => {
      assertEqual(deletePostPure(sample, 999).length, 3);
    });

    return results;
  }

  function renderTestPanel() {
    const results = runTests();
    const passCount = results.filter(r => r.pass).length;
    const panel = document.getElementById('ccTestPanel');
    panel.innerHTML = `
      <h3>Test results</h3>
      <p class="cc-mono" style="color:${passCount === results.length ? 'var(--published)' : 'var(--danger)'};">
        ${passCount} / ${results.length} passed
      </p>
      <div id="ccTestList" style="display:flex;flex-direction:column;gap:6px;margin-top:10px;max-height:320px;overflow-y:auto;"></div>
    `;
    const list = panel.querySelector('#ccTestList');
    results.forEach(r => {
      const row = document.createElement('div');
      row.className = 'cc-day-item';
      row.style.setProperty('--item-color', r.pass ? 'var(--published)' : 'var(--danger)');
      row.innerHTML = `
        <div class="cc-day-item-top">
          <div class="cc-day-item-title" style="font-size:12px;">${r.pass ? '✓' : '✕'} ${escapeHtml(r.name)}</div>
        </div>
        ${r.error ? `<div class="cc-day-item-meta" style="color:var(--danger);">${escapeHtml(r.error)}</div>` : ''}
      `;
      list.appendChild(row);
    });
  }

  /* ---------------- Wiring ---------------- */
  document.getElementById('ccPrevBtn').addEventListener('click', () => {
    view.month--; if (view.month < 0) { view.month = 11; view.year--; } render();
  });
  document.getElementById('ccNextBtn').addEventListener('click', () => {
    view.month++; if (view.month > 11) { view.month = 0; view.year++; } render();
  });
  document.getElementById('ccTodayBtn').addEventListener('click', () => {
    view.year = todayObj.getFullYear(); view.month = todayObj.getMonth(); render();
  });
  document.getElementById('ccNewPostBtn').addEventListener('click', () => openNewDrawer(todayStr));
  document.getElementById('ccSearch').addEventListener('input', (e) => {
    const value = e.target.value;
    clearTimeout(searchDebounceTimer);
    searchDebounceTimer = setTimeout(() => { filters.search = value; render(); }, 150);
  });
  overlay.addEventListener('click', closeAll);
  document.getElementById('ccInfoBtn').addEventListener('click', () => {
    document.getElementById('ccTestPanel').classList.remove('cc-open');
    aboutPanel.classList.toggle('cc-open');
  });
  document.getElementById('ccTestBtn').addEventListener('click', () => {
    aboutPanel.classList.remove('cc-open');
    const panel = document.getElementById('ccTestPanel');
    renderTestPanel();
    panel.classList.add('cc-open');
  });
  document.getElementById('ccResetBtn').addEventListener('click', () => {
    if (!confirm('Reset all posts back to the sample data? This cannot be undone.')) return;
    posts = JSON.parse(JSON.stringify(SEED_POSTS));
    idSeq = posts.reduce((max, p) => Math.max(max, p.id), 100) + 1;
    savePosts();
    render();
  });
  root.addEventListener('keydown', (e) => { if (e.key === 'Escape') closeAll(); });

  buildFilterChips();
  render();
})();
</script>
