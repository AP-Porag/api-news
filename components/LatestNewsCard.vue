<template>
  <div class="col-md-3">
    <div class="card">
      <div class="card-img">
        <NuxtLink to="#">
          <img src="~assets/images/default/red-school-blur-600x400.jpg" alt="" class="img-fluid" title="Did you know that all these celebs dropped out of college?">
        </NuxtLink>
      </div>
      <div class="card-header" id="card-header">
        <NuxtLink to="#" title="Did you know that all these celebs dropped out of college?" class="text-decoration-none">
          <h3 class="news_headline">Did you know that all these celebs dropped out of college?</h3>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LatestNewsCard"
}
</script>

<style scoped>
.card{
  border: none;
}
.card-img:hover #card-header .news_headline{
  color: #c10e55;
  transition: 0.4s;
}
.card-header{
  padding-left: 0px;
  padding-right: 0px;
  background-color: white;
}
.news_headline{
  font-size: 18px;
  font-weight: 500;
  color: #2b2b2b;
  text-decoration: none;
  transition: 0.4s;
}
.news_headline:hover{
  color: #c10e55;
  transition: 0.4s;
}
</style>
