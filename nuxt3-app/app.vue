<template>
  <div>
    <!-- Remove this component to get started! -->
      Page visits: {{ data }}
    <NuxtWelcome />
</div>
</template>

<script lang="ts">
export default {
  async setup() {

    const { data } = await useAsyncData('count', () => $fetch('/api/counter'))


    return {
      data
    }
  }
}
</script>