<script setup lang="ts">
import ProductCard from '@/components/card/ProductCard.vue';
import { useRouter } from 'vue-router';

const router = useRouter();

const LogOut = () => {
  // Clear Token in Local Storage
  localStorage.clear()

  setTimeout(() => {
    // Redirect to Sign in Page After 1 sec
    router.push("/auth/sign-in")
  }, 1000)
}

</script>

<template>
  <header>
    <div class="nav-links">
      <div class="logo-img">
        <img src="https://scontent-los2-1.xx.fbcdn.net/v/t39.30808-6/247164088_106107808529896_3909532067585029766_n.png?_nc_cat=105&ccb=1-7&_nc_sid=09cbfe&_nc_ohc=CXXhyYmRdw0AX-869nl&_nc_ht=scontent-los2-1.xx&oh=00_AfCLHn-gzBKmsRj_dAmlEbgID2UIwQS-tMMM8oAcscx5sg&oe=641A74ED" alt="altschool logo">
      </div>
      <h2> Altschool Africa</h2>
      <button :onclick="LogOut">Logout</button>
    </div>
  </header>
  <section class="product__grid">
    <ProductCard msg="Real-estate" />
    <ProductCard msg="Real-estate" />
    <ProductCard msg="Real-estate" />
    <ProductCard msg="Real-estate" />
    <ProductCard msg="Real-estate" />
    <ProductCard msg="Real-estate" />
    <ProductCard msg="Real-estate" />
    <ProductCard msg="Real-estate" />
    <ProductCard msg="Real-estate" />
  </section>
</template>

<style lang="scss" scoped>
header {
  width: 100%;
  color: white;
  background-color: #212569;

  .nav-links {
    max-width: 90%;
    margin: 0 auto;
    padding: 1em 0;
    display: flex;
    align-items: center;
    justify-content: space-between;

    button {
      width: auto !important;
      background-color: white;
      color: #212569;
      border-radius: 2px;
      padding: .8em 2em !important;
    }
  }
}

  .logo-img {
    width: 120px;
    height: 50px;
    margin: 0 1rem 0 0;
  }

  .logo-img img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
.product__grid {
  max-width: 90%;
  margin: 0 auto;
  padding: 2em 0;
  display: grid;
  gap: 20px;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));

  @media (max-width: 800px) {
    grid-template-columns: repeat(2, 1fr)
  }

  @media (max-width: 600px) {
    max-width: 85%;
    grid-template-columns: repeat(1, 1fr)
  }
}
</style>

