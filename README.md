fast Word Displayer

A clean, no-nonsense, word-by-word reader with an immersive fullscreen mode, simple controls, a built-in Analyzer for your reading stats, and a Converter that turns PDFs/EPUBs into plain text right in the browser. No servers. No logins. Just open the page and read.

What it does (in plain terms)

Paste or drop text and the app shows it one word at a time at your pace (WPM slider + numeric input).

Fullscreen “cinema” mode for pure focus (toggle with Shift+Enter).

Spacebar to play/pause, ←/→ to step words, and mouse wheel scrubbing while in fullscreen.

Analyzer tab tracks your session: time spent, words shown, and pause count, plus a live activity log.

Converter tab: drop a PDF or EPUB, extract text client-side, then send it straight to the reader or download a .txt.

Adjustable text size and theme brightness so it looks great on any screen.

Quick demo of the vibe

Minimal black UI, high contrast, smooth transitions, big type, and zero clutter. It’s meant to disappear and let the words do their thing.

How it works (under the hood)

The text is cleaned and split into words, then a timer advances the index based on WPM.

Two displays share the same state: the normal word area and a fullscreen overlay. Going fullscreen adds a body class and shows a dedicated overlay for crisp, centered words.

Mouse wheel in fullscreen pauses playback and nudges word index forward/back with a tiny cooldown so it feels responsive but not jittery.

PDF to text uses PDF.js to read page content; EPUB to text uses JSZip to open the container, follows the OPF spine when possible, and falls back to scanning XHTML/HTML files, stripping scripts/styles and flattening to plain text.

Everything runs entirely client-side (static HTML + JS + Tailwind via CDN).

Keyboard shortcuts

Space — Play/Pause

Shift+Enter — Toggle Fullscreen

→ / ← — Next/Previous word

(During fullscreen) Mouse wheel — Scrub words (auto-pauses)

Features at a glance

WPM control (slider + numeric, 50–1000 WPM)

Text size control (20–120 px)

Theme brightness (0–100%)

Optional “Ask for fullscreen on Start” prompt

Drag-and-drop .txt import

PDF/EPUB Convert → Send to Reader

Analyzer stats + Activity Log with timestamps

Toasts, modals, and smooth transitions so the UX feels polished

Tech stack

HTML + Vanilla JS (no frameworks)

Tailwind CSS (CDN)

PDF.js for PDF extraction

JSZip for EPUB parsing

Getting started

Clone the repo or download the files.

Open index.html in your browser. That’s it.

Pro tip: If the browser blocks local file access for the Converter, run a tiny static server (e.g., python -m http.server) and open http://localhost:8000.

Deploying on GitHub Pages (super quick)

Push this project to a GitHub repo.

Go to Settings → Pages.

Set Source to Deploy from a branch, pick your default branch, and / (root).

Save. Pages will build and give you a public URL.
