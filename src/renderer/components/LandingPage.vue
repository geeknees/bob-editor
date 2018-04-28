<template>
  <div id="wrapper">
    <main>
      <editor></editor>
    </main>
  </div>
</template>

<script>
  import Editor from './Editor'

  export default {
    name: 'landing-page',
    components: { Editor },
    methods: {
    }
  }
</script>

<style>

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  @font-face {
    font-family: 'SFZimmerman';
    src: url(../assets/SFZimmerman.ttf);
  }
  body { font-family: 'SFZimmerman', sans-serif; }

  #wrapper {
    height: 100vh;
    padding: 10px;
    width: 100vw;
  }

</style>
