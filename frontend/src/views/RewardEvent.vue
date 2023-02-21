<template>
  <div>
    <phone-header></phone-header>

    <div class="image-container">    
    <img src="../assets/reward-event.svg" />
    <img class="animation" src="../assets/bronze-coin.gif" />
    <img class="top-bear" src="../assets/trumpet-bear.svg" />
    </div>

    <img @click="goBack" class="back_x" src="../assets/X.png" />

  </div>
</template>

<script>
import PhoneHeader from "../components/PhoneHeader.vue";

export default {
  components: { PhoneHeader },

  methods: {
    goBack() {
      window.history.length > 1 ? this.$router.go(-1) : this.$router.push("/");
    },
  },
};
</script>
<style scoped>
.back_x {
  position: absolute;
  z-index: 3;
  top: 50px;
  left: 10px;
}

.image-container{
  position: relative;
  z-index: 0;
}

.image-container .animation {
  position: absolute;
  margin-top: 40px;
  width: 320px;
  top: 40px;
  left: 0px;
  z-index: 1;
}

.image-container .top-bear {
  position: absolute;
  width: 161px;
  height: 148px;
  left: 153px;
  top: 234px;
  z-index: 2;
}

</style>
