<template>
  <div class="conditionalRenderingContainer">
    <h1 class="title">Conditional rendering</h1>
    <h3 class="subTitle">Que es el renderizado condicional?</h3>
    <p class="text">El renderizado condicional es la posibilidad de representar visualmente
      distintos elementos si una condición es verdadera o falsa.<br>En Vue, podemos renderizar
      diferentes elementos o componentes en función de estas condiciones.
      <br>
      <br>
      <u>Ejemplo:</u>
      <br>
      <br>
      La directiva <code class="codeBlock">v-if</code> se usa para renderizar condicionalmente un bloque.<br>
      El bloque solo se renderizará si la expresión de la directiva devuelve un valor verdadero.
    </p>

    <code class="codeContainer">
        <p class="codePiece">
          &#60;div v-if="awesome">Vue esta bueno!&#60;/div> 
        </p>
        &nbsp; data() {
          <br>
          &nbsp; &nbsp; return {
            <br>
          &nbsp; &nbsp; &nbsp; awesome: true,
            <br>
          &nbsp; &nbsp; }
          <br>
        &nbsp; }
      </code>

      <br>

      <p class="text2">También se puede agregar un "bloque else" con <code class="codeBlock">v-else</code>&nbsp;:</p>

      <code class="codeContainer2">
        <p class="codePiece">
          &#60;div v-else>Oh no 😢&#60;/div>
        </p>
      </code>

      <br>

      <div class="vueExample">

      <div v-if="awesome">Vue esta bueno!</div>
      <div v-else>Oh no 😢</div>
      <button class="vueExampleButton" v-on:click="toFalse">Cambiar a false</button>
      <button class="vueExampleButton" v-on:click="toTrue">Cambiar a true</button>

      </div>

      <br>

      <p class="text3">Diferencia entre <code class="codeBlock">v-if</code> y <code class="codeBlock">v-show</code>&nbsp;:
      <br>
      <br>
      Al igual que v-if, v-show tambien renderiza o no un elemento de manera condicional. La diferencia es que v-show<br>
      renderiza todos los elementos y solo muestra el que cumpla con la condicion, cambiando la propiedad display de CSS<br>
      por detras de camara.
      <br>
      <br>
      Es decir:
      <br>
      </p>

      <br>

      <code class="codeContainer3">
        <p class="codePiece">
          &#60;div v-show="awesome">Vue esta bueno otra vez!&#60;/div> 
          <br>
          &#60;div v-show="!awesome">Oh no 😢 Oh no 😢&#60;/div> 
        </p>
      </code>

      <div class="vueExample2">

      <div v-show="awesome">Vue esta bueno x2!</div>
      <div v-show="!awesome">Oh no 😢 x2</div>
      <button class="vueExampleButton" v-on:click="toFalse">Cambiar a false</button>
      <button class="vueExampleButton" v-on:click="toTrue">Cambiar a true</button>
      
      </div>
  </div>
</template>

<script>
export default {
  name: "ConditionalRendering",
  data() {
    return {
      awesome: true,
    }
  },
  methods: {
    toFalse() {
      this.awesome = false;
      console.log(this.awesome);
    },
    toTrue() {
      this.awesome = true;
      console.log(this.awesome);
    }
  }
}
</script>

<style scoped>
.conditionalRenderingContainer {
  position: fixed;
  top: 10vh;
  left: 0;
  width: 100%;
  height: 90vh;
  font-family: Arial, Helvetica, sans-serif;
  overflow: scroll;
}
.conditionalRenderingContainer::-webkit-scrollbar {
  display: none;
}

.title {
  transform: matrix(1,0,0,1, 690, 15);
}

.subTitle {
  font-size: 20px;
  transform: matrix(1,0,0,1, 200, 35);
}

.text {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 65);
}

.text2 {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 300);
}

.codeBlock {
  background: #001B4C;
  color: #fff;
  border-radius: 3px;
}

.codeContainer {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  position: absolute;
  top: 380px;
  left: 130px;
  width: 80%;
  height: 25vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}
.codePiece {
  padding: 15px;
}

.vueExample {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  width: 50%;
  height: 20vh;
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 335);
}
.vueExampleButton {
  width: 20%;
  height: 20%;
  font-weight: bold;
  font-size: 15px;
  background: #001B4C;
  color: #fff;
  border-radius: 5px;
  border: none;
  cursor: pointer;
}

.codeContainer2 {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  position: absolute;
  top: 670px;
  left: 130px;
  width: 80%;
  height: 10vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}

.text3 {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 310);
}

.codeContainer3 {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  position: absolute;
  top: 1060px;
  left: 130px;
  width: 80%;
  height: 13vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}

.vueExample2 {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  width: 50%;
  height: 20vh;
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 380);
}
</style>