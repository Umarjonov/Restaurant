<template>
  <nav class="flex fixed bg-white w-full gap-16 justify-between items-center border-b border-gray:50 z-30">
    <div class="pl-8">
      <NuxtLink to="/">
        <span>
          <img src="/logo/Restaurant.svg" class="w-28" alt="Restaurant logo">
        </span>
      </NuxtLink>
    </div>
    <div class="flex gap-5 flex-1">
      <div class="flex gap-2" style="width: 450px">
        <div class="flex flex-1 relative items-center border overflow-hidden rounded-xl">
          <div class="absolute left-3 text-base">
            <span class="Icon">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M11.5 19C15.6421 19 19 15.6421 19 11.5C19 7.35786 15.6421 4 11.5 4C7.35786 4 4 7.35786 4 11.5C4 15.6421 7.35786 19 11.5 19Z" fill="transparent" stroke="#1A1A18" stroke-linecap="round" stroke-linejoin="round"></path>
                <path d="M20 20L17 17" stroke="#1A1A18" stroke-linecap="round" stroke-linejoin="round"></path>
              </svg>
            </span>
          </div>
          <input type="text" class="px-10 py-3.5 w-full text-ellipsis focus:outline-none" placeholder="Заведение, блюдо, товар или кухня">
          <div class="absolute right-3 cursor-pointer" style="color: rgb(174, 174, 178);">
            <span class="Icon" data-inherit-color="true">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M12 2C6.49 2 2 6.49 2 12C2 17.51 6.49 22 12 22C17.51 22 22 17.51 22 12C22 6.49 17.51 2 12 2ZM15.36 14.3C15.65 14.59 15.65 15.07 15.36 15.36C15.21 15.51 15.02 15.58 14.83 15.58C14.64 15.58 14.45 15.51 14.3 15.36L12 13.06L9.7 15.36C9.55 15.51 9.36 15.58 9.17 15.58C8.98 15.58 8.79 15.51 8.64 15.36C8.35 15.07 8.35 14.59 8.64 14.3L10.94 12L8.64 9.7C8.35 9.41 8.35 8.93 8.64 8.64C8.93 8.35 9.41 8.35 9.7 8.64L12 10.94L14.3 8.64C14.59 8.35 15.07 8.35 15.36 8.64C15.65 8.93 15.65 9.41 15.36 9.7L13.06 12L15.36 14.3Z" fill="#1A1A18"></path>
              </svg>
            </span>
          </div>
        </div>
        <button id="btn_search" class="py-3.5 px-4 rounded-xl text-base font-semibold bg-yellow-400 hover:bg-yellow-500">Найти</button>
      </div>
      <div class="local w-30"></div>
    </div>
    <div class="flex justify-end">
      <div class="flex cursor-pointer flex-col justify-center items-center w-28 border">
        <Dropdown />
      </div>
      <div class="flex cursor-pointer flex-col justify-center items-center w-28 border">
        <span>
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M9.17129 21.4286H14.8284C19.5427 21.4286 21.4284 19.5428 21.4284 14.8286V9.17141C21.4284 4.45713 19.5427 2.57141 14.8284 2.57141H9.17129C4.457 2.57141 2.57129 4.45713 2.57129 9.17141V14.8286C2.57129 19.5428 4.457 21.4286 9.17129 21.4286Z" fill="transparent" stroke="#1A1A18" stroke-linecap="round" stroke-linejoin="round"></path>
            <path d="M8.99976 8H14.9998" stroke="#1A1A18" stroke-linecap="round" stroke-linejoin="round"></path>
            <path d="M8.99976 12H14.9998" stroke="#1A1A18" stroke-linecap="round" stroke-linejoin="round"></path>
            <path d="M8.99976 16H14.9998" stroke="#1A1A18" stroke-linecap="round" stroke-linejoin="round"></path>
          </svg>
        </span>
        <div>
          Заказы
        </div>
      </div>
      <div class="flex cursor-pointer flex-col justify-center items-center w-28 border active" id="profile">
        <span class="Icon_bm1tf" data-filled="true">
           <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M17.5259 20.658C16.7339 20.892 15.7979 21 14.6999 21H9.29988C8.20188 21 7.26588 20.892 6.47388 20.658C6.67188 18.318 9.07488 16.473 11.9999 16.473C14.9249 16.473 17.3279 18.318 17.5259 20.658Z" stroke="#1A1A18" stroke-linecap="round" stroke-linejoin="round"></path>
              <path d="M14.7 3H9.3C4.8 3 3 4.8 3 9.3V14.7C3 18.102 4.026 19.965 6.474 20.658C6.672 18.318 9.075 16.473 12 16.473C14.925 16.473 17.328 18.318 17.526 20.658C19.974 19.965 21 18.102 21 14.7V9.3C21 4.8 19.2 3 14.7 3ZM12 13.953C10.218 13.953 8.778 12.504 8.778 10.722C8.778 8.94002 10.218 7.5 12 7.5C13.782 7.5 15.222 8.94002 15.222 10.722C15.222 12.504 13.782 13.953 12 13.953Z" fill="transparent" stroke="#1A1A18" stroke-linecap="round" stroke-linejoin="round"></path>
              <path d="M15.2221 10.722C15.2221 12.504 13.7821 13.953 12.0001 13.953C10.2181 13.953 8.77808 12.504 8.77808 10.722C8.77808 8.94002 10.2181 7.5 12.0001 7.5C13.7821 7.5 15.2221 8.94002 15.2221 10.722Z" stroke="#1A1A18" stroke-linecap="round" stroke-linejoin="round"></path>
          </svg>
        </span>
        <div>
          Usulidin
        </div>
      </div>
    </div>
  </nav>
</template>
<script setup lang="ts">
</script>
<style scoped>
#profile.active svg path[stroke][fill] {
  fill: yellow;
}
.Icon[data-inherit-color] svg :not(path[stroke]) {
  fill: currentcolor;
}
</style>