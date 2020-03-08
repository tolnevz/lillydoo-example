<template>
  <div class="dark">
    <div class="content">
      <h2 class="text-center">Dein Testpaket enthält</h2>
      <div v-for="composition in compositionContent" :key="composition.id">
        <div class="wrapper-2fr" v-if="tabId == composition.id">
          <div class="composition-item">
            <div class="composition-image">
              <img :src="composition.item_1.image">
            </div>
            <div class="composition-content">
              <h4>{{ composition.item_1.title }}</h4>
              <div class="stars">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star-half-alt"></i>
                <span class="star-count">({{ composition.item_1.review_count }})</span>
              </div>
              <div v-html="composition.item_1.description"></div>
            </div>
          </div>
          <div class="composition-item">
            <div class="composition-image">
              <img :src="composition.item_2.image">
            </div>
            <div class="composition-content">
              <h4>{{ composition.item_2.title }}</h4>
              <div class="stars">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star-half-alt"></i>
                <span class="star-count">({{ composition.item_2.review_count }})</span>
              </div>
              <div v-html="composition.item_2.description"></div>
            </div>
          </div>
        </div>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: 'Composition',
  props: {
    tabId: null
  },
  data: function(){
    return {
      compositionContent: [
        {
          id: 1,
          item_1: {
            image: require('../assets/images/diaper.png'),
            title: '10 LILLYDOO WINDELN',
            review_count: 12,
            description: '<ul><li>0 % Parfüme & Lotionen, 100 % LILLYDOO Schutz</li><li>Extra weich und super bequem</li><li>Mit unseren Turbo Tunneln für eine ideale Passform und schnelle Absorption</li></ul>',
          },
          item_2: {
            image: require('../assets/images/water-wipes-15.png'),
            title: '15 FEUCHTTÜCHER MIT 99 % WASSER',
            review_count: 114,
            description: '<ul><li>0 % Parfüme & PEGs, 100 % biologisch abbaubar</li><li>Natürlich rein, extra mild, Alternative zu "Wasser & Watte"</li></ul>',
          },
        },
        {
          id: 2,
          item_1: {
            image: require('../assets/images/diaper.png'),
            title: '10 LILLYDOO WINDELN',
            review_count: 91,
            description: '<ul><li>0 % Parfüme & Lotionen, 100 % LILLYDOO Schutz</li><li>Extra weich und super bequem</li><li>Mit unseren Turbo Tunneln für eine ideale Passform und schnelle Absorption</li></ul>',
          },
          item_2: {
            image: require('../assets/images/water-wipes-15.png'),
            title: '15 FEUCHTTÜCHER MIT 99 % WASSER',
            review_count: 114,
            description: '<ul><li>0 % Parfüme & PEGs, 100 % biologisch abbaubar</li><li>Natürlich rein, extra mild, Alternative zu "Wasser & Watte"</li></ul>',
          },
        },
        {
          id: 3,
          item_1: {
            image: require('../assets/images/diaper.png'),
            title: '10 LILLYDOO WINDELN',
            review_count: 327,
            description: '<ul><li>0 % Parfüme & Lotionen, 100 % LILLYDOO Schutz</li><li>Extra weich und super bequem</li><li>Mit unseren Turbo Tunneln für eine ideale Passform und schnelle Absorption</li></ul>',
          },
          item_2: {
            image: require('../assets/images/water-wipes-15.png'),
            title: '15 FEUCHTTÜCHER MIT 99 % WASSER',
            review_count: 114,
            description: '<ul><li>0 % Parfüme & PEGs, 100 % biologisch abbaubar</li><li>Natürlich rein, extra mild, Alternative zu "Wasser & Watte"</li></ul>',
          },
        },
        {
          id: 4,
          item_1: {
            image: require('../assets/images/diaper.png'),
            title: '10 LILLYDOO WINDELN',
            review_count: 481,
            description: '<ul><li>0 % Parfüme & Lotionen, 100 % LILLYDOO Schutz</li><li>Extra weich und super bequem</li><li>Mit unseren Turbo Tunneln für eine ideale Passform und schnelle Absorption</li></ul>',
          },
          item_2: {
            image: require('../assets/images/sensitive-wipes-15.png'),
            title: '15 SENSITIVE FEUCHTTÜCHER',
            review_count: 46,
            description: '<ul><li>0 % Parfüme & PEGs, 100 % biologisch abbaubar</li><li>Extra dickes und kompostierbares Tuch</li></ul>',
          },
        },
        {
          id: 5,
          item_1: {
            image: require('../assets/images/diaper.png'),
            title: '10 LILLYDOO WINDELN',
            review_count: 387,
            description: '<ul><li>0 % Parfüme & Lotionen, 100 % LILLYDOO Schutz</li><li>Extra weich und super bequem</li><li>Mit unseren Turbo Tunneln für eine ideale Passform und schnelle Absorption</li></ul>',
          },
          item_2: {
            image: require('../assets/images/sensitive-wipes-15.png'),
            title: '15 SENSITIVE FEUCHTTÜCHER',
            review_count: 46,
            description: '<ul><li>0 % Parfüme & PEGs, 100 % biologisch abbaubar</li><li>Extra dickes und kompostierbares Tuch</li></ul>',
          },
        },
      ]
    }
  },
}
</script>