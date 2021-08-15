<template>
  <div>
    <Users />
  </div>
</template>

<script>
import { defineComponent } from 'vue';
import Users from '@/components/Users.vue';

export default defineComponent({
  components: {Users},
  props: {
    mes: {
      type: String,
      require: true
    }
  }
})
</script>
