<template>
  <div>
    <div class="header">
      <myheader />
    </div>
    <div class="content1">
      <mycontent1 />
    </div>
    <div class="content2">
      <mycontent2 />
    </div>
    <div class="content3">
      <mycontent3 />
    </div>
    <div class="content4">
      <mycontent4 />
    </div>
  </div>
</template>

<script>
  import myheader from './components/MyHeader.vue'
  import mycontent1 from './components/MyContent1.vue'
  import mycontent2 from './components/MyContent2.vue'
  import mycontent3 from './components/MyContent3.vue'
  import mycontent4 from './components/MyContent4.vue'
  export default {
    name: 'App',
    components: {
      myheader,
      mycontent1,
      mycontent2,
      mycontent3,
      mycontent4,

    }
  }
</script>

<style>
  * {
    margin: 0%;
  }

  .header {
    background-image: url(./assets/home-banner@2x.jpg);
    background-size: 100% 100%;
    height: 300px;
  }

  .content1 {
    background-color: #e4e3e3;
    height: 720px;
  }

  .content2 {
    background-color: white;
    height: 650px;
  }

  .content3 {
    background-color: white;
    height: 500px;
    display: inline-block;
  }

  .content4 {
    background-color: aliceblue;
    height: 100px;
  }
</style>