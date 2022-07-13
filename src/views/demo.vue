<template>
  <div class="about">
    <van-button type="primary">主要按钮</van-button>

  </div>
</template>
<script>
import { onMounted, reactive, toRefs } from 'vue'
import { getFissionCourseList, getGetrequs } from "../utils/request";
export default {
  name: 'aboutUs',
  components: {

  },
  setup() {
    const state = reactive({
      init: async () => {
        await getFissionCourseList({ t35: "post" }).then((res) => {
          console.log(res);
        });
        await getGetrequs({ t35: "get" }).then((res) => {
          console.log(res);
        });
      }

    })
    onMounted(() => {
        state.init()
    })
    return {
      ...toRefs(state)
    }
  }

}
</script>