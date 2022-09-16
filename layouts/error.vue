<template>
  <div class="text-center">
    <div class="min-h-screen flex items-center justify-center">
      <div class="flex flex-col">
        <h1 class="text-3xl">Mohon Maaf Ada Kesalahan !</h1>
        <h2 class="text-2xl" v-if="error.statusCode === 404">Halaman Tidak Ditemukan</h2>
        <h2 class="text-2xl" v-else>Terjadi Kesalahan Pada Server</h2>
        <nuxt-link to="/" class="btn__error">kembali Ke Beranda</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["error"],
  layout: "erro_layout"
};
</script>
