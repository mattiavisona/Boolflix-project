    <script>

    import AppHeader from "./components/AppHeader.vue";
    import AppMain from "./components/AppMain.vue";

    import {store} from "./store.js";
    import axios from "axios";

    export default {
      data() {
        return{

          store,

        };
      },

      components: {
        AppMain,
        AppHeader,
    },

    created() {
      axios.get("https://api.themoviedb.org/3/search/movie?api_key=73bafa27b8cf325da1f263932832f596&query=fast and furious").then ((response) =>{
          console.log(response.data.results);

          this.store.movies = response.data.results
      })

    }

    }
    </script>

    <template>

        <AppHeader></AppHeader>
        
        <AppMain></AppMain>

    </template>

    <style lang="scss" scoped>

    </style>

