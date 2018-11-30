<template>
  <section id="posts">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
      :excerpt="post.previewText"
      :thumbnail="post.thumbnailUrl"
      :id="post.id"
    />
  </section>
</template>

<script>
import PostPreview from '@/components/Blog/PostPreview'

export default {
  components: {
    PostPreview
  },
  data() {
    return {
      posts: [
        {
          title: 'How this all started',
          previewText: 'But I build robots',
          thumbnailUrl:
            'https://images.unsplash.com/photo-1483728642387-6c3bdd6c93e5?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=aecdd0f4ea59dfb2d0622cab6e3c3901&auto=format&fit=crop&w=755&q=80',
          id: 'post1'
        },
        {
          title: 'Post Botcamp',
          previewText: 'That was intense',
          thumbnailUrl:
            'https://images.unsplash.com/photo-1464983953574-0892a716854b?ixlib=rb-0.3.5&s=e6075ab276e38b517ed3e3f28801ff2a&auto=format&fit=crop&w=750&q=80',
          id: 'post2'
        },
        {
          title: 'Job Hunting frustration',
          previewText: 'Did you even read my resume',
          thumbnailUrl:
            'https://images.unsplash.com/photo-1473800447596-01729482b8eb?ixlib=rb-0.3.5&s=ac8f8b10cb586a94e1ecea3ae080a71e&auto=format&fit=crop&w=750&q=80',
          id: 'post3'
        },
        {
          title: 'Challenages ',
          previewText: 'freelancer ... attempt uno',
          thumbnailUrl:
            'https://images.unsplash.com/photo-1441936064713-d73d35f4fcb1?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=66eb239708b0d604000887eff0c61973&auto=format&fit=crop&w=693&q=80',
          id: 'post4'
        }
      ]
    }
  }
}
</script>

<style scoped>
#posts {
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  flex-wrap: wrap;
}

@media (min-width: 35rem) {
  #posts {
    flex-direction: row;
  }
}
</style>
