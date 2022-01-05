<template>
  <Toast v-if="store.state.showToast" />
  <div>this is Home page</div>
</template>
<script>
import { inject } from "vue";
import Toast from "../components/Toast.vue";
export default {
  name: "Login",
  setup() {
    const store = inject("store");
    return {
      store,
    };
  },
  components: {
    Toast,
  },
};
</script>
