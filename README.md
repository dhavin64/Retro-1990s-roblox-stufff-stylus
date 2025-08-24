# Retro-1990s-roblox-stufff-stylus

/* ==UserStyle==
@name           Roblox — 1990s Retro Theme
@namespace      github.com/openstyles/stylus
@version        1.0.2
@description    A neon retro 90s style theme for Roblox
@preprocessor   default
==/UserStyle== */

@-moz-document domain("roblox.com") {
    :root {
        --retro-bg: #0b001a; /* deep dark purple */
        --retro-panel: rgba(30, 10, 60, 0.9);
        --retro-accent: #ff00cc; /* neon pink */
        --retro-accent2: #00ffff; /* neon cyan */
        --retro-text: #ffff66; /* yellowish neon */
        --retro-border: #ff6600; /* bright orange */
    }

    /* Background with animated gradient stripes */
    html, body {
        background: linear-gradient(135deg, #0b001a 25%, #1a0033 25%, #1a0033 50%, #0b001a 50%, #0b001a 75%, #1a0033 75%, #1a0033);
        background-size: 40px 40px;
        animation: retroStripes 3s linear infinite;
        color: var(--retro-text) !important;
        font-family: "Press Start 2P", monospace, sans-serif !important;
        text-shadow: 0 0 5px var(--retro-accent), 0 0 10px var(--retro-accent2);
    }

    @keyframes retroStripes {
        from { background-position: 0 0; }
        to { background-position: 40px 40px; }
    }

    /* Panels (navbar, cards, etc.) */
    .navbar, .content, .game-card, .profile-header, .rbx-upgrade-now {
        background: var(--retro-panel) !important;
        border: 3px solid var(--retro-border);
        border-radius: 0px; /* retro = blocky */
        box-shadow: 0 0 12px var(--retro-accent), 0 0 24px var(--retro-accent2);
    }

    /* Retro glowing links & buttons */
    a, button {
        color: var(--retro-text) !important;
        text-shadow: 0 0 8px var(--retro-accent2), 0 0 16px var(--retro-accent);
        transition: all 0.2s ease-in-out;
        font-weight: bold;
    }
    a:hover, button:hover {
        color: var(--retro-accent2) !important;
        text-shadow: 0 0 10px var(--retro-accent), 0 0 20px var(--retro-accent2);
        transform: scale(1.05);
    }

    /* Sidebar (left navigation) */
    .left-col, .navigation, .rbx-left-col, #navigation, .navbar-left {
        background: var(--retro-panel) !important;
        border-right: 3px solid var(--retro-border) !important;
        box-shadow: 4px 0 12px var(--retro-accent);
    }

    .left-col a, .navigation a, .rbx-left-col a, #navigation a {
        display: block;
        padding: 6px 12px; /* reduced spacing */
        font-family: "Press Start 2P", monospace, sans-serif !important;
        color: var(--retro-text) !important;
        text-shadow: 0 0 5px var(--retro-accent), 0 0 12px var(--retro-accent2);
        transition: all 0.2s ease-in-out;
    }

    .left-col a:hover, .navigation a:hover, .rbx-left-col a:hover, #navigation a:hover {
        background: var(--retro-accent) !important;
        color: #000 !important;
        text-shadow: none;
        transform: translateX(4px);
    }

    /* Sidebar section headers */
    .left-col .section, .navigation .section {
        font-size: 11px;
        text-transform: uppercase;
        letter-spacing: 1px;
        color: var(--retro-accent2) !important;
        border-bottom: 2px solid var(--retro-border);
        margin-bottom: 8px;
        padding: 6px;
    }

    /* Scrollbar */
    ::-webkit-scrollbar {
        width: 14px;
        height: 14px;
    }
    ::-webkit-scrollbar-thumb {
        background: var(--retro-accent);
        border: 2px solid var(--retro-border);
    }
    ::-webkit-scrollbar-track {
        background: #1a0033;
    }

    /* Fix warning bar if it appears */
    .alert.alert-warning {
        display: none !important;
    }
}
