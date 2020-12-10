<template>
  <div class="about-container" id="about">
    <div class="ma-10">
      <h1 class="text-uppercase display-1 font-weight-bold ma-5" style="color: #19d3cc">
        Loyiha haqida
      </h1>
      <p class="mx-5 mt-15 headline" style="color: #3d3d3d">
        Ushbu ilova orqali siz endi o'z murojaatlarini onlayn tarzda yuborishingiz mumkin.
        Sizni qiynayotgan har qanday muammo endilikda bizning mutasaddi tashkilotlar
        tomonidan zudlik bilan, qisqa muddatda hal qilinadi. Siz o'z muammoingiz hal
        bo'lishi uchun uzoq navbatlar kutmaysiz, hech qanday ovoragarchiliklar sizni
        be'zovta qilmaydi. Faqatgina ilovani yuklab oling, rasmga oling va bizga yuboring!
      </p>
    </div>
    <div class="ma-15 d-flex justify-center">
      <img src="../assets/only.png" alt="pic" height="100%" width="100%" />
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped>
.about-container {
  width: 100%;
  background-color: #e5e5e5;
  display: grid;
  grid-template-columns: auto auto;
}

@media (max-width: 1000px) {
  .about-container {
    grid-template-columns: auto;
    grid-template-rows: auto auto;
    justify-content: center;
  }
}
</style>
