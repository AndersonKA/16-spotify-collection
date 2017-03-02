<template lang="html">
  <div class="SongItem">
    <div class="panel-block">
      <div class="media is-fullwidth">
        <div class="media-left">
          <img src="http://cdn3-www.dogtime.com/assets/uploads/gallery/30-impossibly-cute-puppies/impossibly-cute-puppy-21.jpg" alt="" class="track__frame">
        </div>

        <div class="media-content">
          <div class="track__artist">something</div>
          <div class="track__name">else</div>
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
