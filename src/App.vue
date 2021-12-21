<template>
  <div>
    <div class="buttonsContainer">
      <button class="conditionalsAndLoopsButton" @click="toConditionalsAndLoops">Conditionals And Loops</button>
      <button class="directivesButton" @click="toDirectives">Directives</button>
      <button class="conditionalRenderingButton" @click="toConditionalRendering">Conditional Rendering</button>
      <button class="listRenderingButton" @click="toListRendering">List Rendering</button>
    </div>
    <ConditionalsAndLoops v-show="ConditionalsAndLoops"/>
    <Directives v-show="Directives"/>
    <ConditionalRendering v-show="ConditionalRendering"/>
    <ListRendering v-show="ListRendering"/>
  </div>
</template>

<script>
import ConditionalsAndLoops from "./components/ConditionalsAndLoops.vue";
import Directives from "./components/Directives.vue";
import ConditionalRendering from "./components/ConditionalRendering.vue";
import ListRendering from "./components/ListRendering.vue";

export default {
  name: "App",
  components: {
      ConditionalsAndLoops,
      Directives,
      ConditionalRendering,
      ListRendering
  },
  data() {
    return {
      ConditionalsAndLoops: true,
      Directives: false,
      ConditionalRendering: false,
      ListRendering: false,
    }
  },
  methods: {
    toConditionalsAndLoops() {
      this.ConditionalsAndLoops = true;
      this.Directives = false;
      this.ConditionalRendering = false;
      this.ListRendering = false;
    },
    toDirectives() {
      this.ConditionalsAndLoops = false;
      this.Directives = true;
      this.ConditionalRendering = false;
      this.ListRendering = false;
    },
    toConditionalRendering() {
      this.ConditionalsAndLoops = false;
      this.Directives = false;
      this.ConditionalRendering = true;
      this.ListRendering = false;
    },
    toListRendering() {
      this.ConditionalsAndLoops = false;
      this.Directives = false;
      this.ConditionalRendering = false;
      this.ListRendering = true;
    }
  }
};
</script>

<style scoped>
.buttonsContainer {
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  width: 70vw;
  height: 10vh;
}
.conditionalsAndLoopsButton {
  width: 20%;
  height: 60%;
  border-radius: 5px;
  border: none;
  background: #ECB200;
  color: #fff;
  font-weight: bold;
  font-size: 18px;
  cursor: pointer;
}
.conditionalsAndLoopsButton:active {
  background: #fff;
  color: #ECB200;
}
.directivesButton {
  width: 20%;
  height: 60%;
  border-radius: 5px;
  border: none;
  background: #00D372;
  color: #fff;
  font-weight: bold;
  font-size: 18px;
  cursor: pointer;
}
.directivesButton:active {
  background: #fff;
  color: #00D372;
}

.conditionalRenderingButton {
  width: 20%;
  height: 60%;
  border-radius: 5px;
  border: none;
  background: #00A0BF;
  color: #fff;
  font-weight: bold;
  font-size: 18px;
  cursor: pointer;
}
.conditionalRenderingButton:active {
  background: #fff;
  color: #00A0BF;
}

.listRenderingButton {
  width: 20%;
  height: 60%;
  border-radius: 5px;
  border: none;
  background: #B00043;
  color: #fff;
  font-weight: bold;
  font-size: 18px;
  cursor: pointer;
}
.listRenderingButton:active {
  background: #fff;
  color: #B00043;
}
</style>