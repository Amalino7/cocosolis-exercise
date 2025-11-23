<template>
  <div class="drawer-overlay" id="drawerOverlay"></div>

  <!-- Search Drawer -->
  <aside class="drawer-right" id="searchDrawer">
    <header class="drawer-header">
      <h2>Търсене</h2>
      <button class="close-drawer">&times;</button>
    </header>
    <search>
      <form class="search-input-group">
        <input type="search" placeholder="Какво търсите днес?">
        <button type="submit">GO</button>
      </form>
      <div class="search-suggestions">
        <p class="suggestion-label">Най-често търсени:</p>
        <div class="tags-container">
          <a href="#" class="tag">Масло за тен</a>
          <a href="#" class="tag">Кокос</a>
        </div>
      </div>
    </search>
  </aside>

  <!-- Shopping Cart Drawer -->
  <aside class="drawer-right" id="cartDrawer">
    <header class="drawer-header">
      <h2>Количка (2)</h2>
      <button class="close-drawer">&times;</button>
    </header>
    
    <div class="cart-items">
      <div class="cart-item">
        <img 
          src="https://images.unsplash.com/photo-1629198688000-71f23e745b6e?w=600&auto=format&fit=crop" 
          alt="Product"
          class="item-img"
        >
        <div class="item-details">
          <h4>Glow Shimmer Oil</h4>
          <p class="item-price">1 x 45.00 лв.</p>
        </div>
      </div>
    </div>

    <div class="cart-footer">
      <div class="cart-total">
        <span>Общо:</span>
        <span>45.00 лв.</span>
      </div>
      <button class="btn-add-prominent">Плащане</button>
    </div>
  </aside>
</template>

<style scoped>
/* --- Base Drawer Styles --- */
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
  right: max(-450px, -100vw);
  width: min(450px, 100vw);
  height: 100vh;
  background: var(--c-white);
  z-index: 1000;
  padding: 2rem;
  transition: right 0.4s cubic-bezier(0.25, 1, 0.5, 1);
  box-shadow: -5px 0 20px rgba(0, 0, 0, 0.1);
  display: flex;
  flex-direction: column;
}

.drawer-right.active {
  right: 0;
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

.close-drawer {
  background: none;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
  padding: 0.25rem;
  line-height: 1;
}

/* --- Cart Items --- */
.cart-items {
  flex-grow: 1;
  overflow-y: auto;
  padding-right: 0.5rem; 
}

.cart-item {
  display: flex;
  gap: 1rem;
  margin-bottom: 1.5rem;
  align-items: center;
}

.item-img {
  width: 70px;
  height: 70px;
  object-fit: cover;
  border-radius: 4px;
}

.item-details h4 {
  margin: 0 0 0.25rem 0;
  font-size: 0.95rem;
  line-height: 1.2;
}

.item-price {
  color: #888;
  font-size: 0.85rem;
  margin: 0;
}

/* --- Cart Footer --- */
.cart-footer {
  margin-top: auto;
  padding-top: 1rem;
  border-top: 1px solid #eee;
}

.cart-total {
  display: flex;
  justify-content: space-between;
  font-weight: bold;
  font-size: 1.2rem;
  margin-bottom: 1rem;
}

.btn-add-prominent {
  width: 100%;
  padding: 1rem;
  background-color: var(--c-text-main);
  color: #fff;
  border: none;
  font-weight: bold;
  text-transform: uppercase;
  cursor: pointer;
}

/* --- Search --- */
.search-input-group {
  display: flex;
  border: 2px solid var(--c-text-main);
  border-radius: 4px;
  overflow: hidden;
}

.search-input-group input {
  width: 100%;
  padding: 1rem;
  border: none;
  outline: none;
  font-size: 1rem;
}

.search-input-group button {
  padding: 0 1.5rem;
  background: var(--c-text-main);
  color: var(--c-white);
  font-weight: 600;
  border: none;
  cursor: pointer;
}

.search-suggestions {
  margin-top: 1.5rem;
}

.suggestion-label {
  color: #888;
  font-size: 0.9rem;
  margin-bottom: 0.5rem;
}

.tag {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: #f5f5f5;
  border-radius: 20px;
  font-size: 0.85rem;
  margin: 0.25rem 0.25rem 0.25rem 0;
  text-decoration: none;
  color: #333;
  transition: all 0.2s;
}

/* Mobile layout */
@media (max-width: 600px) {
.drawer-right{ 
    padding: 1.25rem;
 }
  .drawer-right.active {
    width: 100%;
  }

  .drawer-header {
    margin-bottom: 1.25rem;
    padding-bottom: 0.75rem;
  }

  .drawer-header h2 {
    font-size: 1.25rem;
  }

  .cart-item {
    gap: 0.75rem;
    margin-bottom: 1rem;
  }

  .item-img {
    width: 60px;
    height: 60px;
  }
  
  .item-details h4 {
    font-size: 0.9rem;
  }

  .search-input-group input {
    padding: 0.75rem;
    font-size: 0.95rem;
  }
  
  .search-input-group button {
    padding: 0 1rem;
  }
  
  .search-suggestions {
    margin-top: 1rem;
  }

  .cart-footer {
    padding-top: 0.75rem;
  }

  .cart-total {
    font-size: 1.1rem;
    margin-bottom: 0.75rem;
  }
  
  .btn-add-prominent {
    padding: 0.85rem;
  }
}
</style>