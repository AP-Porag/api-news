<template>
  <div class="col-md-6">
    <div class="card">
      <div class="card-header">
        <div class="card_title">
          <h3 class="card_title_h3">
            <NuxtLink :to="'/news/'+news.title.replace(/[^a-zA-Z ]/g, '').replace(/\s*$/g, '').replace(/\s+/g, '-')" class="text-decoration-none card_link">
              {{news.title.substring(0,120)+'...'}}
<!--              making slug-->
<!--              {{news.title.replace(/[^a-zA-Z ]/g, '').replace(/\s*$/g, '').replace(/\s+/g, '-')}}-->
            </NuxtLink>
          </h3>
        </div>
        <div class="card_news_info d-flex justify-content-between">
          <div class="author_Published_date">
            <span>
              {{news.author }} |
            </span>
            <span>
            {{ new Date(news.publishedAt).toLocaleDateString("sq-AL", {year: 'numeric', month: '2-digit', day: '2-digit'})}}
          </span>
          </div>
          <div class="news_views">
<!--            <h6>{{news.source.name}}</h6>-->
          </div>
        </div>
      </div>
      <div class="card-body p-0">
        <img :src="news.urlToImage" alt="" class="img-fluid" style="max-height: 197px; width: 100%">
      </div>
      <div class="card-footer">
        <div class="card_summary">
          <p>{{news.description.substring(0,120)+'...'}}</p>
        </div>
        <div class="card_link d-flex justify-content-between">
          <div class="card_news_link">
            <NuxtLink to="#">Read More</NuxtLink>
          </div>
          <div class="sharing_link">
            <ul class="list-inline">
              <li class="list-inline-item">
                <a href="#" target="_blank" title="facebook-news-api">
                  <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'facebook' }"/>
                </a>
              </li>
              <li class="list-inline-item">
                <a href="#" target="_blank" title="twitter-news-api">
                  <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'twitter' }"/>
                </a>
              </li>
              <li class="list-inline-item">
                <a href="#" target="_blank" title="instagram-news-api">
                  <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'instagram' }"/>
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ExclusiveNewsSection",
  props:['news'],
  slug:'',
}
</script>

<style scoped>
.card_title_h3, .card_link{
  font-size: 20px;
  font-weight: 500;
  color: #2b2b2b;
  text-transform: capitalize;
}
</style>
