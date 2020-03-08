<template>
  <div>
    <div class="content">
      <div class="tab-wrapper">
        <div class="tab-content">
          <img v-bind:src="image">
        </div>
        <div class="tab-nav">
          <h2>Entdecke unsere Hautfreundlichkeit</h2>
          <p class="text-upper">Wähle Deine Größe</p>

          <ul class="btns-wrapper">
            <li class="tab-btn" :class="{ 'active' : currentTab == item.id }" 
                                @click="selectTab(item.id)"
                                v-for="item in tabsContent" 
                                :key="item.id" >
              <p>{{ item.id }}</p>
              <span class="text-upper">{{ item.weight }}</span>
            </li>
          </ul>

          <p>Teste jetzt unsere hautfreundlichen Windeln und erhalte unsere Feuchttücher mit 99 % Wasser zu Größe 1 - 3 oder die Sensitiven Feuchttücher zu Größe 4 - 5.</p>

          <ul>
            <li>Wir zahlen die Produkte, Du nur den Versand.</li>
            <li class="primary-color">Automatischer Übergang ins jederzeit kündbare Windel-Abo für 49,50 € pro Lieferung.</li>
            <li>Preise inkl. MwSt., ggf. zzgl. <a href="#">Versandkosten</a></li>
          </ul>

          <button class="btn btn-block">IN DEN WARENKORB LEGEN</button>

        </div>
      </div>
    </div>
    <Composition :tabId="currentTab"></Composition>
  </div>
</template>

<script>

import Composition from './Composition'

export default {
  name: 'Tabs',
  components: {
    Composition,
  },
  data: function(){
    return {
      currentTab: 1,
      image: require('../assets/images/lillydoo-testpaket-10.jpg'),
      tabsContent: [
        {
          id: 1,
          weight: '(2-5 kg)',
        },
        {
          id: 2,
          weight: '(4-8 kg)',
        },
        {
          id: 3,
          weight: '(6-10 kg)',
        },
        {
          id: 4,
          weight: '(9-14 kg)',
        },
        {
          id: 5,
          weight: '(11-16 kg)',
        },
      ]
    }
  },
  methods: {
    selectTab(selectedTab){
      this.currentTab = selectedTab;
      this.image = require('../assets/images/lillydoo-testpaket-'+ selectedTab +'0.jpg');
    }
  },
}
</script>