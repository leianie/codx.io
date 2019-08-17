<template>
  <div class="container">
    <div>
      <h1 class="title">
        <span :style="{ color: txtColor1 }">cod</span><span :style="{ color: txtColor2 }">x</span><span :style="{ color: txtColor3 }">.</span><span :style="{ color: txtColor4 }">io</span>
      </h1>
      <h5 class="subtitle">
        💻 soon. 🚀
      </h5>
      <!-- <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div> -->
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      txtColor1: '',
      txtColor2: '',
      txtColor3: '',
      txtColor4: '',
    }
  },
  created() {
    setTimeout(() => this.changeColor(), 1500)
  },
  methods: {
    changeColor() {
      this.txtColor1 = '#0059bb'
      this.txtColor2 = '#0059bb'
      this.txtColor3 = '#0059bb'
      this.txtColor4 = '#0059bb'
      setTimeout(()=> {
        this.txtColor2 = '#1287d9'
        this.txtColor3 = '#f0e53c' 
        this.txtColor4 = '#cf335f'
      }, 500)
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
  font-family: 'Comfortaa';
  display: block;
  font-weight: 300;
  font-size: 80px;
  color: #181e25;
  letter-spacing: 1px;
}

.title span {
  transition: color 0.5s ease;
}

.subtitle {
  font-family: 'Comfortaa';
  font-weight: 300;
  /* font-size: 42px; */
  color: #222b35;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
