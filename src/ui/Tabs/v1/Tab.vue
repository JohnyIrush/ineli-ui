<template>
  <div class="tab-content" v-show="title == selectedTitle">
      <slot />
  </div>
</template>

<script>
import { inject } from '@vue/runtime-core'
export default {
    props: ['title'],
    setup(props, {slots})
    {
        const selectedTitle = inject("selectedTitle")

        return {
            selectedTitle
        }
    }
}
</script>

<style>
.tab-content
{
    min-height: 400px;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 3px 5px rgba(0, 0, 0, 0.5);
}
</style>