<template>
  <div class="home">
    <h1>Home</h1>
    <PostList :posts="posts" />
  </div>
</template>

<script>
import { ref } from "vue";
import PostList from "../components/PostList";
export default {
  components: { PostList },
  setup() {
    const posts = ref([
      {
        title:
          "2021 Sony Dünya Fotoğraf Ödülleri'nde Türkiye Ulusal Ödülü'nün Sahibi Belli Oldu",
        body:
          "Sony Türkiye, Dünya Fotoğraf Organizasyonu ile beraber 2021 Sony Dünya Fotoğraf Ödülleri Türkiye Ulusal Ödülü’nü Mehmet Aslan’ın kazandığını açıkladı.",
        id: 1,
      },
      {
        title:
          "Microsoft, Şubat Ayının İkinci Yarısı İçin Xbox Game Pass Oyunlarını Duyurdu",
        body:
          "Xbox Game Pass kullanıcılarının ücretsiz oynayabileceği içeriklere yenileri ekleniyor. 18 Şubat’tan itibaren Game Pass’e gelecek oyunlar PC ve konsol ortamında yayınlanacak.",
        id: 2,
      },
    ]);
    return { posts };
  },
};
</script>

<style>
</style>