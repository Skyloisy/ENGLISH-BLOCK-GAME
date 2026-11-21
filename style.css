:root {
  --bg: #0f172a;
  --panel: #1e293b;
  --panel-light: #273549;
  --border: #334155;
  --text: #f8fafc;
  --muted: #94a3b8;
  --subj: #3b82f6;
  --subj-dark: #1d4ed8;
  --verb: #f97316;
  --verb-dark: #c2410c;
  --obj: #10b981;
  --obj-dark: #047857;
  --time: #a855f7;
  --time-dark: #7e22ce;
  --gold: #facc15;
  --danger: #ef4444;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  user-select: none;
  -webkit-tap-highlight-color: transparent;
}

body {
  font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
  background: radial-gradient(circle at top, #1e293b 0%, var(--bg) 75%);
  color: var(--text);
  min-height: 100vh;
  display: flex;
  justify-content: center;
  padding: 12px;
  overflow-x: hidden;
}

.app {
  width: 100%;
  max-width: 680px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

/* Header & Stats */
.topbar {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 10px 14px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 8px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.25);
}

.brand {
  display: flex;
  align-items: center;
  gap: 10px;
}

.brand-badge {
  width: 36px;
  height: 36px;
  border-radius: 10px;
  background: linear-gradient(135deg, var(--subj), var(--verb));
  display: grid;
  place-items: center;
  font-weight: 900;
  font-size: 16px;
  box-shadow: 0 4px 10px rgba(59, 130, 246, 0.35);
}

.brand-title h1 {
  font-size: 16px;
  font-weight: 800;
  letter-spacing: 0.4px;
}

.brand-title span {
  font-size: 11px;
  color: var(--muted);
  display: block;
}

.stats {
  display: flex;
  align-items: center;
  gap: 8px;
}

.stat-pill {
  background: var(--bg);
  border: 1px solid var(--border);
  padding: 5px 10px;
  border-radius: 10px;
  text-align: center;
  min-width: 64px;
}

.stat-label {
  font-size: 10px;
  text-transform: uppercase;
  color: var(--muted);
  letter-spacing: 0.5px;
}

.stat-value {
  font-size: 15px;
  font-weight: 800;
}

.stat-value.score { color: var(--gold); }
.stat-value.combo { color: #38bdf8; }
.stat-value.timer { color: #fb7185; }

/* Mode Selector */
.mode-bar {
  display: flex;
  gap: 6px;
  background: var(--panel);
  padding: 5px;
  border-radius: 12px;
  border: 1px solid var(--border);
}

.mode-btn {
  flex: 1;
  border: none;
  background: transparent;
  color: var(--muted);
  font-weight: 700;
  font-size: 12px;
  padding: 7px 8px;
  border-radius: 8px;
  cursor: pointer;
  transition: 0.2s;
}

.mode-btn.active {
  background: var(--subj);
  color: white;
  box-shadow: 0 2px 8px rgba(59, 130, 246, 0.4);
}

/* Color Legend */
.legend {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
  font-size: 11px;
  color: var(--muted);
  padding: 2px 4px;
}

.legend-item {
  display: flex;
  align-items: center;
  gap: 5px;
}

.dot {
  width: 10px;
  height: 10px;
  border-radius: 3px;
}

.dot.subj { background: var(--subj); }
.dot.verb { background: var(--verb); }
.dot.obj { background: var(--obj); }
.dot.time { background: var(--time); }

/* Feedback Banner */
.feedback-banner {
  background: rgba(30, 41, 59, 0.9);
  border: 1px solid var(--border);
  border-left: 4px solid #38bdf8;
  border-radius: 10px;
  padding: 8px 12px;
  font-size: 12.5px;
  min-height: 38px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 8px;
  transition: 0.2s;
}

.feedback-banner.success {
  border-left-color: var(--obj);
  background: rgba(16, 185, 129, 0.14);
  color: #a7f3d0;
}

.feedback-banner.error {
  border-left-color: var(--danger);
  background: rgba(239, 68, 68, 0.14);
  color: #fecaca;
}

/* Game Board */
.board-wrap {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 12px;
  box-shadow: inset 0 2px 10px rgba(0, 0, 0, 0.3);
}

.board {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.row {
  display: grid;
  gap: 8px;
  background: rgba(15, 23, 42, 0.55);
  padding: 8px;
  border-radius: 12px;
  border: 1px solid rgba(51, 65, 85, 0.7);
  transition: transform 0.2s, box-shadow 0.2s, border-color 0.2s;
  position: relative;
}

.row.cols-3 {
  grid-template-columns: repeat(3, 1fr);
}

.row.cols-4 {
  grid-template-columns: repeat(4, 1fr);
}

.row.ready-glow {
  border-color: var(--gold);
  box-shadow: 0 0 16px rgba(250, 204, 21, 0.35);
}

.row.invalid-shake {
  animation: shake 0.38s ease;
  border-color: var(--danger);
}

.row.clearing {
  animation: clearRow 0.45s ease forwards;
}

@keyframes shake {
  0%, 100% { transform: translateX(0); }
  25% { transform: translateX(-6px); }
  50% { transform: translateX(6px); }
  75% { transform: translateX(-4px); }
}

@keyframes clearRow {
  0% { transform: scale(1); opacity: 1; background: rgba(16, 185, 129, 0.35); }
  50% { transform: scale(1.03); opacity: 1; }
  100% { transform: scale(0.92); opacity: 0; }
}

.slot {
  height: 54px;
  border-radius: 10px;
  border: 2px dashed #334155;
  background: rgba(15, 23, 42, 0.45);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 4px;
  cursor: pointer;
  transition: 0.15s;
  position: relative;
}

.slot:hover, .slot.drag-over {
  border-color: #64748b;
  background: rgba(51, 65, 85, 0.4);
}

.slot.hint-valid {
  border-color: var(--gold);
  background: rgba(250, 204, 21, 0.12);
}

.slot-hint {
  font-size: 10px;
  font-weight: 700;
  text-transform: uppercase;
  color: #475569;
  letter-spacing: 0.5px;
}

/* Word Blocks */
.block {
  width: 100%;
  height: 100%;
  border-radius: 9px;
  padding: 6px 8px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-weight: 800;
  font-size: 13px;
  color: white;
  cursor: grab;
  transition: transform 0.15s, box-shadow 0.15s;
  text-align: center;
  line-height: 1.15;
}

.block small {
  font-size: 9px;
  font-weight: 700;
  opacity: 0.85;
  text-transform: uppercase;
  margin-top: 2px;
  letter-spacing: 0.4px;
}

.block.subj {
  background: linear-gradient(180deg, var(--subj), var(--subj-dark));
  box-shadow: 0 4px 0 #1e3a8a;
}

.block.verb {
  background: linear-gradient(180deg, var(--verb), var(--verb-dark));
  box-shadow: 0 4px 0 #7c2d12;
}

.block.obj {
  background: linear-gradient(180deg, var(--obj), var(--obj-dark));
  box-shadow: 0 4px 0 #064e3b;
}

.block.time {
  background: linear-gradient(180deg, var(--time), var(--time-dark));
  box-shadow: 0 4px 0 #4c1d95;
}

.block.selected {
  transform: translateY(-4px) scale(1.04);
  outline: 3px solid var(--gold);
}

/* Tray (Bottom Blocks) */
.tray-section {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 12px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.tray-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 12px;
  color: var(--muted);
}

.powerups {
  display: flex;
  gap: 6px;
}

.power-btn {
  background: var(--panel-light);
  border: 1px solid var(--border);
  color: var(--text);
  font-size: 11px;
  font-weight: 700;
  padding: 5px 9px;
  border-radius: 8px;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 4px;
}

.power-btn:hover:not(:disabled) {
  border-color: var(--gold);
  color: var(--gold);
}

.power-btn:disabled {
  opacity: 0.4;
  cursor: not-allowed;
}

.tray {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  min-height: 68px;
}

.tray-slot {
  height: 66px;
  background: rgba(15, 23, 42, 0.5);
  border-radius: 12px;
  padding: 4px;
  border: 1px solid rgba(51, 65, 85, 0.6);
}

/* Floating Score Pop */
.float-pop {
  position: fixed;
  pointer-events: none;
  font-weight: 900;
  font-size: 18px;
  color: var(--gold);
  text-shadow: 0 2px 8px rgba(0, 0, 0, 0.7);
  animation: floatUp 0.9s ease-out forwards;
  z-index: 50;
}

@keyframes floatUp {
  0% { transform: translateY(0) scale(0.8); opacity: 1; }
  100% { transform: translateY(-48px) scale(1.15); opacity: 0; }
}

/* Modal Game Over */
.modal-backdrop {
  position: fixed;
  inset: 0;
  background: rgba(2, 6, 23, 0.8);
  display: none;
  place-items: center;
  padding: 16px;
  z-index: 100;
}

.modal-backdrop.open {
  display: grid;
}

.modal {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 20px;
  padding: 24px;
  max-width: 380px;
  width: 100%;
  text-align: center;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
}

.modal h2 {
  font-size: 22px;
  margin-bottom: 6px;
}

.modal p {
  color: var(--muted);
  font-size: 13px;
  margin-bottom: 16px;
}

.modal-stats {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
  margin-bottom: 18px;
}

.m-stat {
  background: var(--bg);
  padding: 10px;
  border-radius: 12px;
  border: 1px solid var(--border);
}

.m-stat .k { font-size: 11px; color: var(--muted); }
.m-stat .v { font-size: 20px; font-weight: 800; color: var(--gold); }

.primary-btn {
  width: 100%;
  padding: 12px;
  border: none;
  border-radius: 12px;
  background: linear-gradient(135deg, var(--subj), #2563eb);
  color: white;
  font-weight: 800;
  font-size: 14px;
  cursor: pointer;
}

@media (max-width: 480px) {
  .block { font-size: 11.5px; padding: 4px; }
  .slot { height: 50px; }
  .topbar { flex-wrap: wrap; }
}
