<template>
  <dialog id="loginDialog">
    <div class="modal-content">
      <button class="close-modal" onclick="this.closest('dialog').close()">&times;</button>
      
      <h2 class="modal-title">Влезте в профила си</h2>

      <form method="dialog">
        <div class="form-group">
          <label for="email">Имейл адрес</label>
          <input type="email" id="email" placeholder="name@example.com">
        </div>
        
        <div class="form-group">
          <label for="pass">Парола</label>
          <input type="password" id="pass">
        </div>
        
        <div class="form-group form-actions">
          <label class="remember-me">
            <input type="checkbox"> Запомни ме
          </label>
          <a href="#" class="forgot-pass">Забравена парола?</a>
        </div>
        
        <button class="btn-add-prominent">Вход</button>
      </form>
      
      <footer class="modal-footer">
        <p>Нямате акаунт? <a href="#" class="register-link">Регистрация</a></p>
      </footer>
    </div>
  </dialog>
</template>

<style scoped>
/* --- Base Dialog Styles --- */
dialog {
  border: none;
  border-radius: var(--radius-md);
  padding: 0;
  box-shadow: var(--shadow-float);
  max-width: 500px;
  width: 90%;
  margin: auto;
  background:var(--c-bg);
}

dialog::backdrop {
  background: rgba(0, 0, 0, 0.6);
  backdrop-filter: blur(4px);
}

.modal-content {
  padding: 2.5rem;
  position: relative;
}

.close-modal {
  position: absolute;
  top: 1rem;
  right: 1rem;
  background: none;
  border: none;
  font-size: 1.5rem;
  padding: 0.5rem;
  cursor: pointer;
  line-height: 1;
  color: var(--c-text-light);
}

.modal-title {
  font-family: var(--font-heading, sans-serif);
  margin: 0 0 1.5rem 0;
  text-align: center;
  font-size: 1.75rem;
}

/* --- Form Elements --- */
.form-group {
  margin-bottom: 1.2rem;
}

.form-group label {
  display: block;
  font-size: 0.9rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
}

.form-group input:not([type="checkbox"]) {
  width: 100%;
  padding: 0.8rem;
  border: 1px solid #ddd;
  border-radius: var(--radius-sm, 4px);
  font-size: 1rem;
}

.form-group input:focus {
  border-color: var(--c-gold);
  outline: none;
}

/* --- Form Actions (Remember / Forgot) --- */
.form-actions {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.85rem;
  margin-bottom: 1.5rem;
}

.remember-me {
  font-weight: 400 !important;
  margin-bottom: 0 !important;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  cursor: pointer;
}

.remember-me input {
  width: auto !important;
}

.forgot-pass {
  color: var(--c-gold);
  text-decoration: none;
}

.modal-footer {
  text-align: center;
  margin-top: 1.5rem;
  font-size: 0.9rem;
  color: var( --c-text-light);
}

.register-link {
  font-weight: 600;
  text-decoration: underline;
  color: var(--c-text-main);
}

/* --- MOBILE OPTIMIZATIONS --- */
@media (max-width: 600px) {
  dialog {
    width: 95%;
  }

  .modal-content {
    padding: 1.5rem; 
  }

  .modal-title {
    font-size: 1.5rem;
    margin-bottom: 1.25rem;
  }

  .form-group {
    margin-bottom: 1rem;
  }

  .form-group input:not([type="checkbox"]) {
    padding: 0.75rem;
  }

  .btn-primary {
    padding: 0.85rem;
  }

  .close-modal {
    top: 0.5rem;
    right: 0.5rem;
  }
}
</style>