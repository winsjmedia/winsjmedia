<template>
  <div class="blog">
    <div class="blog__header">
      <p class="blog__title title">
        <span class="highlight">Blog</span>
        Posts
      </p>
      <p class="contact__description">
        I got my hands in a lot of different things and it's hard to put it down into any reasonable paragraph, so let me introduce you to my attempted solution:
        <br />
        <br />MY VERY INTERESTING BLOG
        <br />
        <br />Here you can read all about my adventures, strong opinions and sometimes even get a little sneak peak into my latest creative expression.
        <br />
        <br />I won't promise any scheduled content, but I'll do my best to post something every now and then.
      </p>
    </div>
    <div class="blog__articles articles">
      <div
        class="articles__article article"
        v-on:click="open(index)"
        v-for="(article, index) in articles"
        :key="index"
      >
        <img class="article__cover" :src="article.cover" alt />
        <p class="article__date">{{article.date}}</p>
        <p class="article__title title">
          <span class="highlight">{{getFirstWord(article.title)}}</span>
          {{getLastWords(article.title)}}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Blog",
  data: function () {
    return {
      articles: [
        {
          title: "Hello World",
          excerpt:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsum neque, amet nemo tempore ipsa quos, nostrum, placeat at molestias dignissimos earum unde consequuntur sed.",
          cover:
            "https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80",
          date: "08.04.2020",
        },
        {
          title: "Hello World",
          excerpt:
            "Lorem, ipsum dolor sit amet amet nemo tempore ipsa quos, nostrum, placeat at molestias dignissimos earum unde consequuntur sed.",
          cover:
            "https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80",
          date: "08.04.2020",
        },
        {
          title: "Hello World",
          excerpt: "Lorem, ipsum dolor sit amet consectetur adipisicir sed.",
          cover:
            "https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80",
          date: "08.04.2020",
        },
        {
          title: "Hello World",
          excerpt:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsum neque, amet nemo tempore ipsa quos",
          cover:
            "https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80",
          date: "08.04.2020",
        },
      ],
    };
  },
  methods: {
    open: function (index) {
      console.log(index);
    },
    getFirstWord: function (word) {
      return word.split(" ")[0];
    },
    getLastWords: function (word) {
      return word.split(" ").slice(1).join(" ");
    },
  },
};
</script>

<style scoped lang="scss">
.blog {
  padding: 0 2.5rem;
  &__articles {
    .article {
      margin-top: 5rem;
      -webkit-transition: all 1s ease;
      -moz-transition: all 1s ease;
      -o-transition: all 1s ease;
      -ms-transition: all 1s ease;
      transition: all 1s ease;
      &:hover {
        cursor: pointer;
        transform: scale(0.9);
      }
      &__cover {
        margin-bottom: 0.5rem;
        overflow: hidden;
        width: 100%;
      }
      &__date {
        font-size: 1.3rem;
      }
    }
  }
}
@media only screen and (min-width: 992px) {
  .blog {
    &__header {
      margin-bottom: 2.5rem;
      text-align: center;
    }
    &__articles {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      .article {
        width: calc(100% * (1 / 2) - 2.5rem);
        &__cover {
          width: 100%;
        }
      }
    }
  }
}
</style>