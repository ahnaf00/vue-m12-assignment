<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { toast } from 'vue3-toastify';
import 'vue3-toastify/dist/index.css';

import Dialog from 'primevue/dialog';
import Button from 'primevue/button';

const notify = () => {
      toast("Wow so easy !", {
        autoClose: 1000,
      }); // ToastOptions
    }
  // return { notify };



import { ref } from "vue";

const visible = ref(false);
</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12 ">
        <div>
          <!-- <button class="btn btn-primary" @click="notify">Toast Message</button> -->
          <Button label="Toast Message" icon="pi pi-external-link" @click="notify" />
        </div>
      </div>
    </div>
  </div>








  <div class="card flex justify-content-center">
      <Button label="Alert Dialogue" icon="pi pi-external-link" @click="visible = true" />
      <Dialog v-model:visible="visible" modal header="Header" :style="{ width: '50vw' }">
          <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
              Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
          </p>
      </Dialog>
  </div>






</template>

<style scoped>

</style>
