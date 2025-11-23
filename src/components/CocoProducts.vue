<template>
    <section :class="['section-products', `section-${variant}`]">
        <div class="container">
            <header class="section-header">
                <h2>{{ title }}</h2>
                <p v-if="subtitle">{{ subtitle }}</p>
            </header>

            <div class="product-grid">
                <article v-for="(p, i) in products" :key="i" class="product-card">
                    <span v-if="p.badge" class="card-badge">{{ p.badge }}</span>
                    <a :href="p.href || '#'" class="card-image">
                        <img :src="p.image" :alt="p.title">
                    </a>
                    <div class="card-details">
                        <h3 class="card-title">{{ p.title }}</h3>
                        <p class="card-desc">{{ p.desc }}</p>
                        <div class="price-group">
                            <span>{{ p.price }}</span>
                            <span v-if="p.oldPrice" class="price-old">{{ p.oldPrice }}</span>
                        </div>
                        <button class="btn-add-prominent">{{ p.buttonText || 'Добави в количка' }}</button>
                    </div>
                </article>
            </div>

            <div class="show-more-wrap">
                <button class="btn-show-more" @click="$emit('show-more')">Покажи още</button>
            </div>
        </div>
    </section>
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
    products: {
        type: Array,
        default: () => []
    },
    title: {
        type: String,
        default: 'Любими Продукти'
    },
    subtitle: {
        type: String,
        default: ''
    },
    // New prop to control background color
    variant: {
        type: String,
        default: 'sage', // Options: 'sage', 'white', 'rose'
        validator: (value) => ['sage', 'white', 'rose'].includes(value)
    }
})
</script>

<style scoped>
.section-products {
    padding: 5rem 0;
    width: 100%;
    transition: background-color 0.3s ease;
}


.section-sage {
    background-color: var(--c-sage);
}

.section-white {
    background-color: var(--c-white);
}

.section-rose {
    background-color: var(--c-rose); 
}

.section-header {
    text-align: center;
    margin-bottom: 3rem;
}

.section-header h2 {
    font-family: var(--font-heading, sans-serif);
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
    color: var(--c-text-main);
}


.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 2rem;
}

@media (min-width: 1000px) {
    .product-grid {
        grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
    }
}




.product-card {
    background: var(--c-bg);
    border-radius: var(--radius-md);
    overflow: hidden;
    position: relative;
    display: flex;
    flex-direction: column;
    box-shadow:  var(--shadow-card);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.product-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-hover);
}

.card-badge {
    position: absolute;
    top: 12px;
    left: 12px;
    background: var(--c-sale);
    color: var(--c-white);
    padding: 4px 10px;
    font-size: 0.75rem;
    font-weight: 700;
    border-radius: var(--radius-sm);
    z-index: 2;
}

.card-image {
    aspect-ratio: 1;
    overflow: hidden;
    background: var(--c-white);
    border-bottom: 1px solid #f0f0f0;
}

.card-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
}

.product-card:hover .card-image img {
    transform: scale(1.05);
}

.card-details {
    padding: 1.5rem;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
}

.card-title {
    font-size: 1.2rem;
    margin: 0 0 0.5rem 0;
    color: #333;
}

.card-desc {
    font-size: 0.9rem;
    color:  var(--c-text-light);
    margin-bottom: 1.2rem;
    line-height: 1.4;
}

.price-group {
    font-weight: 700;
    font-size: 1.1rem;
    margin-bottom: 1rem;
    color: #333;
}

.price-old {
    color: #aaa;
    font-size: 0.9rem;
    text-decoration: line-through;
    margin-left: 6px;
}

.show-more-wrap {
    display: flex;
    justify-content: center;
    margin-top: 2rem;
}

.btn-show-more {
    background: transparent;
    color: #333;
    border: 2px solid #333;
    padding: 0.6rem 1.25rem;
    border-radius: 999px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.2s;
}

.btn-show-more:hover {
    background: #333;
    color: #fff;
}
.btn-show-more:active {
    transform: scale(0.96);
}

</style>