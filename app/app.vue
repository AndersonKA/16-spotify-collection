<template lang="html">
    <div class="page">
    <div class="section">
      <div class="container">
        <div class="panel">
          <div class="panel-heading">
          Stuff
        </div>

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
      .then((tracks) => {
        this.repositories = tracks;
      });
  },
  data() {
    return {
      track: {
        artist: 'Bastille',
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
