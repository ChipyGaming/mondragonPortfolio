<template>
<div>


<section id="home" class="w3l-banner py-5">
    <div class="container">
        <div class="row align-items-center">
        </div>
    </div>
</section>



<div id = "blog" class="anchor"></div>
<section>
  <div class="container">
    <div>
        <h5 class="title-small text-center">Blog</h5>
        <h3 class="title-big text-center mb-sm-5 mb-4">Updates On My Projects</h3>
        <nav class="navbar navbar-expand-lg stroke">
      <nuxt-link v-for="post in posts" :key="post.date" :to="{ path: '/Blog',hash: post.title}" class="nav-link">{{post.title}}</nuxt-link>
        </nav>
      <Loader v-if="$fetchState.pending" />
      <div v-else>
        <post-item v-for="post in posts" :key="post.date" :post="post" />
      </div>
    </div>
  </div>
</section>


</div>
</template>



<script>
import data from '~/static/api/data.json'
import PostItem from '@/components/PostItemBlog.vue';
import Loader from '@/components/Loader.vue';
import axios from "axios";

export default {
    components:{
        Loader,
        PostItem
    },
    
    name:"index",
    data(){
        return {
            data:data,
            posts: [],
        };
    },
  async fetch() {
    const { data: posts } = await axios.get(
      "https://public-api.wordpress.com/rest/v1.1/sites/imchipy.wordpress.com/posts"
    );
    this.posts = posts.posts;
    },
    

    head() {
      return {
        title: 'Home : '+this.data.main.name,
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'My custom description'
          }
        ]
      }
    }
}
</script>