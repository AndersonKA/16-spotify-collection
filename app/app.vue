<template lang="html">
    <div class="page">
      <div class="section">
        <div class="panel">

            <div class="panel-heading">
              Bastille
            </div>
            <div class="results">
              <song-item v-for="item in tracks" v-bind:track="item"></song-item>
          </div>
        </div>
      </div><!--section-->
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
      .then((data) => {
        this.tracks = data.tracks.items;
      });
  },
  data() {
    return {
      tracks: []
    };
  },

  methods: {
  },
};
</script>
