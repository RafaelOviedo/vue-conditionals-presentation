<template>
  <div class="directivesContainer">
    <h1 class="title">Directives</h1>
    <h3 class="subTitle">Que son directivas en Vue?</h3>
    <p class="text">Las directivas de Vue son atributos especiales de HTML que nos permiten manipular elementos en el DOM.
      <br>
      <br>
      <u>Ejemplo:</u>
    </p>

    <code class="codeContainer">
        <p class="codePiece">
          &#60;div v-text="message">&#60;/div>
        </p>
        &nbsp; data() {
          <br>
          &nbsp; &nbsp; return {
            <br>
          &nbsp; &nbsp; &nbsp; message: "hola",
            <br>
          &nbsp; &nbsp; }
          <br>
        &nbsp; }
      </code>

      <!-- <div class="text2">{{message}}</div> -->

      <p class="text3">Directivas mas comunes en Vue:</p>
      <br>
      <p class="text4">
        - v-if
        <br>
        - v-else
        <br>
        - v-if-else
        <br>
        - v-show
        <br>
        - v-for
        <br>
        - v-on
        <br>
        - v-bind
        <br>
        - v-model
        <br>
        <br>
      </p>
  </div>
</template>

<script>
export default {
  name: "Directives",
  data() {
    return {
      message: "hola",

      classesOptions: {
        color: "#fff",
        backGround: "#000",
        width: "30px",
      }
    }
  }
}
</script>

<style scoped>
.directivesContainer {
  position: fixed;
  top: 10vh;
  left: 0;
  width: 100%;
  height: 90vh;
  font-family: Arial, Helvetica, sans-serif;
  overflow: scroll;
}
.directivesContainer::-webkit-scrollbar {
  display: none;
}

.title {
  transform: matrix(1,0,0,1, 770, 15);
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
  top: 290px;
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

.text2 {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 320);
}

.text3 {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 350);
}
.text4 {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 330);
}
</style>