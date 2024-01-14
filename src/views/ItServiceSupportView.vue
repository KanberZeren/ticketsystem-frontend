<template>
  <div class="ItServiceSupport">
    <div class="content">
      <div class="text-container">
        <h2>Herzlich willkommen beim IT Service Support</h2>
        <p>
          Unser engagiertes IT-Support-Team steht Ihnen zur Verfügung, um Ihnen bei allen technischen Herausforderungen zu helfen. Wir sind hier, um sicherzustellen, dass Ihre IT-Erfahrung reibungslos verläuft. <br><br>Bei Fragen können Sie uns unter folgender Nummer erreichen: +49 12345678910112
        </p>
      </div>
      <div class="image-container">
        <img src="@/assets/servicefoto.png" alt="IT Support Image">
      </div>
    </div>
  </div>
</template>

<style scoped>
.ItServiceSupport {
  text-align: center;
  padding-top: 10%;
  background: #96c1e2;
  color: #fff;
  min-height: 100vh;
}

.content {
  display: flex;
  justify-content: space-between;
  max-width: 800px;
  margin: 0 auto;
}

.text-container {
  flex: 1;
  text-align: left;
}

.image-container {
  flex: 1;
  text-align: right;
}

img {
  height: auto;
  width: 500px;

}
</style>
