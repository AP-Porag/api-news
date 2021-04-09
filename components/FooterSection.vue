<template>
<div class="footer">
  <div class="footer_top">
    <div class="container">
      <div class="row">
        <div class="col-md-5">
          <div class="brand_div">
            <h1>Api-News Logo</h1>
          </div>
          <div class="footer_about_text">
            <p class="footer_about_us_text">Entertainment and celebrity gossip magazine theme. Start writing, publishing, advertising and sharing in
              minutes with
              pre-defined options
              and layouts or start customizing and be surprised by our theme flexibility. More news, less hassle…</p>
          </div>
          <div class="social_link_list d-flex">
            <div class="follow_text">
              <p>Follow us:</p>
            </div>
            <div class="follow_link">
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
        <div class="col-md-7">
          <div class="row">
            <div class="col-md-4">
              <h3>About Api-News</h3>
              <div class="list_box">
                <ul>
                  <li>
                    <NuxtLink to="#" class="text-capitalize">contact us</NuxtLink>
                  </li>
                  <li>
                    <NuxtLink to="#" class="text-capitalize">About Us</NuxtLink>
                  </li>
                  <li>
                    <NuxtLink to="#" class="text-capitalize">Advertise</NuxtLink>
                  </li>
                </ul>
              </div>
            </div>
            <div class="col-md-4">
              <h3>Categories</h3>
              <div class="list_box">
                <ul>
                  <li
                  v-for="menu in menus"
                  :key="menu.title"
                  >
                    <NuxtLink :to="menu.link" class="text-capitalize">{{menu.title}}</NuxtLink>
                  </li>
                </ul>
              </div>
            </div>
            <div class="col-md-4">
              <h3>Our Partners</h3>
              <div class="list_box">
                <ul>
                  <li
                    v-for="partner in partners"
                    :key="partner.title"
                  >
                    {{partner.title}}
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="footer_bottom">
    <p class="text-center">© {{Date.now()}} - All rights reserved to Programmers Node.</p>
  </div>
</div>
</template>

<script>
export default {
  name: "FooterSection",
  data(){
    return{
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
      partners:[
        {
          title:'News Api'
        },
        {
          title:'Rapid Api'
        }
      ],
    }
  }
}
</script>

<style scoped>
.footer{
  background: #c10e55;
}
.footer_top{
  background: #db0a5b;
}
.footer_bottom{
  background: #c10e55;
}
</style>
