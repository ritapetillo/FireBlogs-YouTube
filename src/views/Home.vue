<template>
  <div class="home">
    <BlogPost :post="welcomeScreen" />
    <BlogPost
      v-for="(post, index) in sampleBlogPosts"
      :key="index"
      :post="post"
    />
    <div class="blog-card-wrap">
      <div class="container">
        <h3>View More Recent Blogs</h3>
        <div class="blog-cards">
          <BlogCard v-for="(post, index) in sampleBlogCards" :key="index" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BlogPost from "../components/BlogPost.vue";
import BlogCard from "../components/BlogCard.vue";
export default {
  name: "Home",
  components: {
    BlogPost,
    BlogCard,
  },
  data() {
    return {
      welcomeScreen: {
        title: "Welcome Screen!",
        blogPost:
          "Weekly blog articles with all things programming including HTML, CSS, JavaScript and more. Register today to never miss a post!",
        welcomeScreen: true,
        photo: "coding",
      },
      sampleBlogPosts: [
        {
          blogTitle: "Welcome!",
          blogHTML:
            "Weekly blog articles with all things programming including HTML, CSS, JavaScript and more. Register today to never miss a post!",
          blogCoverPhoto: "beautiful-stories",
        },
        {
          blogTitle: "Welcome!",
          blogHTML:
            "Weekly blog articles with all things programming including HTML, CSS, JavaScript and more. Register today to never miss a post!",
          blogCoverPhoto: "coding",
        },
      ],
      sampleBlogCards: [1, 2],
    };
  },
};
</script>
<style lang="scss">
.blog-card-wrap {
  h3 {
    font-weight: 300;
    font-size: 28px;
    margin-bottom: 32px;
  }
}
</style>
