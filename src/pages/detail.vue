<template>
  <div>
    <h2>Email:</h2>
    <p>{{ email }}</p>
    <h2>PhoneNumber:</h2>
    <p>{{ PhoneNumber }}</p>
  </div>
</template>

<script>
import { computed } from 'vue';
import { useRoute } from 'vue-router/dist/vue-router.esm-bundler';
export default {
  name: 'Detail',
  setup() {
    const route = useRoute();
    const email = computed(() => route.params.email);
    const PhoneNumber = computed(() => route.params.phoneNumber);
    return {
      email,
      PhoneNumber,
    };
  },
  // data: () => ({
  //   device: [
  //     {
  //       Title: '',
  //       Processor: '',
  //       Photo: '',
  //       Price: '',
  //     },
  //   ],
  // }),
};
</script>
