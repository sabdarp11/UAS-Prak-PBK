<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="bg-primary text-white" height-hint="98">
      <q-toolbar class="toolbar-center">
        <q-toolbar-title class="toolbar-title-center">
          <q-avatar size="100px">
            <img src="@/assets/download.jpg" alt="Profile Picture">
          </q-avatar>
          <span class="title-text">UAS PRAKTIKUM PBK</span>
        </q-toolbar-title>
      </q-toolbar>

      <q-tabs align="right">
        <q-btn
          outline
          color="white"
          to="/tasks"
          label="TUGAS SABDA RP"
          class="task-button"
        />
      </q-tabs>
    </q-header>

    <q-page-container>
      <WeatherPage />
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import WeatherPage from '../pages/WeatherPage.vue'

export default {
  components: {
    WeatherPage
  }
}
</script>

<style lang="scss">
.bg-primary {
  background-color: #a5105b !important;
}

.text-white {
  color: #000000 !important;
}

.q-toolbar {
  padding: 0.5rem;
}

.toolbar-center {
  display: flex;
  justify-content: center;
}

.toolbar-title-center {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
}

.title-text {
  margin-left: 0.5rem;
  font-size: 1.5rem;
  font-weight: bold;
}

.task-button {
  font-size: 1.2rem;
  font-weight: bold;
}

.q-page-container {
  padding: 1rem;
}

.weather-page {
  padding: 2rem;
  border: 1px solid #ccc;
  border-radius: 0.5rem;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.q-avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
