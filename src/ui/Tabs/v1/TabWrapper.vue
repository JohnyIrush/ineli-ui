<template>
  <div class="tab">
      <ul class="tabs_header">
          <li v-for="title in tabTitles" 
          :key="title" 
          @click="selectedTitle = title"
          :class="{ selected: title == selectedTitle}"
          >
          {{title}}
          </li>
      </ul>
  </div>
  <slot />
</template>

<script>
import { provide, ref } from 'vue'
export default {
    setup(props, {slots})
    {
        const tabTitles = ref(slots.default().map((tab) => tab.props.title))

        const selectedTitle = ref(tabTitles.value[0])

        provide("selectedTitle",  selectedTitle)

        return {
            tabTitles,
            selectedTitle
        }
    }
}
</script>

<style scoped>
.tabs
{
    max-width: 400px;
    margin: 0 auto;
}

.tabs_header{
    margin-bottom: 10px;
    list-style: none;
    padding: 0;
    display: flex;
}

.tabs_header li {
    width: 80px;
    text-align: center;
    padding: 10px 20px;
    margin-right: 10px;
    background-color: #ddd;
    border-radius: 5px;
    cursor: pointer;
    transform: a.4s all ease-out;
}

.tabs_header li.selected{
    background-color: rgb(49, 49, 228);
}
</style>