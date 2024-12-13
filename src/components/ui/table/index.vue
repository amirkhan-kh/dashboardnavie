<template>
  <div class="table">
    <table>
      <thead>
        <tr class="tr">
          <th>Customer Name</th>
          <th>Company</th>
          <th>Phone Number</th>
          <th>Email</th>
          <th>Country</th>
          <th style="padding-left: 70px">Status</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="el in tableData" :key="el">
          <td>{{ el.name }}</td>
          <td>{{ el.compony }}</td>
          <td>{{ el.phone }}</td>
          <td>{{ el.email }}</td>
          <td>{{ el.country }}</td>
          <td>
            <n-popselect v-model:value="value" :options="options">
              <n-button>{{ value || 'Popselect' }}</n-button>
            </n-popselect>
          </td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup lang="ts">
import { tableData } from '../../../constants/index'
import { ref } from 'vue'
const value = ref('Active')
const options = [
  { label: 'Active', value: 'Inactive' },
  { label: 'Inactive', value: 'Active' },
]

const user = {
  status: 'Active',
}
</script>

<style lang="scss" scoped src="./_style.scss">
</style>
