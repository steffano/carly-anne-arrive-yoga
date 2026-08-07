# AGENT DIRECTIVES: ARRIVE WEBSITE

## MANDATORY ARCHITECTURAL CONSTRAINTS
1. SINGLE-FILE RULE: ALL markup, Tailwind CDN config, CSS keyframes, inline styles, vector assets, and vanilla JavaScript MUST reside strictly inside `index.html`. 
2. NO EXTERNAL SCRIPT/STYLE FILES: Do NOT create external `.js`, `.css`, or build pipeline configurations (e.g., Webpack, Vite, Tailwind CLI).
3. NO THIRD-PARTY NPM DEPENDENCIES: Rely solely on standard ES7 JavaScript and the Tailwind CSS CDN (`cdn.tailwindcss.com`).

## DESIGN SYSTEM INTEGRATION
- Palette: "Psychedelic Sunset & Disco Lux" (Plum `#2d0a3d`, Neon Pink `#ff007f`, Neon Green `#39ff14`, Peacock Teal `#00f5d4`, Radiant Gold `#ffd700`, Sunset Orange `#ff5e00`).
- Typography: Display headlines MUST use `font-serif` (`Cinzel`), body/UI text MUST use `font-sans` (`Montserrat`).
- Glassmorphism: Cards use `.luxury-glass` (`rgba(22, 5, 31, 0.85)` + backdrop-blur + neon pink border glow).

## CODE MODIFICATION RULES
- When updating JavaScript, preserve existing global state variables (`configState`, `scoreSheet`, `quizMatrix`).
- Always keep the `<body class="psychedelic-sunset-bg...">` mobile overflow shield (`overflow-x-hidden`) intact.
- Format all JS handlers with standard defensive checks (`if (!element) return;`).
