<script setup>
</script>

<template>
  <main>
    <h1 class="text-3xl text-center my-[50px]">Amazing Store</h1>
    
    <h2 class="text-2xl text-center">Contact info</h2>
    <div class="flex justify-center align-center">
      <form action="" class="flex flex-col gap-[20px] bg-slate-200 rounded-lg py-[30px] px-[20px] mt-[20px]">
        <div class="flex gap-3 items-center">
          <label for="">Name:</label>
          <input type="text">
        </div>
        <div class="flex gap-3 items-center">
          <label for="">Surname:</label>
          <input type="text">
        </div>
        <div class="flex gap-3 items-center">
          <label for="">Email:</label>
          <input type="text">
        </div>
        <div class="flex gap-3 items-center">
          <label for="">Phone:</label>
          <input type="text">
        </div>
        <input type="submit" class="bg-blue-500 text-white rounded-lg transition hover:bg-blue-400 hover:cursor-pointer">
      </form>
    </div>
  </main>
</template>
