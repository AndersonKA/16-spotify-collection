<template lang="html">
  <div class="SongItem">
      <img src="http://cdn3-www.dogtime.com/assets/uploads/gallery/30-impossibly-cute-puppies/impossibly-cute-puppy-21.jpg" alt="" class="SongItem__pic">
        <h3 class="SongItem__artist">{{profile.artist}}</h3>
        <h5 class="SongItem__name">{{profile.name}}</h5>
        <span class="panel-icon level-right">
          <i class="fa fa-spotify level-item"></i>
        </span>
  </div>
</template>

<script>
export default {
  props: ['tracks'],

  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
