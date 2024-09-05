<template>
  <div>
    <h1>{{ title }}</h1>
    <p v-if="isEnabled">{{ subtitle  }}</p>
    <button @dblclick="toggle">トグル</button>
  </div>
</template>

<script>

export default({
  data() {
    return{
      title: "Vue入門",
      subtitle: "Vue練習",
      isEnabled: true
    }
  },
  methods: {
    toggle(){
      this.isEnabled = !this.isEnabled
    }
  }
})
</script>

