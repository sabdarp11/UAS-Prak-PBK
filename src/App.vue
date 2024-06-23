<template>
  <q-layout view="hHh lpR fFf" class="app-layout">
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-btn flat dense @click="$router.push('/')" class="back-home-btn">
          BACK HOME
        </q-btn>
        <q-toolbar-title class="text-center">
          PROJECT UAS PRAKTIKUM PBK
        </q-toolbar-title>
      </q-toolbar>
    </q-header>
    
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'App'
};
</script>

<style scoped>
.app-layout {
  height: 100vh;
  background-image: url('@/assets/bmwm4.jpg');
  background-size: cover;
  background-position: center;
  position: relative;
}

.bg-primary {
  background-color: #ff0d8e;
}

.q-layout-content:before {
  content: '';
  background: rgba(0, 0, 0, 0.5);
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

.text-center {
  text-align: center;
}

.back-home-btn {
  color: #000000;
  border-color: #ffffff;
  border-width: 2px;
  margin-right: 10px;
  padding: 8px 16px;
  border-radius: 4px;
}

.back-home-btn:hover {
  background-color: rgba(0, 0, 0, 0.361);
}
</style>
