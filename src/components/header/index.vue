<template>
  <div>
    <header>
      <nav>
        <h1>Hello Evano 👋🏼,</h1>
        <form action="#">
          <i class="bi bi-search"></i>
          <n-auto-complete
            v-model:value="value"
            :input-props="{
              autocomplete: 'disabled',
            }"
            :options="options"
            placeholder="Search"
            clearable
          />
        </form>
      </nav>
    </header>
  </div>
</template>

<script setup lang="ts">
</script>

<style lang="scss" scoped src="./_style.scss">
</style>
