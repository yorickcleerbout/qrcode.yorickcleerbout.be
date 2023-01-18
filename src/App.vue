<template>
  <div class="container">
    <HeroText :title="'QR Code Generator'" :subTitle="'Insert a link or text below to generate a QR Code'"/>
    <LogicComponents :placeholder="'Insert link or text here...'" />
  </div>
  
</template>

<script>
import HeroText from './components/HeroText.vue'
import LogicComponents from './components/LogicComponents.vue'

export default {
  name: 'App',
  components: {
    HeroText,
    LogicComponents
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: #3f3b49;
}

.container {
  margin-top: 6%;
}
</style>
