<template>
    <div class="container">
    <h2 id="bad_idea_title">Good ideas</h2>
      <div class="card" v-for="article of articles" :key="article.slug">
        <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }">
          <div class="card-body">
          <h4 class="card-title" id="card-title-dec">{{ article.title }}</h4>
          <!-- <div class="card-text">{{ article.description }}</div> -->
          </div>
        </NuxtLink>
      </div>
    </div>
</template>

<script>
  export default {
    async asyncData({ $content, params }) {
      try{
        const articles = await $content('articles', params.slug)
          .where({ tags: { $contains: 'gideas' } })
          .only(['title', 'description', 'slug'])
          .sortBy('createdAt', 'asc')
          .fetch()

        return {
          articles
        }
      } catch (err) {
        throw new Error(`Problem handling something: ${err}.`);    
    }
    }
  }
</script>

<style> 
  #bad_idea_title{
    margin-top: 20px;
    margin-bottom: 12px;
  }

  .card {
    margin-bottom: 20px;
  }
  .card-text {
    text-decoration: none;
  }
  .card-titile{
    display: inline-block;
    background: linear-gradient(transparent 90%, #00FFC3 90%);
  }
  #card-title-dec{
    display: inline-block;
    background: linear-gradient(transparent 90%, #00FFC3 90%);
  }
  #club_top_title{
    margin-bottom: 15px;
  }
</style>