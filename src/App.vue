<script setup>
  import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav class="flex gap-[20px] py-[10px] px-[20px] bg-slate-300">
        <RouterLink class="hover:underline" to="/">Home</RouterLink>
        <RouterLink class="hover:underline" to="/products">products</RouterLink> 
        <RouterLink class="hover:underline" to="/cart">Cart</RouterLink> 
      </nav>
    </div>
  </header>

  <RouterView />
</template>

