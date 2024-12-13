<template>
  <div class="wrapper">
    <Aside />
    <main>
      <Header />
      <section id="routing">
        <router-view></router-view>
      </section>
    </main>
  </div>
</template>

<script setup lang="ts">
import Aside from '../../components/navigation/index.vue'
import Header from '../../components/header/index.vue'
</script>

<style lang="scss" scoped src="./_style.scss">
</style>
