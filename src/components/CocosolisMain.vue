<template>
    <main>
        <section class="hero">
            <div class="container hero-content">
                <h1>Натурален тен и сияйна кожа</h1>
                <p>Сега с до 30% отстъпка за всички продукти.</p>
                <button class="btn-add-prominent" style="width:auto; padding: 1rem 3rem;">Пазарувай</button>
            </div>
            <img src="https://images.unsplash.com/photo-1515688594390-b649af70d282?q=80&w=1000&auto=format&fit=crop"
                alt="Hero" role="presentation">
        </section>


        <!-- 2. FAVORITE PRODUCTS (Distinct Section Background) -->
        <CocoProducts
            :products="products"
            title="Любими Продукти"
            variant="rose"
            subtitle="Най-продаваните ни натурални масла"
            @show-more="onShowMore"
        />
        <CocoProducts
            title="ТЕН" 
            subtitle="Натурални, био масла за супер тен и сияйна кожа"
            variant="sage"
            :products="suntanProducts"
        />
        <CocoProducts
            title="КОСА" 
            subtitle="Натурални продукти за силна, гъста и бляскава коса"
            variant="white"
            :products="hairProducts"
        />

        <!-- 3. REVIEWS SECTION (Distinct Background, Headings & Avatars) -->
        <section class="section-reviews container">
            <!-- Heading Added -->
            <header class="section-header">
                <h2>Клиентите споделят</h2>
            </header>

            <div class="reviews-summary">
                <div class="rating-big">4.5</div>
                <div>
                    <div style="color: var(--c-gold); font-size: 1.2rem;">★★★★½</div>
                    <p style="color: #666;">36,979 отзива</p>
                </div>
            </div>

            <div class="review-grid">
                <article class="review-item">
                    <div class="review-header">
                        <!-- Placeholder Avatar -->
                        <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?w=100" alt=""
                            class="avatar">
                        <div>
                            <strong>Мария И.</strong>
                            <span style="color: green; font-size:0.8rem;">✓ Verified</span>
                        </div>
                    </div>
                    <div style="color:var(--c-gold)">★★★★★</div>
                    <h4 style="margin: 0.5rem 0;">Любимият ми продукт!</h4>
                    <p style="font-size: 0.9rem; color: #555;">Използвам го вече трето лято.</p>
                </article>

                <article class="review-item">
                    <div class="review-header">
                        <!-- Placeholder Avatar -->
                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=100" alt=""
                            class="avatar">
                        <div>
                            <strong>Петър Д.</strong>
                            <span style="color: green; font-size:0.8rem;">✓ Verified</span>
                        </div>
                    </div>
                    <div style="color:var(--c-gold)">★★★★☆</div>
                    <h4 style="margin: 0.5rem 0;">Страхотен аромат</h4>
                    <p style="font-size: 0.9rem; color: #555;">Мирише на истински шоколад!</p>
                </article>

                <article class="review-item">
                    <div class="review-header">
                        <!-- Placeholder Avatar -->
                        <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?w=100" alt=""
                            class="avatar">
                        <div>
                            <strong>Елена С.</strong>
                            <span style="color: green; font-size:0.8rem;">✓ Verified</span>
                        </div>
                    </div>
                    <div style="color:var(--c-gold)">★★★★★</div>
                    <h4 style="margin: 0.5rem 0;">Косата ми сияе</h4>
                    <p style="font-size: 0.9rem; color: #555;">Много съм доволна от маслото за коса.</p>
                </article>
            </div>
        </section>

        <!-- 4. NEWSLETTER (Fixed Button Leak) -->
        <section class="newsletter-section container">
            <h2 style="font-family: var(--font-heading); font-size: 2rem; margin-bottom: 1rem;">Нека бъдем приятели!
            </h2>
            <p>Абонирай се за ексклузивни оферти.</p>

            <form class="newsletter-form" action="/subscribe" method="POST">
                <label for="nl-email" class="visually-hidden">Имейл адрес</label>
                <input type="email" id="nl-email" placeholder="Вашият имейл адрес..." required>
                <button type="submit">Абонирай се</button>
            </form>
            <label style="display: block; margin-top: 1rem; font-size: 0.8rem;">
                <input type="checkbox" required> Съгласен съм с Политиката за поверителност
            </label>
        </section>

        <CocoBenefits/>

        <!-- CHARITY (Accent: Sage) -->
        <section class="charity-section">
                <!-- Placeholder for SOS logo -->
                <img src="https://cocosolis.com/bg/wp-content/themes/cocosolis/public/images/sos-detski-selishta-logo.49ca40.svg" alt="SOS Детски селища България" id="sos_partnership_logo" loading="lazy">
                <img src="https://cocosolis.com/bg/wp-content/themes/cocosolis/public/images/cocosolis-sos-detski-selishta-gold-partners-2024.5a74d4.svg" alt="Златен партньор на SOS Детски селища България за 2023 г." id="sos_partnership_goldenPartner" loading="lazy">
                <div class="charity-text">
                    <h3>SOS Детски селища България</h3>
                    <p>Даряваме 1 лв. от всеки закупен продукт в подкрепа на децата.</p>
                </div>
        </section>
    </main>
</template>

<script setup lang="js">
import CocoBenefits from './CocoBenefits.vue'
import CocoProducts from './CocoProducts.vue'
import { ref } from 'vue'

const products = ref([
    {
        badge: '-20%',
        image: 'https://images.unsplash.com/photo-1629198688000-71f23e745b6e?w=600&auto=format&fit=crop',
        title: 'Glow Shimmer Oil',
        desc: 'Озаряващо сухо масло за лице и тяло.',
        price: '45 лв.',
        oldPrice: '56 лв.',
        buttonText: 'Добави в количка'
    },
    {
        image: 'https://images.unsplash.com/photo-1629198688000-71f23e745b6e?w=600&auto=format&fit=crop',
        title: 'Aloha Suntan Oil',
        desc: 'За бърз, гладък и наситен тен на плажа.',
        price: '32 лв.',
        buttonText: 'Добави в количка'
    },
    {
        image: 'https://images.unsplash.com/photo-1629198688000-71f23e745b6e?w=600&auto=format&fit=crop',
        title: 'Choco Suntan Oil',
        desc: 'Неустоим аромат на шоколад.',
        price: '32 лв.',
        buttonText: 'Добави в количка'
    },
    {
        badge: 'NEW',
        image: 'https://images.unsplash.com/photo-1629198688000-71f23e745b6e?w=600&auto=format&fit=crop',
        title: 'Grow Hair Oil',
        desc: 'Заздравява и стимулира растежа.',
        price: '38 лв.',
        buttonText: 'Добави в количка'
    }
])

const suntanProducts = ref([
    {
        title: 'CHOCO Suntan & Body Oil',
        desc: 'За бърз, наситен тен и сияйна кожа. С неповторим аромат на шоколад.',
        price: '37,35 лв.',
        oldPrice: '45,00 лв.',
        badge: '-17%',
        image: 'https://placehold.co/400x400/png?text=CHOCO+Oil', // Replace with real asset
        href: '/product/choco-suntan-body-oil'
    },
    {
        title: 'ALOHA Suntan & Body Oil',
        desc: 'За бърз, наситен тен и сияйна кожа. С нежен кокосов аромат.',
        price: '37,35 лв.',
        oldPrice: '45,00 лв.',
        badge: '-17%',
        image: 'https://placehold.co/400x400/png?text=ALOHA+Oil',
        href: '/product/aloha-suntan-body-oil'
    },
    {
        title: 'MONOI Suntan & Body Oil',
        desc: 'За бърз, наситен тен и сияйна кожа. С моной от остров Таити.',
        price: '39,84 лв.',
        oldPrice: '48,00 лв.',
        badge: '-17%',
        image: 'https://placehold.co/400x400/png?text=MONOI+Oil',
        href: '/product/monoi-suntan-body-oil'
    },
    {
        title: 'GLOW Shimmer Oil',
        desc: 'Натурално озаряващо и овлажняващо масло с блестящи частици.',
        price: '44,20 лв.',
        oldPrice: '52,00 лв.',
        badge: '-15%',
        image: 'https://placehold.co/400x400/png?text=GLOW+Shimmer',
        href: '/product/glow-shimmer-oil'
    }
])

const hairProducts = ref([
    {
        title: 'GROW Hair Serum Spray',
        desc: 'Спрей серум за бърз растеж на косата. Намалява косопада.',
        price: '50,15 лв.',
        oldPrice: '59,00 лв.',
        badge: '-15%',
        image: 'https://placehold.co/400x400/png?text=GROW+Serum',
        href: '/product/grow-hair-serum'
    },
    {
        title: 'HAIR Oil Mask 3in1',
        desc: 'Натурално масло-маска 3в1 за интензивно подхранване и възстановяване.',
        price: '38,25 лв.',
        oldPrice: '45,00 лв.',
        badge: '-15%',
        image: 'https://placehold.co/400x400/png?text=HAIR+Mask',
        href: '/product/hair-oil-mask'
    },
    {
        title: 'GROW Shampoo',
        desc: 'Шампоан за растеж на косата с KERASCALP™. С антиейдж ефект.',
        price: '39,95 лв.',
        oldPrice: '47,00 лв.',
        badge: '-15%',
        image: 'https://placehold.co/400x400/png?text=GROW+Shampoo',
        href: '/product/grow-shampoo'
    }
])

function onShowMore() {
    // Example: append more items or navigate to products page
    // Here we simply log; replace with real behavior as needed.
    console.log('Show more clicked — load more products or navigate.')
}
</script>

<style scoped>
    /* Hero */
    .hero {
        background: #F2EFE9;
        height: 600px;
        display: flex;
        align-items: center;
        position: relative;
        overflow: hidden;
    }

    .hero img {
        position: absolute;
        right: 0;
        top: 0;
        height: 100%;
        width: 50%;
        object-fit: cover;
        object-position: center;
        mask-image: linear-gradient(to right, transparent, black 20%);
    }

    @media (max-width: 768px) {
        .hero-content {
            max-width: 100%!important;
        }
    }

    .hero-content {
        position: relative;
        z-index: 1;
        max-width: 50%;
        padding-left: 5%;
    }

    .hero-content h1 {
        font-family: var(--font-heading);
        font-size: 3.5rem;
        line-height: 1.1;
        margin-bottom: 1.5rem;
    }

    
    .section-header {
        text-align: center;
        margin-bottom: 3rem;
    }

    .section-header h2 {
        font-family: var(--font-heading);
        font-size: 2.5rem;
        margin-bottom: 0.5rem;
        color: var(--c-text-main);
    }

    /* Reviews */
    .section-reviews {
        background-color: var(--c-peach);
        padding: 5rem 0;
        width: 100%;
    }

    .reviews-summary {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 2rem;
        margin-bottom: 3rem;
    }

    .review-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 2rem;
        padding: 1rem;
    }

    .review-item {
        background: var(--c-white);
        padding: 2rem;
        border-radius: var(--radius-md);
        box-shadow: var(--shadow-card);
    }

    .review-header {
        display: flex;
        align-items: center;
        gap: 1rem;
        margin-bottom: 1rem;
    }

    .avatar {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        object-fit: cover;
        background: #eee;
    }

    .newsletter-section {
        background-color: var(--c-white);
        padding: 5rem 1rem;
        text-align: center;
    }
    @media (max-width: 1023px) {
        .newsletter-form{
            flex-direction: column;
        }

        .newsletter-form button {
            padding: 0.75rem 2rem !important;
        }
    }

    .newsletter-form {
        max-width: 500px;
        margin: 2rem auto 0;
        display: flex;
        gap: 0.5rem;
    }

    .newsletter-form input[type="email"] {
        flex: 1;
        padding: 1rem 1.2rem;
        border-radius: 50px;
        border: 1px solid #ddd;
        background: #f9f9f9;
    }

    .newsletter-form button {
        background: var(--c-text-main);
        color: var(--c-white);
        border-radius: 50px;
        padding: 0 2rem;
        font-weight: 600;
        white-space: nowrap;
    }

    .newsletter-form button:hover {
        background: var(--c-gold);
    }

    .charity-section {
        background-color: rgb(0,173,239);
        padding: 3rem 0;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
        gap: 2rem;
    }
    .charity-section img {
        height: 80px;
        width: auto;
    }

    /* .charity-images {
        display: flex;
        gap: 1rem;
    } */

    .charity-text h3 {
        font-family: var(--font-heading);  
    }
    .charity-text{
        padding: 0 1rem;
    }
</style>