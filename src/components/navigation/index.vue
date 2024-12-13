<template>
  <div>
    <aside>
      <div>
        <a class="logo" href="#"
          ><img src="../../icons/setting 1.png" alt="" />Dashboard <span>v.</span>
          <p>01</p></a
        >
        <ul class="list" v-if="navLinks.length">
          <li class="list-item" v-for="el in navLinks" :key="el">
            <router-link class="list-item-links" :to="el.path">
              <div class="list-item-links-title">
                <span v-html="el.icon"></span>
                {{ el.name }}
              </div>
              <img src="../../icons/chevron-right 2.png" alt="" />
            </router-link>
          </li>
        </ul>
      </div>
      <div class="notification">
        <div class="top">
          <h3>Upgrade to PRO to get access all Features!</h3>
          <n-button>Default</n-button>
        </div>
        <div class="bottom">
          <li>
            <img src="../../icons/Ellipse 8.png" alt="" />
            <h2>
              Evano <br />
              <span>Project Manager</span>
            </h2>
          </li>
          <img src="../../icons/chevron-right 2.png" alt="" />
        </div>
      </div>
    </aside>
  </div>
</template>

<script setup lang="ts">
import { navLinks } from '../../constants/index'
</script>

<style lang="scss" scoped src="./_style.scss">
</style>
