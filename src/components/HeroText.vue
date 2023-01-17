<template>
  <div class="hero">
    <h1>{{ title }}</h1>
    <h2>{{ subTitle }}</h2>
  </div>
</template>
  
<script>
export default {
  name: 'HeroText',
  props: {
      title: String,
      subTitle: String
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&display=swap');

  .hero {
    text-align: center;
    color: white;
    font-family: 'Roboto', sans-serif;
  }

  h1 {
    font-weight: bold;
    padding: 10px;
  }

  h2 {
    font-style: italic;
  }
</style>
  