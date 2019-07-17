<template>
  <div class="container">
    <div>
      <div class="inline" v-for="n in kanpaiCount">
        <logo />
      </div>
      <div class="links">
        <button class="kanpaiButton" @click="kanpai">乾杯する！</button>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },

  data() {
    return {
      kanpaiCount : 1,
    }
  },

  methods: {
    kanpai: function () {
      console.log('kanpai');
      this.kanpaiCount++;
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.inline {
  display: inline-block;
}
.kanpaiButton {
  font-size : 40px;
}
</style>
