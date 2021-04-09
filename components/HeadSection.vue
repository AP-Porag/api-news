<template>
<div class="container">
  <div class="social_bar">
    <div class="row">
      <div class="col-md-6">
        <div class="social_link_list">
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
      <div class="col-md-6">
        <div class="social_link_list">
          <ul class="list-inline text-right">
            <li class="list-inline-item border-right border-secondary">
              <NuxtLink to="/about" class="mr-2">About Us</NuxtLink>
            </li>
            <li class="list-inline-item border-right border-secondary">
              <NuxtLink to="/advertise" class="mr-2">Advertise</NuxtLink>
            </li>
            <li class="list-inline-item">
              <NuxtLink to="/contact-us">Contact Us</NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
  <div class="brand_bar">
    <div class="row">
      <div class="col-md-4">
        <h3>Api-News Logo</h3>
      </div>
      <div class="col-md-8">
        <img src="~assets/images/default/ad_728-90-2.png" alt="api-news" width="100%">
      </div>
    </div>
  </div>
  <div class="navigation_bar mt-4">
    <nav class="navbar navbar-expand-lg navbar-light" style="background: #db0a5b;">
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item"
          v-for="menu in menus"
              :key="menu.title"
          >
            <NuxtLink class="nav-link text-uppercase text-white" :to="menu.link">
              {{menu.title}}
            </NuxtLink>
            <div class="dropdown-menu bg-dark"
            v-if="menu.submenus"
            >
              <ul class="">
                <li class=""
                v-for="submenu in menu.submenus"
                    :key="submenu.title"
                >
                  <NuxtLink class="nav-link text-uppercase text-white" :to="submenu.link">
                    {{submenu.title}}
                  </NuxtLink>
                </li>
              </ul>
            </div>
          </li>
        </ul>
        <div class="form-inline my-2 my-lg-0">
          <button
            class="btn btn-outline-light my-2 my-sm-0"
            @click="searchBar=!searchBar"
          >
            <font-awesome-icon icon="search"/>
          </button>
        </div>
      </div>
    </nav>
  </div>
  <div class="search_bar my-4"
  v-if="searchBar"
  >
    <h6 class="search_header text-center text-capitalize">Search here with topic and country</h6>
    <div class="row">
      <div class="col-md-5">
        <input type="text" class="form-control text-danger" placeholder="Topic">
      </div>
      <div class="col-md-5">
        <select class="form-control">
          <option disabled selected>Select country</option>
          <option>USA</option>
          <option>India</option>
          <option>Australia</option>
        </select>
      </div>
      <div class="col-md-2">
        <button class="btn btn-outline-danger btn-block my-2 my-sm-0">Search</button>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: "HeadSection",
  data(){
    return{
      searchBar:false,
      menus:[
        {
          title:'home',
          link:'/',
          submenus:[
            {
              title:'main home',
              link:'/main-home',
            }
          ]
        },
        {
          title:'celebrity news',
          link:'/celebrity-news',
          submenus:[
            {
              title:'main home',
              link:'/main-home',
            }
          ]
        },
        {
          title:'life style',
          link:'/life-style',
          submenus:[
            {
              title:'main home',
              link:'/main-home',
            }
          ]
        },
        {
          title:'style',
          link:'/style',
          submenus:[
            {
              title:'main home',
              link:'/main-home',
            }
          ]
        },
        {
          title:'picture gallery',
          link:'/picture-gallery',
          submenus:[
            {
              title:'main home',
              link:'/main-home',
            }
          ]
        },
        {
          title:'video gallery',
          link:'/video-gallery',
          submenus:[
            {
              title:'main home',
              link:'/main-home',
            }
          ]
        },
        {
          title:'features',
          link:'/features',
          submenus:[
            {
              title:'main home',
              link:'/main-home',
            }
          ]
        },
      ],
    }
  },
  methods:{

  }
}
</script>

<style scoped>
.search_bar{
  border: 1px solid #db0a5b;
  padding: 15px;
  border-radius: 5px;
}
.search_header{
  color: #db0a5b;
  margin-bottom: 15px;
}
.nav-item:hover .dropdown-menu{
  display: block;
}
</style>
