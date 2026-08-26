# LLama.cpp-Custome-css-Theme
Llama.cpp custome premume ui css by AUniCone-dev

Premium UI CSS themes for Llama.cpp by AUniCone-dev.

I created several custom themes for Llama.cpp. They are lightweight CSS files that are easy to install and customize.

Choose your favorite theme, copy the CSS code, and apply it directly through the Llama.cpp Developer settings.

Tip: You can also use the screenshots below as a visual reference before choosing a theme.

(Scroll down 🡓) For more themes

# Purely Premium New looks _ Austra Unicorn (Recommended)

<img width="1416" height="845" alt="Screenshot_20260826_112349" src="https://github.com/user-attachments/assets/d5433ecf-20d4-4e44-bc12-816d348d55da" />



```/* ==========================================================================
   1. ROOT VARIABLES & ANIMATED AMBIENT BACKGROUND
   ========================================================================== */
:root {
  --glass-bg: rgba(255, 255, 255, 0.55);
  --glass-border: rgba(255, 255, 255, 0.85);
  --glass-shadow: 0 12px 35px rgba(31, 38, 135, 0.07);
  --text-main: #0f172a;
  --text-muted: #475569;
  --copilot-gradient: linear-gradient(135deg, #3b82f6 0%, #8b5cf6 50%, #ec4899 100%);
  --copilot-glow: 0 8px 25px rgba(139, 92, 246, 0.35);
}

body, :root {
  background: radial-gradient(circle at 15% 15%, #dbeafe 0%, #eff6ff 45%, #f0f9ff 100%) !important;
  background-attachment: fixed !important;
  color: var(--text-main) !important;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif !important;
}

/* Floating Fluid Aura Glows */
body::before, body::after {
  content: "";
  position: fixed;
  border-radius: 50%;
  pointer-events: none;
  z-index: 0;
  filter: blur(90px);
}

body::before {
  top: -10%;
  right: -5%;
  width: 55vw;
  height: 55vw;
  background: radial-gradient(circle, rgba(147, 51, 234, 0.25), rgba(56, 189, 248, 0.2) 70%, transparent 100%);
  animation: floatAura 14s ease-in-out infinite alternate;
}

body::after {
  bottom: -15%;
  left: -5%;
  width: 45vw;
  height: 45vw;
  background: radial-gradient(circle, rgba(236, 72, 153, 0.18), rgba(99, 102, 241, 0.18) 70%, transparent 100%);
  animation: floatAura 18s ease-in-out infinite alternate-reverse;
}

@keyframes floatAura {
  0% { transform: translate(0, 0) scale(1); }
  100% { transform: translate(-60px, 50px) scale(1.12); }
}

/* ==========================================================================
   2. SIDEBAR & NAVIGATION GLASS
   ========================================================================== */
aside, .sidebar, [class*="sidebar"] {
  background: rgba(255, 255, 255, 0.45) !important;
  backdrop-filter: blur(24px) saturate(190%) !important;
  -webkit-backdrop-filter: blur(24px) saturate(190%) !important;
  border-right: 1px solid var(--glass-border) !important;
  z-index: 2;
}

aside button, .sidebar-item, [class*="nav-item"] {
  border-radius: 12px !important;
  color: var(--text-main) !important;
  transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1) !important;
}

aside button:hover, .sidebar-item:hover {
  background: rgba(255, 255, 255, 0.8) !important;
  transform: translateX(4px);
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.04) !important;
}

/* ==========================================================================
   3. CHAT INPUT BAR & SEARCH FIX (NO LAYOUT GLITCHES)
   ========================================================================== */
form, div:has(> textarea), [class*="chat-input-wrapper"] {
  background: var(--glass-bg) !important;
  backdrop-filter: blur(20px) saturate(180%) !important;
  -webkit-backdrop-filter: blur(20px) saturate(180%) !important;
  border: 1.5px solid var(--glass-border) !important;
  border-radius: 22px !important;
  box-shadow: var(--glass-shadow) !important;
  transition: border-color 0.3s ease, box-shadow 0.3s ease !important;
}

form:focus-within, div:has(> textarea:focus) {
  border-color: rgba(139, 92, 246, 0.6) !important;
  box-shadow: 0 0 0 4px rgba(139, 92, 246, 0.15), var(--glass-shadow) !important;
}

textarea {
  background: transparent !important;
  color: var(--text-main) !important;
  border: none !important;
  box-shadow: none !important;
  outline: none !important;
}

textarea::placeholder {
  color: var(--text-muted) !important;
}

/* ==========================================================================
   4. CHAT BUBBLES
   ========================================================================== */
.user-message, [data-author="user"] {
  background: var(--copilot-gradient) !important;
  color: #ffffff !important;
  border-radius: 20px 20px 4px 20px !important;
  box-shadow: var(--copilot-glow) !important;
  border: 1px solid rgba(255, 255, 255, 0.3) !important;
}

.assistant-message, [data-author="assistant"] {
  background: rgba(255, 255, 255, 0.65) !important;
  backdrop-filter: blur(16px) !important;
  color: var(--text-main) !important;
  border-radius: 20px 20px 20px 4px !important;
  border: 1px solid var(--glass-border) !important;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.03) !important;
}

/* ==========================================================================
   5. BUTTONS, ICONS & ANIMATION EFFECTS (TEXT VISIBILITY SAFE)
   ========================================================================== */
button, .btn, [role="button"] {
  background: rgba(255, 255, 255, 0.75) !important;
  color: var(--text-main) !important;
  border: 1px solid var(--glass-border) !important;
  backdrop-filter: blur(12px) !important;
  border-radius: 12px !important;
  font-weight: 500 !important;
  transition: all 0.25s cubic-bezier(0.34, 1.56, 0.64, 1) !important;
}

button:hover, .btn:hover {
  background: #ffffff !important;
  transform: translateY(-2px) scale(1.02) !important;
  box-shadow: 0 6px 20px rgba(59, 130, 246, 0.15) !important;
}

button:active, .btn:active {
  transform: translateY(0) scale(0.97) !important;
}

/* Icon rotation and scaling micro-interaction */
button svg, .btn svg, button i {
  transition: transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1) !important;
  color: inherit !important;
}

button:hover svg, .btn:hover svg, button:hover i {
  transform: scale(1.18) rotate(6deg);
}

/* Send & Primary Action Buttons Glow */
button[type="submit"], .send-btn, button:has(svg[class*="send"]) {
  background: var(--copilot-gradient) !important;
  color: #ffffff !important;
  border: none !important;
  box-shadow: var(--copilot-glow) !important;
}

button[type="submit"]:hover, .send-btn:hover {
  transform: translateY(-2px) scale(1.06) !important;
  box-shadow: 0 10px 28px rgba(139, 92, 246, 0.5) !important;
}

/* ==========================================================================
   6. SETTINGS MODAL & TEXT RESTORATION
   ========================================================================== */
dialog, .modal-content, [class*="modal"], [class*="settings"] {
  background: rgba(255, 255, 255, 0.85) !important;
  backdrop-filter: blur(28px) saturate(200%) !important;
  -webkit-backdrop-filter: blur(28px) saturate(200%) !important;
  border-radius: 22px !important;
  border: 1px solid var(--glass-border) !important;
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.1) !important;
  color: var(--text-main) !important;
}

/* Global Typography & Icon Visibility Enforcement */
span, p, label, h1, h2, h3, h4, h5, th, td, div {
  color: var(--text-main);
}

small, .text-muted, [class*="subtext"] {
  color: var(--text-muted) !important;
}

/* Code Blocks Glass Styling */
pre, code {
  background: rgba(241, 245, 249, 0.8) !important;
  border: 1px solid rgba(203, 213, 225, 0.6) !important;
  border-radius: 12px !important;
  color: #0284c7 !important;
}
```









# Premium — Organic OS (Recommended)
<img width="1253" height="802" alt="Organic OS" src="https://github.com/user-attachments/assets/6c449a45-5a0b-4931-bc11-64bcaeac0daf" />
CSS Code

```/* ==========================================================================
   Organic OS 11 Ultra-Premium 3D Glass & Animated Bloom Theme (Pure CSS)
   ========================================================================== */

:root {
  --win-blue: #005fb8;
  --win-blue-gloss: linear-gradient(
    135deg,
    #0078d4 0%,
    #005fb8 60%,
    #004585 100%
  );
  --text-main: #0f172a;
  --text-muted: #475569;

  /* Specular Highlights & 3D Glass Shadows */
  --glass-shine-top: inset 0 1px 1px 0 rgba(255, 255, 255, 0.9);
  --glass-3d-shadow:
    0 12px 32px -4px rgba(0, 0, 0, 0.12),
    0 4px 12px -2px rgba(0, 0, 0, 0.06),
    inset 0 -2px 4px 0 rgba(0, 0, 0, 0.04);
}

/* 1. Dynamic Animated Bloom Mesh Background */
body,
html {
  background-color: #dbebe6 !important;
  background-image:
    radial-gradient(
      at 20% 20%,
      rgba(0, 120, 212, 0.7) 0px,
      transparent 50%
    ),
    radial-gradient(
      at 80% 15%,
      rgba(168, 85, 247, 0.6) 0px,
      transparent 50%
    ),
    radial-gradient(
      at 25% 60%,
      rgba(56, 189, 248, 0.65) 0px,
      transparent 50%
    ),
    radial-gradient(
      at 75% 70%,
      rgba(244, 63, 94, 0.5) 0px,
      transparent 50%
    ),
    radial-gradient(
      at 40% 90%,
      rgba(99, 102, 241, 0.6) 0px,
      transparent 50%
    ),
    radial-gradient(
      at 90% 90%,
      rgba(20, 184, 166, 0.45) 0px,
      transparent 50%
    ) !important;

  background-size: 160% 160% !important;
  background-attachment: fixed !important;
  animation: bloomPulse 18s ease-in-out infinite alternate !important;
  color: var(--text-main) !important;
  font-family:
    "Segoe UI Variable Text",
    "Segoe UI",
    system-ui,
    sans-serif !important;
  margin: 0;
  min-height: 100vh;
  position: relative;
  z-index: 0;
}

@keyframes bloomPulse {
  0% {
    background-position: 0% 0%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0% 100%;
  }
}

/* 2. Global Frosted Glass Overlay */
body::before {
  content: "";
  position: fixed;
  inset: -50px;
  background: rgba(255, 255, 255, 0.35) !important;
  backdrop-filter: blur(50px) saturate(180%) !important;
  -webkit-backdrop-filter: blur(50px) saturate(180%) !important;
  z-index: -1;
  pointer-events: none;
}

/* 3. Deep 3D Blurry Sidebar with Specular Sheen */
aside,
.sidebar,
[class*="sidebar"],
div:has(> button:contains("New chat")) {
  background: rgba(255, 255, 255, 0.42) !important;
  backdrop-filter: blur(35px) saturate(190%) !important;
  -webkit-backdrop-filter: blur(35px) saturate(190%) !important;
  border-right: 1px solid rgba(255, 255, 255, 0.85) !important;
  box-shadow:
    6px 0 28px rgba(0, 0, 0, 0.05),
    var(--glass-shine-top) !important;
  color: var(--text-main) !important;
  border-radius: 0 16px 16px 0 !important;
  transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1) !important;
}

aside div,
aside span,
aside a,
.sidebar div {
  color: var(--text-main) !important;
}

/* 4. 3D Glossy Chat Input Field */
textarea,
input[type="text"],
.input-container,
div:has(> textarea) {
  background: rgba(255, 255, 255, 0.72) !important;
  backdrop-filter: blur(30px) saturate(160%) !important;
  -webkit-backdrop-filter: blur(30px) saturate(160%) !important;
  color: var(--text-main) !important;
  border: 1px solid rgba(255, 255, 255, 0.9) !important;
  border-bottom: 2px solid rgba(0, 0, 0, 0.12) !important;
  border-radius: 18px !important;
  box-shadow:
    var(--glass-3d-shadow),
    var(--glass-shine-top) !important;
  transition: all 0.25s cubic-bezier(0.16, 1, 0.3, 1) !important;
}

textarea:focus,
input:focus {
  background: rgba(255, 255, 255, 0.92) !important;
  border-color: rgba(0, 95, 184, 0.4) !important;
  border-bottom: 2px solid var(--win-blue) !important;
  transform: translateY(-2px) scale(1.002);
  box-shadow:
    0 16px 36px -4px rgba(0, 95, 184, 0.18),
    0 4px 12px rgba(0, 0, 0, 0.04),
    var(--glass-shine-top) !important;
  outline: none !important;
}

/* 5. Elevated 3D Chat Bubbles */
.message,
.chat-message {
  border-radius: 14px !important;
  padding: 16px 20px !important;
  margin-bottom: 16px !important;
  color: var(--text-main) !important;
  font-size: 15px !important;
  line-height: 1.6 !important;
  transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1) !important;
}

/* User Bubble: 3D Tinted Glass */
.message.user,
.user-message {
  background: rgba(0, 95, 184, 0.09) !important;
  border: 1px solid rgba(0, 95, 184, 0.2) !important;
  box-shadow:
    0 8px 20px -4px rgba(0, 95, 184, 0.12),
    inset 0 1px 1px 0 rgba(255, 255, 255, 0.7) !important;
  margin-left: auto;
}

/* AI Bubble: 3D Frosted White Card */
.message.bot,
.assistant-message {
  background: rgba(255, 255, 255, 0.82) !important;
  border: 1px solid rgba(255, 255, 255, 0.95) !important;
  backdrop-filter: blur(20px) !important;
  -webkit-backdrop-filter: blur(20px) !important;
  box-shadow:
    var(--glass-3d-shadow),
    var(--glass-shine-top) !important;
}

/* 6. Dynamic 3D Shiny Buttons with Sweep Sheen */
button,
.btn,
.model-selector {
  position: relative !important;
  overflow: hidden !important;
  background: var(--win-blue-gloss) !important;
  color: #ffffff !important;
  border: 1px solid rgba(255, 255, 255, 0.35) !important;
  border-radius: 8px !important;
  padding: 9px 18px !important;
  font-weight: 600 !important;
  cursor: pointer;
  box-shadow:
    0 6px 16px -2px rgba(0, 95, 184, 0.35),
    inset 0 1px 1px 0 rgba(255, 255, 255, 0.5),
    inset 0 -2px 4px 0 rgba(0, 0, 0, 0.2) !important;
  transition: all 0.25s cubic-bezier(0.16, 1, 0.3, 1) !important;
  transform-style: preserve-3d;
}

/* Animated Reflective Light Sweep Across Buttons */
button::after,
.btn::after,
.model-selector::after {
  content: "";
  position: absolute;
  top: -50%;
  left: -150%;
  width: 200%;
  height: 200%;
  background: linear-gradient(
    60deg,
    transparent 30%,
    rgba(255, 255, 255, 0.45) 50%,
    transparent 70%
  );
  transition: all 0.6s ease;
  pointer-events: none;
}

button:hover::after,
.btn:hover::after,
.model-selector:hover::after {
  left: 100%;
}

button:hover,
.btn:hover,
.model-selector:hover {
  transform: translateY(-2px) scale(1.02);
  box-shadow:
    0 10px 24px -2px rgba(0, 95, 184, 0.45),
    inset 0 1px 2px 0 rgba(255, 255, 255, 0.8),
    inset 0 -2px 4px 0 rgba(0, 0, 0, 0.15) !important;
}

button:active,
.btn:active,
.model-selector:active {
  transform: translateY(1px) scale(0.98);
  box-shadow:
    0 2px 6px rgba(0, 95, 184, 0.25),
    inset 0 2px 4px rgba(0, 0, 0, 0.3) !important;
}

/* Secondary Circular/Icon Buttons */
button.secondary,
button:empty,
[aria-label="Send"],
.add-btn {
  background: rgba(255, 255, 255, 0.65) !important;
  color: var(--text-main) !important;
  border: 1px solid rgba(255, 255, 255, 0.9) !important;
  border-radius: 50% !important;
  backdrop-filter: blur(12px) !important;
  box-shadow:
    0 4px 12px rgba(0, 0, 0, 0.08),
    var(--glass-shine-top) !important;
}

button.secondary:hover,
button:empty:hover {
  background: rgba(255, 255, 255, 0.95) !important;
  transform: translateY(-2px) rotate(5deg) scale(1.05);
  box-shadow:
    0 8px 18px rgba(0, 0, 0, 0.12),
    var(--glass-shine-top) !important;
}
```

# Premium — Kline OS (Recommended)
<img width="1251" height="801" alt="Kline OS" src="https://github.com/user-attachments/assets/86a746b7-b152-4bf7-93cc-c81f260619fc" />
CSS Code


```/* ==========================================================================
   Llama.cpp Premium Glassmorphic & Animated CSS Theme
   ========================================================================== */

/* Root Variables & Color Palette */
:root {
  --bg-gradient-1: #0f172a;
  --bg-gradient-2: #1e1b4b;
  --bg-gradient-3: #2e1065;
  --glass-bg: rgba(15, 23, 42, 0.65);
  --glass-border: rgba(255, 255, 255, 0.12);
  --glass-glow: rgba(168, 85, 247, 0.25);

  --accent-primary: linear-gradient(135deg, #a855f7 0%, #6366f1 100%);
  --accent-hover: linear-gradient(135deg, #c084fc 0%, #818cf8 100%);
  --text-main: #f8fafc;
  --text-muted: #94a3b8;
  --user-msg-bg: rgba(99, 102, 241, 0.25);
  --bot-msg-bg: rgba(255, 255, 255, 0.05);
}

/* Animated Ambient Background */
body {
  background: linear-gradient(
    -45deg,
    var(--bg-gradient-1),
    var(--bg-gradient-2),
    var(--bg-gradient-3),
    #090d16
  );
  background-size: 400% 400%;
  animation: gradientBG 18s ease infinite;
  color: var(--text-main);
  font-family: "Inter", system-ui, -apple-system, sans-serif;
  margin: 0;
  min-height: 100vh;
}

@keyframes gradientBG {
  0% {
    background-position: 0% 50%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0% 50%;
  }
}

/* Glassmorphic Cards & Containers */
.container,
.chat-container,
.panel,
textarea,
select,
input {
  background: var(--glass-bg) !important;
  backdrop-filter: blur(16px) saturate(180%);
  -webkit-backdrop-filter: blur(16px) saturate(180%);
  border: 1px solid var(--glass-border) !important;
  border-radius: 16px !important;
  box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
  transition: all 0.3s ease;
}

/* Glowing Hover Effect for Inputs & Panels */
textarea:focus,
input:focus,
.panel:hover {
  border-color: rgba(168, 85, 247, 0.5) !important;
  box-shadow: 0 0 20px var(--glass-glow) !important;
  outline: none !important;
}

/* Chat Bubbles Styling */
.message,
.chat-message {
  border-radius: 14px !important;
  padding: 14px 18px !important;
  margin-bottom: 12px !important;
  backdrop-filter: blur(10px);
}

.message.user,
.user-message {
  background: var(--user-msg-bg) !important;
  border: 1px solid rgba(99, 102, 241, 0.3) !important;
  margin-left: auto;
}

.message.bot,
.assistant-message {
  background: var(--bot-msg-bg) !important;
  border: 1px solid var(--glass-border) !important;
}

/* Premium Gradient Buttons */
button,
.btn {
  background: var(--accent-primary) !important;
  color: #ffffff !important;
  border: none !important;
  border-radius: 10px !important;
  padding: 10px 20px !important;
  font-weight: 600 !important;
  cursor: pointer;
  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease !important;
}

button:hover,
.btn:hover {
  background: var(--accent-hover) !important;
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(168, 85, 247, 0.4) !important;
}

button:active,
.btn:active {
  transform: translateY(0);
}

/* Scrollbars */
::-webkit-scrollbar {
  width: 8px;
  height: 8px;
}

::-webkit-scrollbar-track {
  background: rgba(0, 0, 0, 0.1);
}

::-webkit-scrollbar-thumb {
  background: rgba(255, 255, 255, 0.2);
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: rgba(168, 85, 247, 0.5);
}
```

# Modern Arch (Recommended)
<img width="1250" height="808" alt="Modern Arch" src="https://github.com/user-attachments/assets/39928131-4d30-4cc2-bcf1-d3cf04799d19" />
CSS Code


```/* ==========================================================================
   Windows 11 Light Glass Theme (Pure CSS)
   ========================================================================== */

:root {
  /* Windows 11 Light Mode Colors */
  --win-blue: #005fb8;
  --win-blue-hover: #0053a0;
  --text-main: #1a1a1a;
  --text-muted: #5d5d5d;

  /* Light Acrylic / Mica Materials */
  --glass-sidebar: rgba(245, 245, 245, 0.55);
  --glass-input: rgba(255, 255, 255, 0.85);
  --glass-border: rgba(255, 255, 255, 0.7);

  /* Chat Bubble Colors */
  --user-msg-bg: rgba(0, 95, 184, 0.08);
  --user-msg-border: rgba(0, 95, 184, 0.15);
  --bot-msg-bg: rgba(255, 255, 255, 0.9);
}

/* 1. Highly Detailed Blurred Background Image */
body,
html {
  background-image: url("2560x1440.jpg") !important;
  background-size: cover !important;
  background-position: center !important;
  background-attachment: fixed !important;
  color: var(--text-main) !important;
  font-family:
    "Segoe UI Variable Text",
    "Segoe UI",
    system-ui,
    sans-serif !important;
  margin: 0;
  min-height: 100vh;
  position: relative;
  z-index: 0;
}

/* Apply the blur specifically to a backdrop layer */
body::before {
  content: "";
  position: fixed;
  inset: 0;
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(35px) saturate(130%);
  -webkit-backdrop-filter: blur(35px) saturate(130%);
  z-index: -1;
  pointer-events: none;
}

/* 2. Main Containers & Sidebar */
.container,
.chat-container,
.panel,
aside,
[class*="sidebar"] {
  background: var(--glass-sidebar) !important;
  backdrop-filter: blur(25px) saturate(140%) !important;
  -webkit-backdrop-filter: blur(25px) saturate(140%) !important;
  border: 1px solid var(--glass-border) !important;
  border-radius: 12px !important;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08) !important;
  color: var(--text-main) !important;
}

/* Text overrides for sidebar items */
[class*="sidebar"] div,
[class*="sidebar"] span,
[class*="sidebar"] a {
  color: var(--text-main) !important;
}

/* 3. Input Areas */
textarea,
input[type="text"],
select,
.input-container {
  background: var(--glass-input) !important;
  color: var(--text-main) !important;
  border: 1px solid rgba(0, 0, 0, 0.08) !important;
  border-bottom: 2px solid transparent !important;
  border-radius: 16px !important;
  box-shadow: 0 6px 24px rgba(0, 0, 0, 0.05) !important;
  padding: 14px 18px !important;
  transition: all 0.25s ease !important;
}

textarea:focus,
input:focus {
  background: #ffffff !important;
  border-color: rgba(0, 0, 0, 0.1) !important;
  border-bottom: 2px solid var(--win-blue) !important;
  box-shadow: 0 8px 28px rgba(0, 95, 184, 0.15) !important;
  outline: none !important;
}

textarea::placeholder,
input::placeholder {
  color: var(--text-muted) !important;
}

/* 4. Chat Bubbles */
.message,
.chat-message,
[class*="message"] {
  border-radius: 12px !important;
  padding: 16px 20px !important;
  margin-bottom: 16px !important;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04) !important;
  color: var(--text-main) !important;
  font-size: 15px !important;
  line-height: 1.6 !important;
}

/* User Text */
.message.user,
.user-message,
[class*="user"] {
  background: var(--user-msg-bg) !important;
  border: 1px solid var(--user-msg-border) !important;
  margin-left: auto;
}

/* AI Text */
.message.bot,
.assistant-message,
[class*="bot"],
[class*="ai"] {
  background: var(--bot-msg-bg) !important;
  border: 1px solid var(--glass-border) !important;
  backdrop-filter: blur(10px) !important;
}

/* 5. Buttons */
button,
.btn {
  background: var(--win-blue) !important;
  color: #ffffff !important;
  border: none !important;
  border-radius: 6px !important;
  padding: 8px 16px !important;
  font-weight: 500 !important;
  cursor: pointer;
  box-shadow: 0 2px 6px rgba(0, 95, 184, 0.2) !important;
  transition: all 0.2s ease !important;
}

button:hover,
.btn:hover {
  background: var(--win-blue-hover) !important;
  transform: translateY(-1px);
  box-shadow: 0 4px 10px rgba(0, 95, 184, 0.3) !important;
}

/* Secondary / Icon Buttons */
button.secondary,
button.icon-btn,
[aria-label="Send"],
.add-btn,
button:empty {
  background: rgba(0, 0, 0, 0.05) !important;
  color: var(--text-main) !important;
  box-shadow: none !important;
  border-radius: 50% !important;
}

button.secondary:hover,
button.icon-btn:hover,
[aria-label="Send"]:hover,
.add-btn:hover {
  background: rgba(0, 0, 0, 0.1) !important;
}
```

# Sinoatic Arc
<img width="1256" height="807" alt="Sinoatic Arc" src="https://github.com/user-attachments/assets/dc7e87b8-9a98-492c-bab0-f6404c8b2ee1" />
CSS Code


```/* ==========================================================================
   Cyber Emerald Theme for Llama.cpp
   ========================================================================== */

:root {
  --bg-gradient-1: #022c22;
  --bg-gradient-2: #064e3b;
  --bg-gradient-3: #020617;
  --glass-bg: rgba(6, 78, 59, 0.45);
  --glass-border: rgba(52, 211, 153, 0.25);
  --glass-glow: rgba(16, 185, 129, 0.35);

  --accent-primary: linear-gradient(135deg, #10b981 0%, #06b6d4 100%);
  --accent-hover: linear-gradient(135deg, #34d399 0%, #22d3ee 100%);
  --text-main: #f0fdf4;
  --text-muted: #94a3b8;
  --user-msg-bg: rgba(6, 182, 212, 0.2);
  --bot-msg-bg: rgba(255, 255, 255, 0.04);
}

body {
  background: linear-gradient(
    -45deg,
    var(--bg-gradient-1),
    var(--bg-gradient-2),
    var(--bg-gradient-3),
    #01130e
  );
  background-size: 400% 400%;
  animation: emeraldFlow 16s ease infinite;
  color: var(--text-main);
  font-family: "Inter", system-ui, sans-serif;
  margin: 0;
  min-height: 100vh;
}

@keyframes emeraldFlow {
  0% {
    background-position: 0% 50%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0% 50%;
  }
}

.container,
.chat-container,
.panel,
textarea,
select,
input {
  background: var(--glass-bg) !important;
  backdrop-filter: blur(18px) saturate(180%);
  -webkit-backdrop-filter: blur(18px) saturate(180%);
  border: 1px solid var(--glass-border) !important;
  border-radius: 16px !important;
  box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.45);
}

textarea:focus,
input:focus,
.panel:hover {
  border-color: rgba(52, 211, 153, 0.6) !important;
  box-shadow: 0 0 22px var(--glass-glow) !important;
  outline: none !important;
}

.message.user,
.user-message {
  background: var(--user-msg-bg) !important;
  border: 1px solid rgba(34, 211, 238, 0.3) !important;
  border-radius: 14px !important;
}

.message.bot,
.assistant-message {
  background: var(--bot-msg-bg) !important;
  border: 1px solid var(--glass-border) !important;
  border-radius: 14px !important;
}

button,
.btn {
  background: var(--accent-primary) !important;
  color: #022c22 !important;
  font-weight: 700 !important;
  border: none !important;
  border-radius: 10px !important;
  padding: 10px 20px !important;
  cursor: pointer;
  transition: all 0.25s ease !important;
}

button:hover,
.btn:hover {
  background: var(--accent-hover) !important;
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(52, 211, 153, 0.4) !important;
}


```
# Luiev
<img width="1257" height="806" alt="Luiev" src="https://github.com/user-attachments/assets/b009e756-8e20-4350-a26b-df766c3895d7" />
CSS Code

```/* ==========================================================================
   Windows 11 Premium Mica & Fluent v2 Theme for Llama.cpp
   ========================================================================== */

/* Windows 11 System Tokens & Color Variables */
:root {
  /* Mica / Acrylic Dark Base Surfaces */
  --win-bg-base: #0f0f11;
  --win-mica-layer1: rgba(32, 32, 32, 0.72);
  --win-mica-layer2: rgba(44, 44, 44, 0.65);
  --win-card-bg: rgba(255, 255, 255, 0.05);

  /* Windows 11 Fluent Borders & Outlines */
  --win-border-stroke: rgba(255, 255, 255, 0.08);
  --win-border-subtle: rgba(255, 255, 255, 0.05);
  --win-border-accent: rgba(96, 205, 255, 0.6);

  /* Windows 11 Blue Accent Gradient */
  --win-accent: #0078d4;
  --win-accent-light: #60cdff;
  --win-accent-gradient: linear-gradient(
    135deg,
    #0078d4 0%,
    #005a9e 100%
  );
  --win-accent-hover: linear-gradient(
    135deg,
    #1890e8 0%,
    #0078d4 100%
  );

  /* Windows Typography System */
  --win-text-primary: #ffffff;
  --win-text-secondary: rgba(255, 255, 255, 0.605);
  --win-font-family:
    "Segoe UI Variable Text",
    "Segoe UI",
    system-ui,
    -apple-system,
    sans-serif;

  /* Geometry & Motion */
  --win-radius-window: 12px;
  --win-radius-control: 8px;
  --win-radius-pill: 9999px;
  --win-ease-spring: cubic-bezier(0.1, 0.9, 0.2, 1);
}

/* Background Shell with Soft Fluent Ambient Lights */
body {
  background-color: var(--win-bg-base);
  color: var(--win-text-primary);
  font-family: var(--win-font-family);
  margin: 0;
  min-height: 100vh;
  position: relative;
  overflow-x: hidden;
  -webkit-font-smoothing: antialiased;
}

/* Subtle Animated Ambient Glow */
body::before {
  content: "";
  position: fixed;
  top: -15%;
  right: 10%;
  width: 700px;
  height: 700px;
  background: radial-gradient(
    circle,
    rgba(0, 120, 212, 0.12) 0%,
    rgba(0, 0, 0, 0) 70%
  );
  filter: blur(100px);
  pointer-events: none;
  z-index: 0;
}

/* Win 11 Acrylic & Glassmorphism Panels */
.container,
.chat-container,
.panel,
textarea,
select,
input {
  background: var(--win-mica-layer1) !important;
  backdrop-filter: blur(30px) saturate(125%) !important;
  -webkit-backdrop-filter: blur(30px) saturate(125%) !important;
  border: 1px solid var(--win-border-stroke) !important;
  border-radius: var(--win-radius-window) !important;
  box-shadow:
    0 16px 32px rgba(0, 0, 0, 0.36),
    0 2px 6px rgba(0, 0, 0, 0.12);
  transition: all 0.25s var(--win-ease-spring);
}

/* Input Fields & Textareas */
textarea,
input[type="text"],
select {
  background: rgba(0, 0, 0, 0.2) !important;
  color: var(--win-text-primary) !important;
  border: 1px solid var(--win-border-stroke) !important;
  border-bottom: 1px solid rgba(255, 255, 255, 0.2) !important;
  border-radius: var(--win-radius-control) !important;
  padding: 12px 16px !important;
  font-size: 14px;
}

/* Active Focus State */
textarea:focus,
input:focus {
  background: rgba(0, 0, 0, 0.35) !important;
  border-color: var(--win-border-accent) !important;
  border-bottom: 2px solid var(--win-accent-light) !important;
  box-shadow: 0 0 12px rgba(96, 205, 255, 0.25) !important;
  outline: none !important;
}

/* Chat Bubbles */
.message,
.chat-message {
  border-radius: var(--win-radius-control) !important;
  padding: 14px 18px !important;
  margin-bottom: 12px !important;
  font-size: 14px;
  line-height: 1.5;
}

.message.user,
.user-message {
  background: rgba(0, 120, 212, 0.2) !important;
  border: 1px solid rgba(96, 205, 255, 0.25) !important;
  margin-left: auto;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.message.bot,
.assistant-message {
  background: var(--win-card-bg) !important;
  border: 1px solid var(--win-border-subtle) !important;
  backdrop-filter: blur(10px);
}

/* Fluent Action Buttons */
button,
.btn {
  background: var(--win-accent-gradient) !important;
  color: #ffffff !important;
  font-family: var(--win-font-family) !important;
  font-weight: 600 !important;
  font-size: 13.5px !important;
  border: 1px solid rgba(255, 255, 255, 0.15) !important;
  border-radius: var(--win-radius-control) !important;
  padding: 9px 20px !important;
  cursor: pointer;
  transition: all 0.15s var(--win-ease-spring) !important;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2) !important;
}

button:hover,
.btn:hover {
  background: var(--win-accent-hover) !important;
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(0, 120, 212, 0.35) !important;
}

button:active,
.btn:active {
  transform: translateY(1px) scale(0.98);
  opacity: 0.9;
}

/* Windows 11 Native Thin Scrollbars */
::-webkit-scrollbar {
  width: 6px;
  height: 6px;
}

::-webkit-scrollbar-track {
  background: transparent;
}

::-webkit-scrollbar-thumb {
  background: rgba(255, 255, 255, 0.18);
  border-radius: var(--win-radius-pill);
}

::-webkit-scrollbar-thumb:hover {
  background: rgba(255, 255, 255, 0.35);
}

```

# Credite 

Themes Included
Organic OS — Ultra-premium 3D glass and animated bloom design.
Kline OS — Dark glassmorphic design with purple and indigo accents.
Modern Arch — Windows 11-inspired light acrylic design.
Sinoatic Arc — Cyber emerald glass theme with green and cyan accents.
Luiev — Windows 11 Premium Mica and Fluent-inspired dark theme.
Oceanic Glass — Deep ocean glassmorphic theme with cyan and blue accents.
Credits

Created with by AUniCone-dev.

If you like these themes, consider ⭐ starring the repository and sharing it with other Llama.cpp users.

