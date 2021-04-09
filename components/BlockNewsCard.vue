<template>
  <div class="card_box">
    <div class="card">
      <img src="~assets/images/default/fashion-woman-girl-pullover-380x250.jpg" alt="" class="img-fluid">
    </div>
    <div class="card_overlay">
      <div class="card_icon"></div>
      <div class="card_info">
        <div class="card_category_text">
          <h6>
            <NuxtLink to="#">Lifestyle Picture</NuxtLink>
          </h6>
          <h3>
            <NuxtLink to="#">Ella Barton’s old tweets are exactly as hilarious as you think they’d be</NuxtLink>
          </h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BlockNewsCard"
}
</script>

<style scoped>
.card_box{
  position: relative;
}
.card_overlay{
  position: absolute;
  top: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.196);
  height: 100%;
}
</style>
