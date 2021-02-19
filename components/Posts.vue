<template>
  <div>
    <div class="posts overflow-scroll mb-24">
      <post v-for="post in posts" :key="post.id" :post="post.content" :user="post.user" :be-liked="post.beLiked" />
    </div>
  </div>
</template>

<script>
import Post from '~/components/Post.vue';

export default {
  components: {
    Post
  },
  data() {
    return {
      posts: [
        {
          user: {
            displayName: 'aki',
            photoURL: '/images/post0.jpg'
          },
          content: {
            text: '渋谷です',
            image: '/images/post1.jpg'
          },
          beLiked: true
        },
        {
          user: {
            displayName: 'test user',
            photoURL: '/images/post1.jpg'
          },
          content: {
            text: '新宿です',
            image: '/images/post0.jpg'
          },
          beLiked: false
        }
      ],
    }
  },
}
</script>
