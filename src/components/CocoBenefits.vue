<script setup>
const benefits = [
  {
    id: 1,
    title: 'Натурални и Био',
    text: 'Продуктите на COCOSОLIS са винаги натурални и създадени само с най-висококачествени био, студено пресовани масла.',
    icon: 'https://cocosolis.com/bg/wp-content/uploads/icon-leaf-regular-white.svg'
  },
  {
    id: 2,
    title: 'Създадени с любов',
    text: 'Създадени с любов и уважение към хората и природата. Нежни към кожата. Притежаващи аромат, в който ще се влюбите.',
    icon: 'https://cocosolis.com/bg/wp-content/uploads/icon-heart-solid-white.svg'
  },
  {
    id: 3,
    title: 'С отношение',
    text: 'Без наличие на парабени, оцветители, минерални и синтетични масла и разбира се, без тестване върху животни!',
    icon: 'https://cocosolis.com/bg/wp-content/uploads/icon-paw-solid-white.svg'
  }
];
</script>

<template>
  <section aria-labelledby="benefits-title" class="benefits-section">
    <h2 id="benefits-title" class="visually-hidden">Предимства</h2>

    <div class="benefits-grid">
      <ul class="benefits-list">
        <li v-for="item in benefits" :key="item.id" class="benefit-item">
          <div class="icon-wrapper">
            <img 
              :src="item.icon" 
              alt="" 
              loading="lazy" 
              class="benefit-icon"
            />
          </div>
          <div class="text-wrapper">
            <h3>{{ item.title }}</h3>
            <p>{{ item.text }}</p>
          </div>
        </li>
      </ul>

      <div class="benefits-image-container">
        <picture>
          <img 
            src="https://cocosolis.com/bg/wp-content/uploads/home-benefits-image.jpg" 
            alt="COCOSOLIS Benefits" 
            loading="lazy"
          >
        </picture>
      </div>
    </div>
  </section>
</template>

<style scoped>
.benefits-section {
  background-color: var(--color-bg-secondary);
  padding: 4rem 2rem;
  color: var(--c-white);
}

.benefits-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 3rem;
  max-width: 1200px;
  margin: 0 auto;
  align-items: center;
}

@media (min-width: 768px) {
  .benefits-grid {
    grid-template-columns: 1fr 1fr;
  }
}

.benefits-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 2.5rem;
}

.benefit-item {
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
}

.icon-wrapper {
  flex-shrink: 0;
  width: 50px;
}

.benefit-icon {
  width: 100%;
  height: auto;
  display: block;
}

.benefits-image-container img {
  width: 100%;
  height: auto;
  border-radius: 8px;
  display: block;
  object-fit: cover;
}
</style>