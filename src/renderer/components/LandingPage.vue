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
    background:
      radial-gradient(
        ellipse at top left,
        rgba(255, 255, 255, 1) 40%,
        rgba(229, 229, 229, .9) 100%
      );
    height: 100vh;
    padding: 60px 80px;
    width: 100vw;
  }

</style>
