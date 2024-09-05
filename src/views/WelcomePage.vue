<template>
  <div>
    <h1>{{ title }}</h1>
    <p v-if="isEnable">{{ subtitle  }}</p>
  </div>
</template>

<script>

export default({
  data() {
    return{
      title: "Vue入門",
      subtitle: "Vue練習",
      isEnable: true
    }
  },
})
</script>

