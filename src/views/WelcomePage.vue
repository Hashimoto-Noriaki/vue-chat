<template>
  <div>
    <h1>{{ title }}</h1>
    <TestComponent :isEnabled = "isEnabled" message="コンポーネントにデータが渡されています"/>
  </div>
</template>

<script>
import TestComponent from '@/components/TestComponent.vue';

export default({
  components: {
    TestComponent
  },
  data() {
    return{
      title: "Vue入門",
      subtitle: "Vue練習",
      isEnabled: true
    }
  },
  computed: {
    text(){
      if(this.isEnabled){
        return "ハロー"
      } else {
        return "きゃー"
      }
    }
  },
  methods: {
    toggle(){
      this.isEnabled = !this.isEnabled
    }
  }
})
</script>

