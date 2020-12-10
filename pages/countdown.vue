/* eslint-disable prettier/prettier */
<template id="template">
  <div id="container">
    <h1 id="title">{{ days }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      time: '',
      now: '',
      days: '',
      hours: '',
      interval: '',
    }
  },
  created() {
    this.startTimer()
  },
  methods: {
    startTimer() {
      this.time = new Date(2021, 1, 9, 12).getTime()
      this.interval = setInterval(
        function () {
          this.now = new Date().getTime()
          const distance = this.time - this.now
          this.days = Math.floor(distance / (1000 * 60 * 60 * 24))
        }.bind(this),
        1000
      )
    },
  },
}
</script>

<style scoped>
#template {
  overflow: hidden;
}

#container {
  width: 80vw;
  height: 80;
  text-align: center;
}

@media screen and (min-width: 600px) {
  #title {
    margin-top: 300px;
  }
}
@media screen and (max-width: 600px) {
  #title {
    margin-top: 50px;
  }
}
</style>
