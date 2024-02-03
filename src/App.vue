<template>
  <div id="app">
    <HelloWorld title="slot">
      <li v-for="obj in slotobjs" v-bind:key="obj.name">{{ obj.name }}({{ obj.mail }})</li>
    </HelloWorld>
  </div>
</template>

<script lang="ts">
import HelloWorld from "./components/HelloWorld.vue"

export default {
  name: "app",
  components: {
    HelloWorld,
  },
  data: function () {
    return {
      slotobjs: [
        { name: "Taro", mail: "taro@yamada" },
        { name: "Hanako", mail: "hanako@flower" },
        { name: "Sachiko", mail: "sachiko@happy" },
      ],
    }
  },
}
</script>
