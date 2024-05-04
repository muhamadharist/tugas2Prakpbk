<template>
  <div>
    <!-- 1. Beberapa elemen HTML yang berbeda -->
    <h1>Welcome!!</h1>

    <!-- 2. Elemen input teks -->
    <input v-model="inputText" placeholder="Masukkan teks di sini" />

    <!-- 3. Penggunaan class bindings dan style bindings -->
    <div :class="{ 'highlighted': isHighlighted }" :style="{ color: textColor }">
      Teks ini akan berubah warna ketika klik ubah saya.
    </div>

    <!-- 4. Interaksi dinamis dengan event listener -->
    <button @click="changeText">Ubah Teks</button>
    <p>{{ dynamicText }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
      isHighlighted: false,
      textColor: 'red',
      dynamicText: 'Teks ini akan berubah!',
    };
  },
  methods: {
    changeText() {
      this.dynamicText = 'Teks berhasil diubah!';
      this.isHighlighted = !this.isHighlighted;
    },
  },
};
</script>

<style scoped>
.highlighted {
  background-color: yellow;
}
</style>
