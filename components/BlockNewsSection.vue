<template>
  <div class="latest_news_section mt-4" id="latest_news_section">
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <BlockNewsCard/>
        </div>
        <div class="col-md-6">
          <div class="row">
            <div class="col-md-6">
              <BlockNewsCard/>
            </div>
            <div class="col-md-6">
              <div class="row">
                <div class="col-md-12">
                  <BlockNewsCard/>
                </div>
                <div class="col-md-12">
                  <BlockNewsCard/>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BlockNewsSection"
}
</script>

<style scoped>

</style>
