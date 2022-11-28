<template>
  <div class="fancy-list" v-for="(item, index) in filtered" :key="index">
    <div class="loyalty-program-card">
      <div class="background">
        <slot :item="item" :index="index"></slot>
      </div>
    </div>
  </div>
</template>

<script>
import _ from 'lodash'
export default {
  props: {
    items: [],
    searchObject: {},
  },

  computed: {
    filtered() {
      return _.filter(this.items, this.searchObject)
    },
  },
}
</script>

<style>
.fancy-list {
  @apply container m-4 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 md:gap-2;
}

.background {
  @apply bg-no-repeat bg-cover;
  @apply rounded-md md:rounded-lg;
  background-position: 50%;
  @apply h-full left-0 right-0 top-0 -z-10 w-full;
}

.loyalty-program-card {
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  border-radius: 0.375rem;
  color: rgb(255 255 255 / var(--tw-text-opacity));
  display: -webkit-box;
  display: -ms-flexbox;
  -webkit-transition-duration: 0.3s;
  -o-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -webkit-transition-property: -webkit-transform;
  transition-property: -webkit-transform;
  -o-transition-property: transform;
  transition-property: transform, -webkit-transform;
  -webkit-transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  -o-transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}
</style>
