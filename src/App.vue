<script>
import BaseHeader from './components/BaseHeader.vue';
import BaseMain from './components/BaseMain.vue';
import BaseFooter from './components/BaseFooter.vue';

export default {
  name: 'App',
  components: {
    BaseHeader,
    BaseMain,
    BaseFooter
  }
}
</script>

<template>

<BaseHeader/>
<BaseMain/>
<BaseFooter/>

</template>

<style scoped>

</style>
