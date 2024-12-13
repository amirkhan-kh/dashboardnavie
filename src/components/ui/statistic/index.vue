<template>
  <div class="card">
    <div class="item" v-for="el in statistics" :key="el">
      <img :src="el.icon" :alt="el.title" />
      <div class="bio">
        <p>{{ el.title }}</p>
        <h2>{{ el.rating }}</h2>
        <span v-if="el.date"> <i class="bi bi-arrow-up-short"></i>{{ el.date }}</span>
        <span v-else>
          <img src="../../../icons/Ellipse 8.png" alt="" />
          <img src="../../../icons/Ellipse 8.png" alt="" />
          <img src="../../../icons/Ellipse 8.png" alt="" />
          <img src="../../../icons/Ellipse 8.png" alt="" />
        </span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { statistics } from '../../../constants/index'
</script>

<style lang="scss" scoped>
.card {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  background: #fff;
  border-radius: 20px;
  height: 130px;
  padding: 7px 20px;
  width: 100%;
  box-shadow: rgba(149, 157, 165, 0.1) 0px 4px 10px;
  margin-bottom: 10px;
  .item {
    display: flex;
    align-items: center;
    gap: 20px;
    img {
      margin-bottom: 10px;
      width: 60px;
      height: 60px;
      background: linear-gradient(#d3ffe7, #effff6);
      border-radius: 50%;
      padding: 15px;
    }
    .bio {
      flex-grow: 1;
      h2 {
        font-weight: 600;
        margin-bottom: 5px;
        font-size: 32px;
      }
      p {
        font-size: 12px;
        color: #999;
        font-weight: 400;
      }
      span {
        display: flex;
        align-items: center;
        gap: 2px;
        font-size: 12px;
        color: #000;
        font-weight: 500;
        i {
          color: red;
          font-size: 25px;
        }
        img {
          width: 20px;
          height: 20px;
          padding: 0;

          & + img {
            margin-left: -10px;
          }
        }
      }
    }
  }
}
</style>
