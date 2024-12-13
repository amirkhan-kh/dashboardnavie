<template>
  <div class="card">
    <nav>
      <div class="title">
        <h2>All Customers</h2>
        <p>Active Members</p>
      </div>
      <form action="#">
        <n-auto-complete
          v-model:value="value"
          :input-props="{
            autocomplete: 'disabled',
          }"
          :options="options"
          placeholder="Search..."
          clearable
        />
        <n-tree-select
          :options="options"
          default-value="Short by : Newest"
          @update:value="handleUpdateValue"
        />
      </form>
    </nav>
    <!-- table -->
    <Table />
    <footer>
      <p>Showing data 1 to 8 of 256K entries</p>
      <n-pagination v-model:page="page" :page-count="100" />
    </footer>
  </div>
</template>

<script setup lang="ts">
import Table from '../table/index.vue'
import { ref } from 'vue'

const page = ref(2)
</script>

<style lang="scss" scoped src="./_style.scss"></style>
