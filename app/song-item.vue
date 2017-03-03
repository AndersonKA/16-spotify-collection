<template lang="html">
  <div class="SongItem">
    <div class="panel-block">
      <div class="media is-fullwidth">
        <div class="media-left">

            <img v-bind:src="track.album.images[0].url" class="track__frame">

        </div>

        <div class="media-content">
          <div class="track__artist">{{ track.artists[0].name }}</div>
          <div class="track__name">{{ track.name }}</div>
        </div>

        <div class="media-right">
          <a v-bind:href="track.external_urls.spotify"><span class="fa fa-spotify"></span></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['track'],

  data() {
    return {
      images: []
    };
  },

  methods: {

  },
};
</script>
