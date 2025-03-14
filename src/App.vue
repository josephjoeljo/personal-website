<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue';
</script>

<template>
  <div class="main">
    <NavBar/>
  <RouterView />
  </div>
</template>

<style scoped>
.main {
	margin: 0;
	padding: 0;
	display: flex;
	width: 100%;
	height: 100%;
	flex-direction: column;
	background-color: var();
}

@media (min-width: 1024px) {
}
</style>
