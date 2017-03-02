<template lang="html">
  <div class="SongItem">
    <div class="panel-block">
      <div class="media is-fullwidth">
        <div class="media-left">
          <img v-bind:src="track.images">
        </div>

        <div class="media-content">
          <div class="track__artist">{{ track.artists[0].name }}</div>
          <div class="track__name">{{ track.name }}</div>
        </div>

        <div class="media-right">
          <span class="fa fa-spotify"></span>
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
    };
  },

  methods: {

  },
};
</script>
