<template>
  <div class="container">
    <HeroText :title="'QR Code Generator'" :subTitle="'Insert a link or text below to generate a QR Code'"/>
    <LogicComponents :placeholder="'Insert link or text here...'" />
  </div>
  <FooterComponent/>
  
</template>

<script>
import HeroText from './components/HeroText.vue'
import LogicComponents from './components/LogicComponents.vue'
import FooterComponent from './components/FooterComponent.vue'

export default {
  name: 'App',
  components: {
    HeroText,
    LogicComponents,
    FooterComponent
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
  margin-top: 5%;
  min-height: 62.1vh;
}

</style>
