<template>
  <h1>{{ title }}</h1>
  <div>{{ msg.msg1 }}</div>
</template>

<script lang="ts">
import { computed, defineComponent, reactive } from 'vue'
export default defineComponent({
  name:'Setup1',

  /**
   * CompositionAPI setup
   * https://v3.vuejs.org/api/composition-api.html#setup
   */
  setup (props, context) {

    /**
     * ReactivityAPI reactive
     * https://v3.vuejs.org/api/basic-reactivity.html#reactive
     */
    const msg = reactive({ msg1:'bbb' })

    /**
     * ReactivityAPI computed
     * https://v3.vuejs.org/api/computed-watch-api.html#computed
     */
    const title = computed(()=>'This is an Setup1 page')

    return {
      msg,
      title
    }
  }
})
</script>
