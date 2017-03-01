<template lang="html">
  <div class="app">
    <div class="section">
      <div class="container">

        <div class="panel">
          <p class="panel-heading">
            Bastille
          </p>

          <!--<div class="panel-block level-left">-->
            <span class="panel-block level-item">Song


          </span>
          <song-item v-for="item in repositories" v-bind:track="item"></song-item>

          </div>
        </div>
      </div>
    </div>


</template>



<script>
import SongItem from './song-item.vue';
export default {
  components: {
    SongItem,
  },


  created() {
    fetch('https://api.spotify.com/v1/search?query=bastille&type=track&offset=0&limit=20')
      .then(response => response.json())
      .then((track) => {
        this.repositories = track;
      });
  },
  data() {
    return {
      profile: {
        artist: 'Bastille',
        name: 'Pompeii'
      },
      repositories: [
        { name: 'Pompeii' },
        { name: 'Good Grief' },
      ]
    };
  },

  methods: {
  },
};
</script>
