<template>
<div class="container">
  <div class="row">
    {{news.title}}
  </div>
</div>
</template>

<script>
export default {
  name: "single-news-page",
  data(){
    return{
      news:[],
      slug:this.$route.params,
      API_KEY:'a2218caa8a904f239f3d9f111958b1f1',
      category:'entertainment',
      endpoint:'everything',
      country:'us',
      loading:false,
      url:'https://newsapi.org/v2/'
    }
  },
  computed:{
    searchedNews(){
      const slug = this.slug.id
      let url=this.url+this.endpoint+'?q='+slug+'&apiKey='+this.API_KEY
      fetch(url)
        .then(response => response.json())
        .then(result => {
          const newses = result.articles
          const newsesCount = newses.length
          console.log('News Array length => '+newsesCount)
          if (newsesCount > 1){
            const title = slug.toLowerCase()
              .replace(/ /g,'-')
              .replace(/[^\w-]+/g,'');

             let item = newses.find(news => news.title == title)
            this.news.push(item)
            console.log(this.news)

          }else if (newsesCount < 1) {
            console.log('news array length is 0')
          }else {
            this.news = newses
            console.log('printed from else'+this.news)
          }
        })
    }
  }
}
</script>

<style scoped>

</style>
