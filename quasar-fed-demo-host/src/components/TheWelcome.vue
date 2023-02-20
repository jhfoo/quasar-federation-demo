<script setup>
import WelcomeItem from './WelcomeItem.vue'
</script>

<template>
  <WelcomeItem>
    Vue’s<MyButton/>
  </WelcomeItem>
</template>

<script>
import { defineComponent } from 'vue'
const MyButton = defineAsyncComponent(() => import('remote_app/Button'));

export default defineComponent({
  name: 'TheWelcome',
  components: {
    MyButton,
  }
})
</script>