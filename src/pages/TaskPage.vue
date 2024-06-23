<template>
  <div class="q-pa-md" style="background-image: url('@/assets/pp2.jpg');">
    <q-page>
      <q-list bordered padding>
        <q-item
          v-for="taskNumber in 7"
          :key="taskNumber"
          clickable
          v-ripple
          @click="goToTask(taskNumber)"
          class="task-item"
        >
          <q-item-section avatar>
            <q-avatar icon="work" :color="getTaskColor(taskNumber)" />
          </q-item-section>
          <q-item-section>
            Tugas {{ taskNumber }}
          </q-item-section>
        </q-item>
      </q-list>
    </q-page>
  </div>
</template>

<script>
export default {
  methods: {
    goToTask(taskNumber) {
      const taskLinks = {
        1: "https://sabdarp-project-cv.vercel.app/", 
        2: "https://sabda-rp-223510062-t2-pbk.vercel.app/", 
        3: "https://tugas3-pbk-223510062-sabda-rp.vercel.app/", 
        4: "https://t4-prak-pbk-srp.vercel.app/", 
        5: "https://tugas-5-pbk-srp.vercel.app/", 
        6: "https://tugas-6-prak-pbk-mauve.vercel.app/", 
        7: "https://tugas-7-prak-pbk.vercel.app/" 
      };
      window.open(taskLinks[taskNumber], '_blank'); 
    },
    getTaskColor(taskNumber) {
      const colors = ['#ff0e9a', '#32a852', '#2c89a0', '#ffa800', '#b512f7', '#ff3c00', '#18a2b8'];
      return colors[taskNumber - 1];
    }
  }
};
</script>

<style scoped>
.q-pa-md {
  padding: 16px;
  background-size: cover;
  background-position: center;
}

.q-list {
  max-width: 400px;
  margin: 0 auto;
}

.task-item {
  background-color: #434152de;
  padding: 12px;
  border-radius: 8px;
  margin-bottom: 12px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.task-item:hover {
  background-color: rgba(255, 77, 172, 0.74);
}

.q-avatar {
  width: 36px;
  height: 36px;
  font-size: 20px;
}

.q-item-section {
  margin-left: 12px;
  line-height: 36px; 
}
</style>
