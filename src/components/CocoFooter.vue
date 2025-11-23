<template>
  <footer class="main-footer">
    <div class="container">
      
      <section class="payment-methods">
        <h4>Гарантирано сигурно плащане с:</h4>
        <div class="payment-icons">
            <img loading="lazy" src="https://cocosolis.com/bg/wp-content/uploads/icon-payments-visa.svg" alt="Visa">
            <img loading="lazy" src="https://cocosolis.com/bg/wp-content/uploads/icon-payments-mastercard.svg" alt="Mastercard">
            <img loading="lazy" src="https://cocosolis.com/bg/wp-content/uploads/icon-payments-discover.svg" alt="Discover">
            <img loading="lazy" src="https://cocosolis.com/bg/wp-content/uploads/icon-payments-paypal.svg" alt="PayPal">
            <img loading="lazy" src="https://cocosolis.com/bg/wp-content/uploads/icon-payments-amex.svg" alt="Amex">
            <img loading="lazy" src="https://cocosolis.com/bg/wp-content/uploads/icon-payments-gpay.svg" alt="Google Pay">
            <img loading="lazy" src="https://cocosolis.com/bg/wp-content/uploads/icon-payments-apple-pay.svg" alt="Apple Pay">
        </div>
      </section>

      <div class="footer-grid">
        
        <section class="menu-column">
          <h5>Полезни връзки</h5>
          <nav>
            <ul>
              <li><a href="https://cocosolis.com/bg/store/">Продукти</a></li>
              <li><a href="https://cocosolis.com/bg/loyalty/">CLUB</a></li>
              <li><a href="https://cocosolis.com/bg/contacts/">Контакти</a></li>
              <li><a href="https://cocosolis.com/bg/about-us/">За нас</a></li>
              <li><a href="https://cocosolis.com/bg/terms-of-sale/">Правила за закупуване</a></li>
              <li><a href="https://cocosolis.com/bg/terms-of-use/">Условия за ползване на сайта</a></li>
              <li><a href="https://cocosolis.com/bg/terms-of-use/loyalty-terms/">Условия на Програма за лоялност</a></li>
              <li><a href="https://cocosolis.com/bg/cookies/">Политика за бисквитки</a></li>
              <li><a href="https://cocosolis.com/bg/return-policy/">Политика за връщане</a></li>
              <li><a href="https://cocosolis.com/bg/delivery/">Поръчка и доставка</a></li>
              <li><a href="https://cocosolis.com/bg/privacy-policy/">Политика за защита на лични данни</a></li>
            </ul>
          </nav>
        </section>

        <section class="newsletter-column">
          <form class="newsletter-form" @submit.prevent>
            <p class="newsletter-cta">
              <strong>Нека бъдем приятели!</strong> Абонирайте се, за да бъдете сред първите, които ще научат за нашите нови продукти и промоции.
            </p>
            <fieldset>
              <div class="input-group">
                <input type="email" name="email" placeholder="Вашият имейл" required>
              </div>
              
              <div class="checkbox-group">
                <input type="checkbox" id="consent" name="consent">
                <label for="consent">
                  Съгласен/на съм предоставеният от мен имейл да бъде използван, за да получавам известия за новости, подаръци и бъдещи промоции, свързани с продуктите COCOSOLIS, съгласно <a href="/bg/terms-of-use/">Общи условия</a> на уебсайта и <a href="/bg/privacy-policy/">Политиката за поверителност</a>.
                </label>
              </div>

              <button type="submit" class="btn-submit">Влезте в клуба</button>
            </fieldset>
          </form>
        </section>

        <section class="social-column">
          <h5>Последвайте ни</h5>
          <ul class="social-icons">
            <li>
              <a href="https://www.facebook.com/cocosolisbg/" target="_blank" rel="nofollow">
                <img src="https://cocosolis.com/bg/wp-content/uploads/icon-social-media-facebook-footer-v0401.svg" alt="Facebook" loading="lazy">
              </a>
            </li>
            <li>
              <a href="https://www.instagram.com/cocosolis.official/" target="_blank" rel="nofollow">
                <img src="https://cocosolis.com/bg/wp-content/uploads/icon-social-media-instagram-footer-v0401.svg" alt="Instagram" loading="lazy">
              </a>
            </li>
            <li>
              <a href="https://www.tiktok.com/@cocosolisofficial" target="_blank" rel="nofollow">
                <img src="https://cocosolis.com/bg/wp-content/uploads/icon-social-media-tik-tok-footer-v0401.svg" alt="TikTok" loading="lazy">
              </a>
            </li>
            <li>
              <a href="https://www.linkedin.com/company/cocosolis" target="_blank" rel="nofollow">
                <img src="https://cocosolis.com/bg/wp-content/uploads/icon-social-media-linkedin-footer-v0401.svg" alt="LinkedIn" loading="lazy">
              </a>
            </li>
          </ul>
          <p class="social-cta">
            Тагни ни и има шанс да видиш своята снимка или видео в профила ни! <strong>#cocosolis</strong>
          </p>
        </section>
      </div>

    <small class="copyright">
      © 2016 - 2025 COCOSOLIS | All rights reserved
    </small>
    </div>
  </footer>
</template>

<style scoped>
footer.main-footer {
  background: var(--c-text-main);
  color: #fff;
  padding: 3rem 1rem 1rem;
  font-family: sans-serif;
  font-size: 0.9rem;
  line-height: 1.5;
}

a {
  color: inherit;
  text-decoration: none;
  transition: opacity 0.2s;
}

a:hover {
  opacity: 0.8;
  text-decoration: underline;
}

h4, h5 {
  text-transform: uppercase;
  margin-bottom: 1rem;
  letter-spacing: 1px;
  font-weight: 600;
}

/* Payment Methods */
.payment-methods {
  text-align: center;
  margin-bottom: 3rem;
  padding-bottom: 2rem;
  border-bottom: 1px solid rgba(255,255,255, 0.1);
}

.payment-icons {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 1rem;
  margin-top: 1rem;
}

.payment-icons img {
  height: 35px;
  width: auto;
}

/* Grid Layout */
.footer-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 3rem;
  margin-bottom: 3rem;
}

/* Menu Section */
.menu-column ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.menu-column li {
  margin-bottom: 0.5rem;
}

/* Newsletter Section */
.newsletter-form fieldset {
  border: none;
  padding: 0;
  margin: 0;
}

.newsletter-cta {
  margin-bottom: 1rem;
}

.input-group input {
  width: 100%;
  padding: 12px;
  border: 1px solid #fff;
  background: transparent;
  color: var(--c-white);
  margin-bottom: 1rem;
  box-sizing: border-box;
}

.input-group input::placeholder {
  color: rgba(255,255,255, 0.7);
}

.checkbox-group {
  display: flex;
  align-items: flex-start;
  gap: 0.5rem;
  margin-bottom: 1.5rem;
  font-size: 0.8rem;
}

.checkbox-group input {
  margin-top: 4px;
}

.btn-submit {
  width: 100%;
  padding: 12px;
  background-color: var(--c-white);
  color: var(--c-text-main);
  border: none;
  font-weight: bold;
  text-transform: uppercase;
  cursor: pointer;
  transition: background-color 0.2s;
}

.btn-submit:hover {
  background-color: var(--c-gold);
}

/* Social Media Section */
.social-icons {
  display: flex;
  gap: 1rem;
  list-style: none;
  padding: 0;
  margin: 0 0 1rem 0;
}

.social-icons img {
  width: 30px;
  height: 30px;
}

.social-cta {
  font-size: 0.85rem;
  opacity: 0.9;
}

/* Copyright */
.copyright {
  display: block;
  width: 100%;
  text-align: center;
  border-top: 1px solid rgba(255,255,255, 0.1);
  padding-top: 1.5rem;
  font-size: 0.8rem;
  opacity: 0.7;
}

/* Responsive Footer */
@media (max-width: 768px) {
  .payment-icons img {
    height: 28px;
  }
  
  .footer-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  
  .menu-column, .social-column, .newsletter-column {
    text-align: center;
  }

  .social-icons {
    justify-content: center;
  }
  
  .checkbox-group {
    text-align: left;
  }
}
</style>