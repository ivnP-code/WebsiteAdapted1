<template>
  <div>
    <div class="grid-container">
      <div v-for="(article, index) in visibleArticles" :key="index" :class="index === 2 ? 'blogblue' : 'blog'">
        <img :src="article.foto" alt="pic">
        <h3>{{ article.title }}</h3>
        <div class="textblog" v-if="index !== 2">{{ article.intro }}</div>
        <div class="textblog" v-else>{{ article.intro }}</div>
        <button :class="index === 2 ? 'readmore2' : 'readmore'">Читать далее</button>
      </div>
    </div>

    <button v-if="visibleCount < articles.length" @click="loadMore" class="load-more-btn">Показать ещё</button>

    <div class="bottom">Все права защищены</div>
  </div>
</template>

<script>
export default {
  name: 'Blogs',
  data() {
    return {
      visibleCount: 5, 
      articles: [
        {
          foto: '/images/share-1200x630-a-1200x630-22326b97f383.jpg',
          title: 'Сравнение движков: Unreal Engine 4 vs Unity 5',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
        },
        {
          foto: '/images/360_F_534476686_228s1afY8iQB8kgeEVcSCFucn34yFqWi.jpg',
          title: '7 девушек айтишниц из фильмов и сериалов',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
        },
        {
          foto: '/images/9338e84172f76d9796f40c414eed6c59.jpg',
          title: 'Статья с синим фоном',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
        },
        {
          foto: '/images/360_F_314816591_yBAWvMvnpTW05AP0q4DCs5B6y2gnL9xA.jpg',
          title: '11 полезных инструментов для веб-разработчика',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
        },
        {
          foto: '/images/istockphoto-1439425791-612x612.jpg',
          title: 'Что такое Deep Learning? Как работает глубокое обучение?',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
        },
        {
        foto: '/images/bugatti-centodieci.jpg',
        title: 'Что такое Deep Learning? Как работает глубокое обучение?',
        intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
        },
        {
            foto: '/images/timon-klauser-3MAmj1ZKSZA-unsplash.jpg',
          title: 'Что такое Deep Learning? Как работает глубокое обучение?',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
          },{
                 foto: '/images/Red_Kitten_01.jpg',
          title: 'Что такое Deep Learning? Как работает глубокое обучение?',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
          },
          {
                 foto: '/images/leaves-with-droplets.jpg',
          title: 'Что такое Deep Learning? Как работает глубокое обучение?',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
          },
          {
                 foto: '/images/jpg_44-2.jpg',
          title: 'Что такое Deep Learning? Как работает глубокое обучение?',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
          },
          {     foto: '/images/Cat03.jpg',
          title: 'Что такое Deep Learning? Как работает глубокое обучение?',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
        },
        {
                 foto: '/images/sm_5afc4cd0dcaca.jpg',
          title: 'Что такое Deep Learning? Как работает глубокое обучение?',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
          },
          {     foto: '/images/share-1200x630-a-1200x630-22326b97f383.jpg',
          title: 'Что такое Deep Learning? Как работает глубокое обучение?',
          intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Laudantium necessitatibus...'
        }
      ]
    }
  },
  computed: {
    visibleArticles() {
      return this.articles.slice(0, this.visibleCount);
    }
  },
  methods: {
    loadMore() {
      this.visibleCount = Math.min(this.visibleCount + 2, this.articles.length);
    }
  }
}
</script>

<style>

.load-more-btn {
  margin: 20px auto;
  display: block;
  padding: 10px 20px;
  cursor: pointer;
  padding: 15px;
  color: rgb(255, 255, 255);
  background-color: rgb(187, 39, 39);
  border-radius: 5px;
  font-size: 18px;
  width: 200px;
  border: solid 1px rgb(187, 39, 39);
  margin-top: 20px;
  transition-duration: 1s;
}
.load:hover{
  background-color: rgb(117, 17, 17);
   border: solid 1px rgb(117, 17, 17);
  transition-duration: 1s;
}

</style>
