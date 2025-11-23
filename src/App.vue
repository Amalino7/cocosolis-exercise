<script setup lang="js">
import CoCoSolisHeader from './components/CocosolisHeader.vue';
import './assets/main.css';
import CocosolisMain from './components/CocosolisMain.vue';
import CocoFooter from './components/CocoFooter.vue';
import Drawers from './components/Drawers.vue';
import { onMounted } from 'vue';
import CocoDialog from './components/CocoDialog.vue';

onMounted(() => {
          const toggleDrawer = (id, isOpen) => {
              const drawer = document.getElementById(id);
              const overlay = document.getElementById('drawerOverlay');
              if (!drawer || !overlay) return;
              if (isOpen) {
                  drawer.classList.add('active');
                  overlay.classList.add('active');
              } else {
                  drawer.classList.remove('active');
                  overlay.classList.remove('active');
              }
          };

        // Search Drawer Triggers
        const searchBtn = document.getElementById('searchBtnMobile');
        if (searchBtn) searchBtn.addEventListener('click', () => toggleDrawer('searchDrawer', true));

        const searchBtn2 = document.getElementById('searchBtn');
        if (searchBtn) searchBtn2.addEventListener('click', () => toggleDrawer('searchDrawer', true));

        // Cart Drawer Triggers
        const cartBtn = document.getElementById('cartBtn');
        if (cartBtn) cartBtn.addEventListener('click', () => toggleDrawer('cartDrawer', true));
        
        const extraBtn = document.getElementById('extraBtn');
        if (extraBtn) extraBtn.addEventListener('click', () => toggleDrawer('extraDrawer', true));

        // Universal Close (Overlay & Close Buttons)
        const overlayEl = document.getElementById('drawerOverlay');
        if (overlayEl) overlayEl.addEventListener('click', () => {
            toggleDrawer('searchDrawer', false);
            toggleDrawer('cartDrawer', false);
        });

        document.querySelectorAll('.close-drawer').forEach(btn => {
            btn.addEventListener('click', function () {
                const drawer = this.closest('.drawer-right');
                if (drawer) toggleDrawer(drawer.id, false);
            });
        });

        // Close modal buttons
        document.querySelectorAll('.close-modal').forEach(btn => {
            btn.addEventListener('click', function () {
                const dlg = this.closest('dialog');
                if (dlg && typeof dlg.close === 'function') dlg.close();
            });
        });
      });
      
</script>

<template>
  <CoCoSolisHeader />
  <CocoDialog></CocoDialog>
  <Drawers></Drawers>
  <CocosolisMain/>
  <CocoFooter/>
</template>

<style>

       

</style>
