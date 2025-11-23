<template>
    <header class="site-header">
        <aside class="top-bar" role="alert" aria-live="polite">
            <div class="marquee" aria-hidden="false">
                <div class="marquee-track" aria-hidden="false">
                    <span class="message">Black Friday 🤍 До 30% отстъпка в целия сайт 🤍 ПРОМО ПАКЕТИТЕ са най-добрите оферти! </span>
                    <span class="message" aria-hidden="true">Black Friday 🤍 До 30% отстъпка в целия сайт 🤍 ПРОМО ПАКЕТИТЕ са най-добрите оферти!</span>
                    <span class="message" aria-hidden="true">Black Friday 🤍 До 30% отстъпка в целия сайт 🤍 ПРОМО ПАКЕТИТЕ са най-добрите оферти!</span>
                </div>
            </div>
        </aside>

        <div class="container header-inner">
            <div class="header-left mobile-only">
                <button class="icon-btn" id="extraBtn" aria-label="Меню">
                    <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M4 6h16M4 12h16M4 18h16" />
                    </svg>
                </button>
                <button class="icon-btn" id="searchBtnMobile" aria-label="Търсене">
                    <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
                    </svg>
                </button>
            </div>

            <div class="logo-wrapper">
                <a href="/" class="logo" aria-label="Начална страница">COCOSOLIS</a>
            </div>

            <nav class="desktop-only" role="navigation" aria-label="Вторична навигация">
                <ul class="top-nav-list">
                    <li><a href="#">Начало</a></li>
                    <li><a href="#">Продукти</a></li>
                    <li><a href="#">CLUB</a></li>
                    <li><a href="#">За нас</a></li>
                    <li><a href="#">Контакти</a></li>
                    <li class="nav-item-dropdown">
                        <a href="#" class="more-trigger">Още</a>
                        <ul class="sub-menu">
                            <li><a href="#">Условия за ползване</a></li>
                            <li><a href="#">Правила за закупуване</a></li>
                            <li><a href="#">Поръчка и доставка</a></li>
                            <li><a href="#">Политика за лични данни</a></li>
                        </ul>
                    </li>
                </ul>
            </nav>

            <div class="header-actions">
                <button class="icon-btn desktop-only" id="searchBtn" aria-label="Търсене">
                    <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
                    </svg>
                </button>

                <button class="icon-btn" id="cartBtn" aria-label="Количка">
                    <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
                    </svg>
                </button>
                <button class="icon-btn" onclick="document.getElementById('loginDialog').showModal()" aria-label="Профил">
                    <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M20 21v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2" />
                        <circle cx="12" cy="7" r="4" />
                    </svg>
                </button>
            </div>
        </div>

        <nav class="main-nav container" aria-label="Основна навигация">
            <ul>
                <li><a href="#">Промо Пакети</a></li>
                <li><a href="#">Кожа</a></li>
                <li><a href="#">Коса</a></li>
                <li><a href="#">Лице</a></li>
                <li><a href="#">Автобронзанти</a></li>
                <li><a href="#">Тен</a></li>
                <li><a href="#">SPF</a></li>
            </ul>
        </nav>

    </header>

    <!-- Mobile drawer -->
    <aside class="mobile-only">
        <nav class="drawer-right" id="extraDrawer">
            <div class="drawer-header">
                <h2 class="drawer-title">Меню</h2>
                <button class="icon-btn close-drawer">
                    <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </button>
            </div>

            <div class="drawer-content">
                <div class="drawer-section">
                    <ul class="drawer-list secondary">
                        <li><a href="#">Начало</a></li>
                        <li><a href="#">CLUB</a></li>
                        <li><a href="#">За нас</a></li>
                        <li><a href="#">Контакти</a></li>
                    </ul>
                </div>

                <div class="drawer-section">
                    <details>
                        <summary>Полезна информация</summary>
                        <ul class="drawer-list sm-text">
                            <li><a href="#">Условия за ползване</a></li>
                            <li><a href="#">Правила за закупуване</a></li>
                            <li><a href="#">Поръчка и доставка</a></li>
                            <li><a href="#">Политика за лични данни</a></li>
                        </ul>
                    </details>
                </div>
            </div>
        </nav>
    </aside>

</template>

<style scoped>

/* --- Common Base Styles --- */
.site-header {
    background: var(--c-white);
    position: sticky;
    top: 0;
    z-index: var(--z-header);
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
}


.top-bar {
    background: var(--c-text-main);
    color: var(--c-white);
    text-align: center;
    padding: 0.5rem;
    font-size: 0.75rem;
    font-weight: 600;
    overflow: hidden;
    position: relative;
}

.logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--c-text-main);
    text-decoration: none;
    white-space: nowrap;
}

.icon-btn {
    background: transparent;
    border: none;
    cursor: pointer;
    width: 44px;
    height: 44px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--c-text-main);
}
.icon-btn:hover { color: var(--c-gold); }

.header-actions { display: flex; gap: 0.5rem; }

/* Marquee */
.marquee {
	display: block;
	width: 100%;
	overflow: hidden;
}

.marquee-track {
	display: inline-flex;
	align-items: center;
	white-space: nowrap;
	width: max-content;
	animation: marquee 10s linear infinite;
	will-change: transform;
}

.marquee .message {
	display: inline-block;
    margin-left: 25%;
	padding-right: 2rem;
	flex: none;
	font-weight: 600;
}

.marquee:hover .marquee-track {
	animation-play-state: paused;
}

@media (prefers-reduced-motion: reduce) {
	.marquee .marquee-track { animation: none; }
}

@keyframes marquee {
	0%   { transform: translateX(0); }
	100% { transform: translateX(-58.5%); }
}

/* Mobile layout */
@media (max-width: 1023px) {
    .desktop-only {
        display: none !important;
    }

    .header-inner {
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 60px;
        position: relative;
    }

    .header-left {
        flex: 1;
        display: flex;
        justify-content: flex-start;
    }

    .logo-wrapper {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        text-align: center;
    }

    .header-actions {
        flex: 1;
        justify-content: flex-end;
    }

    /* DRAWER STYLES (Mobile Only) */
    .drawer-overlay {
        position: fixed;
        inset: 0;
        background: rgba(0, 0, 0, 0.5);
        opacity: 0;
        pointer-events: none;
        transition: opacity 0.3s;
        z-index: 900;
    }

    .drawer-overlay.active {
        opacity: 1;
        pointer-events: auto;
    }

    .drawer-right {
        position: fixed;
        top: 0;
        left: max(-100vw, -450px);
        width: min(450px, 100vw);
        height: 100vh;
        background: var(--c-white);
        z-index: 1000;
        padding: 2rem;
        transition: left 0.4s cubic-bezier(0.25, 1, 0.5, 1);
        box-shadow: -5px 0 20px rgba(0, 0, 0, 0.1);
        display: flex;
        flex-direction: column;
    }

    .drawer-right.active {
        left: 0;
    }

    /* --- Header --- */
    .drawer-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 2rem;
        padding-bottom: 1rem;
        border-bottom: 1px solid #eee;
    }

    .drawer-header h2 {
        margin: 0;
        font-size: 1.5rem;
    }
    

    .drawer-content {
        padding: 1.5rem;
        display: flex;
        flex-direction: column;
        gap: 2rem;
    }

    .drawer-section h3 {
        font-size: 0.8rem;
        text-transform: uppercase;
        color: var(--c-text-light);
        margin-bottom: 1rem;
        letter-spacing: 1px;
    }

    .drawer-list {
        list-style: none;
        padding: 0;
        margin: 0;
    }

    .drawer-list li {
        margin-bottom: 0.8rem;
    }

    .drawer-list a {
        text-decoration: none;
        color: var(--c-text-main);
        font-size: 1.1rem;
        font-weight: 500;
        display: block;
        transition: color 0.2s;
    }

    .drawer-list.secondary a {
        font-size: 1rem;
        font-weight: 400;
    }

    .drawer-list.sm-text a {
        font-size: 0.9rem;
        color: var(--c-text-light);
    }

    .drawer-list a:hover {
        color: var(--c-gold);
        padding-left: 5px;
    }

    /* Accordion for extra links */
    details summary {
        cursor: pointer;
        font-weight: 600;
        padding: 0.5rem 0;
        list-style: none;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    details summary::after {
        content: '+';
        font-weight: 300;
    }
    details[open] summary::after {
        content: '-';
    }
}

/* Desktop layout */
@media (min-width: 1024px) {
    .mobile-only {
        display: none !important;
    }

    .header-inner {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1rem 0;
    }

    .logo { font-size: 1.8rem; }

    .top-nav-list {
        display: flex;
        gap: 1.5rem;
        list-style: none;
        padding: 0;
        margin: 0 2rem;
    }
    .top-nav-list a {
        color: var(--c-text-light);
        font-weight: 500;
        text-decoration: none;
    }
    .top-nav-list a:hover { color: var(--c-gold); }

    /* Dropdown logic */
    .nav-item-dropdown { position: relative; z-index: 100; }
    .sub-menu {
        position: absolute; top: 100%; right: 0;
        background: white; box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        width: 200px; padding: 0.5rem 0; opacity: 0; visibility: hidden;
        transition: all 0.2s; list-style: none;
    }
    .nav-item-dropdown:hover .sub-menu { opacity: 1; visibility: visible; }
    .sub-menu a { display: block; padding: 0.5rem 1rem; color: #333; }
    .sub-menu a:hover { background: #f9f9f9; }

}

/* Main Bottom Nav */
    .main-nav {
        border-top: 1px solid #eee;
        background: white;
    }
    .main-nav ul {
        overflow-x: auto;
        padding: 0.8rem 0;
        display: flex;
        justify-content: space-around;
        align-items: center;
        gap: 2rem;
        list-style: none;
        margin: 0;
        scrollbar-width: none;
    }
    .main-nav a {
        white-space: nowrap;
        font-size: 0.9rem;
        font-weight: 700;
        text-transform: uppercase;
        letter-spacing: 1px;
        color: var(--c-text-main);
        text-decoration: none;
        position: relative;
    }
    .main-nav a::after {
        content: ''; position: absolute; bottom: -5px; left: 0; width: 0; height: 2px;
        background: var(--c-gold); transition: width 0.3s;
    }
    .main-nav a:hover::after { width: 100%; }
</style>