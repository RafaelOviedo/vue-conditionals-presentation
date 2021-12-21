<template>
  <div class="conditionalsAndLoopsContainer">
    <h1 class="title">Conditionals and loops</h1>
    <h3 class="subTitle">Que es un condicional?</h3>

    <p class="text">Una declaracion condicional es aquella que puede controlar el 
      comportamiento de uno<br>o varios elementos y determinan si una 
      pieza de codigo se ejecuta o no.
      <br>
      <br>
      En javascript hay distintos tipos de condicionales como pueden ser:
      <br>
      <br>
      - If
      <br>
      <br>
      <u>Ejemplo:</u>
      </p>

    <Boolean v-show="booleanComponent" @click="changeCondition" />

      <code class="codeContainer">
        <button class="booleanButton" @click="showBooleanComponent"></button>
        <p class="codePiece">
          var condition = true;
          <br>
          <br>
          if (condition === true) {
            console.log("hola")
          } // output: hola
          <br>
          <br>
          if (condition === false) {
            console.log("no hay hola")
          } // output: no hay hola
        </p>
      </code>

      <p class="text2">
      <br>
      - Else
      <br>
      <br>
      <u>Ejemplo:</u>
      </p>

      <code class="codeContainer2">
        <p class="codePiece">
          var condition = true;
          <br>
          <br>
          if (condition === true) {
            <br>
            console.log("hola")
            <br>
          } else {
            <br>
            console.log("no hay hola")
            <br>
          }
          <br>
          <br>
          <br>
        </p>
      </code>

      <p class="text3">
      - If-Else
      <br>
      <br>
      <u>Ejemplo:</u>
      </p>

      <code class="codeContainer3">
        <p class="codePiece">
          var condition;
          <br>
          <br>
          if(condition === true) {
            <br>
            console.log("hola")
            <br>
          } else if (condition === false) {
            <br>
            console.log("No hay hola")
            <br>
          } else {
            <br>
            console.log("ni uno ni otro")
            <br>
          }
          <br>
          <br>
          <br>
          <br>
        </p>
      </code>

      <p class="text4">
        <b>Operadores Logicos</b>
        <br>
        <br>
        Los operadores lógicos se utilizan para determinar la lógica entre valores.
        <br><br>
        Asignando estas variable x = 6 e y = 3, el siguiente ejemplo explica los operadores lógicos:
      </p>

      <div class="codeContainer4">
        <div class="box0">
          <p>Operador</p>
          <p class="desc">Descripcion</p>
          <p class="ejemplo">Ejemplo</p>
        </div>
        <div class="box1">
          <p><b>&&</b></p>
          <p>and</p>
          <p>(x &#60; 10 && y > 1)&nbsp;&nbsp; is true</p>
        </div>
        <div class="box2">
          <p>||</p>
          <p class="or">or</p>
          <p class="secEx">(x === 5 || y === 5)&nbsp;&nbsp; is false</p>
        </div>
        <div class="box3">
          <p class="exclamation">!</p>
          <p class="not">not</p>
          <p class="terEx">!(x === y)&nbsp;&nbsp; is true</p>
        </div>
      </div>

      <h3 class="subTitleLoop">Que es un loop/bucle?</h3>

      <p class="textLoop">Un bucle o un loop, es un proceso que se ejecuta repetidas veces hasta que la condicion evalua en falso.
         <br>
         <br>
         <u>Ejemplo:</u>
      </p>

      <br>

      <code class="codeContainerLoop">
        <p class="codePiece">
          let list = [1, 2, 3, 4, 5];
          <br>
          <br>
          for (let i = 0; i &#60; list.length; i++) {
            <br>
              console.log(i)
            <br>
          }
          <br>
          // output: 0, 1, 2, 3, 4
        </p>
      </code>
  </div>
</template>

<script>
import Boolean from './Boolean.vue'

export default {
  name: "ConditionalsAndLoops",
  components: { Boolean },
  data() {
    return {
      booleanComponent: false,
    }
  },
  methods: {
    showBooleanComponent() {
      this.booleanComponent = true;
    },
    changeCondition() {
      this.booleanComponent = false;
    }
  }
};
</script>

<style scoped>
.conditionalsAndLoopsContainer {
  position: fixed;
  top: 10vh;
  left: 0;
  width: 100%;
  height: 90vh;
  /* border: 1px solid black; */
  font-family: Arial, Helvetica, sans-serif;
  overflow: scroll;
}
.conditionalsAndLoopsContainer::-webkit-scrollbar {
  display: none;
}

.title {
  transform: matrix(1,0,0,1, 650, 15);
}
.subTitle {
  font-size: 20px;
  transform: matrix(1,0,0,1, 200, 35);
}

.text {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 65);
}

.codeContainer {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  position: absolute;
  top: 400px;
  left: 130px;
  width: 80%;
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
.booleanButton {
  position: absolute;
  top: 30px;
  left: 142px;
  width: 50px;
  height: 20px;
  background: transparent;
  border: none;
  cursor: pointer;
}
.booleanButton:hover {
  border: 1px solid #fff;
}

.text2 {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 265);
}
.codeContainer2 {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  position: absolute;
  top: 680px;
  left: 130px;
  width: 80%;
  height: 22vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}

.text3 {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 500);
}
.codeContainer3 {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  position: absolute;
  top: 1010px;
  left: 130px;
  width: 80%;
  height: 28vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}

.subTitleLoop {
  font-size: 20px;
  transform: matrix(1,0,0,1, 200, 1080);
}
.textLoop {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 1100);
}

.codeContainerLoop {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  position: absolute;
  top: 1790px;
  left: 130px;
  width: 80%;
  height: 22vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}

.text4 {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 790);
}

/* .logicalOperatorsBox {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-direction: column;
  position: absolute;
  top: 1400px;
  left: 130px;
  width: 1200px;
  height: 250px;
  border: 1px solid black;
} */

.box0 {
  display: flex;
  justify-content: space-evenly;
  width: 90%;
  height: 30%;
  border-bottom: 1px solid #fff;
}
.box1 {
  display: flex;
  justify-content: space-evenly;
  width: 90%;
  height: 30%;
  border-bottom: 1px solid #fff;
}
.box2 {
  display: flex;
  justify-content: space-evenly;
  width: 90%;
  height: 30%;
}
.box3 {
  display: flex;
  justify-content: space-evenly;
  width: 90%;
  height: 30%;
  border-top: 1px solid #fff;
}

.codeContainer4 {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-direction: column;
  position: absolute;
  top: 1420px;
  left: 130px;
  width: 80%;
  height: 28vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}
.exclamation {
  transform: matrix(1,0,0,1, -15, 0);
}
.desc {
  transform: matrix(1,0,0,1, -50, 0);
}
.or {
  transform: matrix(1,0,0,1, 10, 0);
}
.not {
  transform: matrix(1,0,0,1, -21, 0);
}
.ejemplo {
  transform: matrix(1,0,0,1, -110, 0);
}
.secEx {
  transform: matrix(1,0,0,1, 20, 0);
}
.terEx {
  transform: matrix(1,0,0,1, -32, 0);
}
</style>
