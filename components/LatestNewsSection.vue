<template>
  <div class="latest_news_section mt-4" id="latest_news_section">
    <div class="container">
      <div class="row latest_news_box">
        <LatestNewsCard
          v-for="card in 4"
          :key="card.title"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LatestNewsSection"
}
</script>

<style scoped>
.latest_news_box{
  border-bottom: 8px solid #2b2b2b;
}
</style>
