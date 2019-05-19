<template>
  <div id="app">
    <div id="common">
      <img
        id="head"
        src="https://www.autochess.biz/wp-content/uploads/2019/02/%EB%A1%9C%EA%B3%A0.png"
        alt="Dota Auto Chess"
      >

      <div class="icont" v-for="itemC in itemCs">
        <transition name="fade">
          <div v-if="itemC.show" class="info">
            {{itemC.name}}
            <p>{{itemC.stats}}</p>
          </div>
        </transition>

        <img
          class="iicon"
          @mouseover="itemC.show=true"
          @mouseleave="itemC.show=false"
          @click="itemC.craft=!itemC.craft"
          :src="itemC.url"
          :alt="itemC.name"
        >

        <transition name="fade">
          <div v-if="itemC.craft" class="combo">
            <div class="icont" v-for="recipe in itemC.recipe">
              <img
                class="iicon"
                @mouseover="itemC.show=true"
                @mouseleave="itemC.show=false"
                :src="itemC.url"
                :alt="itemC.name"
              >
            </div>
          </div>
        </transition>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      itemCs: [
        {
          id: "MOM",
          name: "Mask of Madness ",
          show: false,
          stats: "+40 Attack Speed\n+10% Lifesteal\nSilences the user",
          craft: false,
          rare: 3,
          recipe: [{ p: "MM" }, { p: "QS" }],
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/mask_of_madness_lg.png?3"
        },
        {
          name: "Morbid mask",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/lifesteal_lg.png?3"
        },
        {
          name: "Blades of Attack",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/blades_of_attack_lg.png?"
        },
        {
          name: "Blight Stone",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/blight_stone_lg.png?3"
        },
        {
          name: "Quarterstaff",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/quarterstaff_lg.png?3"
        },
        {
          name: "Robe of the Magi",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/robe_lg.png?3"
        },
        {
          name: "Ring of Health",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/ring_of_health_lg.png?3"
        },
        {
          name: "Ring of Regen",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/ring_of_regen_lg.png?3"
        },
        {
          name: "Void Stone",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/void_stone_lg.png?3"
        },
        {
          name: "Crown",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/crown_lg.png?3"
        },
        {
          name: "Chainmail",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/chainmail_lg.png?3"
        },
        {
          name: "Stout Shield",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/stout_shield_lg.png?3"
        },
        {
          name: "Cloak",
          show: false,
          rare: 1,
          url:
            "https://steamcdn-a.akamaihd.net/apps/dota2/images/items/cloak_lg.png?3"
        }
      ]
    };
  },
  methods: {
    toggle: function() {
      this.info = !this.info;
    }
  }
};
</script>

<style scoped>
body {
  background: #20262e;
  padding: 20px;
  font-family: Helvetica;
}

#app {
  background: #fff;
  border-radius: 4px;
  padding: 20px;
  height: 100%;
}

#common {
  background: #d0d0e1;
  border-radius: 4px;
  padding: 20px;
  display: grid;
  grid-template-columns: repeat(3, minmax(2%, 15%));
  grid-template-rows: auto;
  grid-template-areas: "header header header" "main main main" "footer footer footer";
  gap: 5%;
  justify-content: center;
  align-items: center;
  height: 100%;
}

#head {
  grid-area: header;
  width: 80%;
  height: auto;
  margin: 0 auto;
}

.item {
  border-radius: 10px;
  width: 85;
  height: 64;
}

.iicon {
  width: 100%;
  height: auto;
  border-radius: 3px;
}

.iicon:hover {
  width: 100%;
  height: auto;
  border-radius: 0px;
  border-bottom-left-radius: 3px;
  border-bottom-right-radius: 3px;
}

.icont {
  position: relative;
  z-index: 2;
}

.info {
  z-index: 1;
  position: absolute;
  bottom: 100%;
  right: 0;
  left: 0;
  line-height: 1.5em;
  background: #444;
  color: #fff;
  yofont-size: 70%;
  border-top-left-radius: 3px;
  border-top-right-radius: 3px;
}

.combo {
  background-color: red;
  height: 10px;
  width: 100%;
}

h2 {
  font-weight: bold;
  margin-bottom: 15px;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
