<script>
import FancyList from './components/FancyList.vue'
import _ from 'lodash'
import FormatNumber from './components/FormatNumber.vue'

export default {
  components: { FancyList, FormatNumber },

  data() {
    return {
      imagesLinks: [
        {
          imageLink:
            'https://cdn-staging.soloyal.co/assets/loyalty-programs/bonvoy/images/background.jpg',
        },
        {
          imageLink:
            'https://cdn-staging.soloyal.co/assets/loyalty-programs/beauty-insider/images/background.jpg',
        },
        {
          imageLink:
            'https://cdn-staging.soloyal.co/assets/loyalty-programs/trueblue/images/background.jpg',
        },
        {
          imageLink:
            'https://cdn-staging.soloyal.co/assets/loyalty-programs/7rewards/images/background.jpg',
        },
        {
          imageLink:
            'https://cdn-staging.soloyal.co/assets/loyalty-programs/accor-live-limitless/images/background.jpg',
        },
        {
          imageLink:
            'https://cdn-staging.soloyal.co/assets/loyalty-programs/amc-stubs/images/background.jpg',
        },
      ],
    }
  },
}
</script>

<template>
  <FancyList :items="imagesLinks" v-slot="props">
    <img :src="props.item.imageLink" />
  </FancyList>
</template>
