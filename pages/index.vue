<template>
  <div class="main">
    <LatestNewsSection/>
    <BlockNewsSection/>
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <img src="~assets/images/default/ad_728-90-3.png" alt="" class="img-fluid" width="100%">
        </div>
      </div>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-md-8">
          <h4>Exclusive News</h4>
          <div class="exclusive_news_section">
            <div class="row">
              <LazyExclusiveNewsSection
                class="pb-4"
                v-for="(news,index) in articles"
                :key="index"
                :news="news"
                v-if="news.description != null"
              />
            </div>
          </div>
        </div>
        <div class="col-md-4"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      search:'',
      searchCountry:'',
      articles:[],
      API_KEY:'a2218caa8a904f239f3d9f111958b1f1',
      category:'entertainment',
      endpoint:'top-headlines',
      country:'us',
      loading:false,
      url:'https://newsapi.org/v2/'

    }
  },
  computed:{
    getArticles(){
      let url=this.url+this.endpoint+'?country='+this.country+'&category='+this.category+'&apiKey='+this.API_KEY;
      console.log('API URL => '+url)
      fetch(url)
        .then(response => response.json())
        .then(result => {
          console.log(result)
          this.articles = result.articles
        })

    },
  },
  methods:{

  }
}

</script>

<style>

</style>
