<script>
import BaseHeader from './components/BaseHeader.vue';
import BaseMain from './components/BaseMain.vue';
import BaseFooter from './components/BaseFooter.vue';
import comicsList from './data/comics';

export default {
  name: 'App',
  components: {
    BaseHeader,
    BaseMain,
    BaseFooter,
  },
  data() {
        return {
          links: [
                { text: "Chatachters"}, 
                { text: "Comic"}, 
                { text: "Movies"}, 
                { text: "TV"}, 
                { text: "Games"},
                { text: "Collectibles"}, 
                { text: "Videos"}, 
                { text: "Fans"},
                { text: "News"},
                { text: "Shop"}
            ],
          listafumetti: comicsList,
        }    
    }    
}
</script>

<template>

<BaseHeader :linkList="links"/>
<BaseMain :fumetti="listafumetti"/>
<BaseFooter :linkList="links"/>

</template>

<style lang="scss" scoped>
@use './styles/partials/_variables' as *;
</style>
