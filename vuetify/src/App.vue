<template>
  <div>
    <v-app-bar color="deep-purple accent-4" dense dark>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Page title</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-menu left bottom>
        <template v-slot:activator="{ on, attrs }">
          <v-btn icon v-bind="attrs" v-on="on">
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item v-for="n in 5" :key="n" @click="() => {}">
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
    <v-main>
      <v-row>
      <VueCard :item="articles[0]"/>
      <VueCard/>
      </v-row>
    </v-main>
  </div>
</template>

<script>
import VueCard from "./components/VueCard.vue"

export default {
  data: () => ({
    collapseOnScroll: true,
    articles: [{"source":{"id":"ars-technica","name":"Ars Technica"},"author":"Doug Johnson","title":"We don’t know why, but being in space causes us to destroy our blood - Ars Technica","description":"Space anemia is tied to being in the void and can stick around awhile.","url":"https://arstechnica.com/science/2022/01/we-dont-know-why-but-being-in-space-causes-us-to-destroy-our-blood/","urlToImage":"https://cdn.arstechnica.net/wp-content/uploads/2022/01/image-1-760x380.jpeg","publishedAt":"2022-01-14T16:00:46Z","content":"42 with 25 posters participating\r\nSpace isnt easy on humans. Some aspects are avoidablethe vacuum, of course, and the cold, as well as some of the radiation. Astronauts can also lose bone density, th… [+3452 chars]"}]
  }),
  components: {
    VueCard,
  }
};
</script>
