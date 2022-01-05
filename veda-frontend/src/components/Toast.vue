<template>
  <div class="toast-wrapper">
    <div class="toast">{{ store.state.toastText }}</div>
  </div>
</template>

<script>
import { inject } from "vue";
export default {
  name: "Toast",
  setup() {
    const store = inject("store");
    return {
      store,
    };
  },
  mounted() {
    setTimeout(() => this.store.methods.triggerToast(), 2500);
  },
};
</script>

<style scoped>
.toast-wrapper {
  position: fixed;
  width: 100%;
  top: 85%;
}
.toast {
  padding: 12px;
  color: white;
  background: #a5a5a5;
  border-radius: 10px;
  box-shadow: 1px 3px 5px rgb(0 0 0 / 20%);
  max-width: fit-content;
  margin: 0 auto;
}
</style>
