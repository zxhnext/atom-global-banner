<template>
  <div id="app">
    <AtomBanner :obj="config" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import { Component as AtomBanner } from '../packages/atom-global-banner';

export default defineComponent({
    name: 'App',
    components: {
        AtomBanner,
    },
    setup() {
        const component = ref('div');
        const config = ref({
            src: require('./banner.jpg'),
        })

        return {
            component,
            config
        }
    }
})
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
ul, ol {
  list-style: none;
}
</style>