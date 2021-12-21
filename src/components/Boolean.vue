<template>
  <div class="booleanContainer">
    <button class="closeButton" @click="toParent">&times;</button>
    <p class="booleanText">El tipo de datos booleano en JavaScript puede almacenar uno de dos valores posibles:<br>
      verdadero o falso. Los valores booleanos son el resultado de una comparacion entre dos valores.<br>
      Si comparamos 3 es igual a 30, devuelve falso.
      <br>
      <br>
      Ejemplo:
      <br>
      <code class="codeContainer">
        <p class="codePiece">
          <br>
          2 === 5  // output: false
          <br>
          <br>
          1 === 1  // output: true
          <br>
        </p>
      </code>
      </p>
  </div>
</template>

<script>
export default {
  name: "Boolean",
  data() {
    return {

    }
  },
  methods: {
    toParent() {
      this.$emit("changeCondition")
    }
  }
}
</script>

<style scoped>
.booleanContainer {
  position: absolute;
  top: 10px;
  left: 200px;
  width: 50%;
  height: 50%;
  border: 1px solid #000;
  background: #fff;
  font-size: 15px;
  font-weight: bold;
  pointer-events: none;
}
.closeButton {
  width: 8%;
  height: 8%;
  margin: 15px;
  border: none;
  background: #001B4C;
  color: #fff;
  border-radius: 5px;
  cursor: pointer;
  pointer-events: all;
}
.closeButton:active {
  background: #fff;
  color: #001B4C;
}

.booleanText {
  margin: 10px;
}
.codeContainer {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  position: absolute;
  top: 180px;
  left: 30px;
  width: 90%;
  height: 20vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}
.codePiece {
  padding: 15px;
}
</style>