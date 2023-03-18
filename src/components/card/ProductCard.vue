<template>
  <section class="property-card">
    <div class="image-wrapper">
      <img src="https://netstorage-legit.akamaized.net/images/vllkyt5iogeq5uhe1.jpg?imwidth=720" alt="beautiful villa"/>
    </div>
    <div class="details">
      <h3 class="title">Beautiful Villa with in VGC, Lekki</h3>
      <p class="description">This stunning villa boasts luxurious amenities in a safe and secure environment.</p>
      <div class="info">
        <div class="price">
          ₦20,000,000/night for 10 Yrs
        </div>
      </div>
    </div>
  </section>
</template>



<style scoped>
.property-card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  border-radius: 8px;
  overflow: hidden;
  max-width: 100%;
}

.image-wrapper {
  position: relative;
  height: 0;
  padding-bottom: 56.25%;
  /* 16:9 aspect ratio */
}

img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.details {
  padding: 20px;
}

.title {
  font-size: 20px;
  margin: 0 0 10px;
   color: #3e5661;
}

.description {
  font-size: 12px;
  margin: 0 0 10px;
}

.info {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.price {
  font-size: 17px;
  font-weight: bold;
  color: #212569;
 
}

.location {
  font-size: 14px;
}
</style>
