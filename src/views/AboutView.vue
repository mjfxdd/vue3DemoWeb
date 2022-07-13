<template>
  <div class="about">
    <h1>This is an about page</h1>
    <van-button type="primary">主要按钮</van-button>

  </div>
</template>
<script>
import { onMounted, reactive, toRefs } from 'vue'
export default {
  name:'aboutUs',
  components:{

  },
  setup(){
    const state = reactive({
      
    })
    onMounted(()=>{

    })
    return{
      ...toRefs(state)
    }
  }

}
</script>