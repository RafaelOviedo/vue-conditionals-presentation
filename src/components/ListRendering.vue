<template>
  <div class="listRenderingContainer">
    <h1 class="title">List Rendering</h1>
    <h3 class="subTitle">Que es el renderizado de lista?</h3>
    <p class="text">
    El renderizado de lista se usa para presentar una serie de elementos agrupados de<br>
    manera similar sin repetir codigo
    <br>
    <br>
    <u>Ejemplo:</u>
    <br>
    <br>
    Mapeando elementos de una lista con <code class="codeBlock">v-for</code><br><br>
    La directiva <code class="codeBlock">v-for</code> la podemos usar para renderizar los elementos de una lista (array).<br><br>
    Esta directiva requiere una sintaxis especial en forma de <i>elemento en elementos</i>, donde <i>elementos</i><br>
    es la lista (array) de datos y <i>elemento</i> seria la instancia del elemento en el que esta iterando:
    </p>
    <code class="codeContainer">
        <p class="codePiece">
          &#60;ul id="example-1">
          <br>
            &nbsp;&#60;li v-for="item in items" :key="item.message">
            <br>
              &nbsp;&nbsp;&#123;&#123; item.message &#125;&#125;
              <br>
            &nbsp;&#60;/li>
            <br>
          &#60;/ul>

          <br>
          <br>
          <br>

          data() {
          <br>
          &nbsp; return {
            <br>
          &nbsp; &nbsp; items: [
          <br>
          &nbsp; &nbsp; &nbsp;'Hola',
          <br>
          &nbsp; &nbsp; &nbsp;'soy',
          <br>
          &nbsp; &nbsp; &nbsp;'una',
          <br>
          &nbsp; &nbsp; &nbsp;'lista',
          <br>
          &nbsp; &nbsp; &nbsp;'renderizada',
          <br>
          &nbsp; &nbsp;],
          <br>
          &nbsp; }
          <br>
          }
        </p>
      </code>

      <br>

      <p class="manualTitle"><b>Lista renderizada manualmente</b></p>

      <div class="listContainer">
        <br>
        <p>{{items[0]}}</p>
        <p>{{items[1]}}</p>
        <p>{{items[2]}}</p>
        <p>{{items[3]}}</p>
        <p>{{items[4]}}</p>
      </div>


      <p class="forTitle"><b>Lista renderizada con v-for</b></p>

      <div class="listContainerFor" >
        <br>
        <li class="listItem" v-for="(item, index) in items" :key="index">{{item}}</li>
      </div>

      <br>

      <p class="forOfText">También puede usar <code class="codeBlock">of</code> como delimitador en lugar de <code class="codeBlock">in</code>, y asi estar más cerca de la sintaxis de JavaScript para iteradores:</p>

      <code class="codeContainer2">
        <p class="codePiece">
          &nbsp;&#60;div v-for="item of items">&#60;/div>
        </p>
      </code>

      <br>

      <p class="text2"><b>v-for trabajando con objetos:</b>
      <br>
      <br>
      La directiva <code class="codeBlock">v-for</code> también se puede utilizar para recorrer las propiedades de un objeto.
      </p>
      <code class="codeContainer3">
        <p class="codePiece">
          &#60;ul id="example-1">
          <br>
            &nbsp;&#60;li v-for="value in object">
            <br>
              &nbsp;&nbsp;&#123;&#123; value &#125;&#125;
              <br>
            &nbsp;&#60;/li>
            <br>
          &#60;/ul>

          <br>
          <br>
          <br>

          data() {
          <br>
          &nbsp; return {
            <br>
          &nbsp; &nbsp; object: {
          <br>
          &nbsp; &nbsp; &nbsp;title: 'Un objeto de javascript',
          <br>
          &nbsp; &nbsp; &nbsp;name: 'Rafael Oviedo',
          <br>
          &nbsp; &nbsp; &nbsp;date: '30-11-21',
          <br>
          &nbsp; &nbsp;},
          <br>
          &nbsp; }
          <br>
          }
        </p>
      </code>

      <p class="objectTitle"><b>Valores del objeto renderizado</b></p>

      <div class="objectContainer" id="v-for-object">
        <br>
        <li class="objectItem" v-for="value in object" :key="value">{{value}}</li>
      </div>

      <p class="text3">También se puede agregar un segundo argumento para el nombre de la propiedad (también conocido como key):</p>

      <code class="codeContainer4">
        <p class="codePiece">
          &nbsp;&#60;div v-for="(value, key) of items">
          <br>
          &nbsp;&nbsp;&#123;&#123; key }} &#123;&#123; value }}
          <br>
          &nbsp;&#60;/div>
        </p>
      </code>

      <p class="objectTitle2"><b>Pares prop-valor del objeto renderizado</b></p>

      <div class="objectContainer2" id="v-for-object">
        <br>
        <li class="objectItem" v-for="(value, key, index) in object" :key="value">{{index}}. {{key}} : {{value}}</li>
      </div>
  </div>
</template>

<script>
export default {
  name: "ListRendering",
  data() {
    return {
      items: [
        "Hola",
        "soy",
        "una",
        "lista",
        "renderizada",
      ],
      object: {
        title: 'Un objeto de javascript',
        author: 'Rafael Oviedo',
        publishedAt: '30-11-21'
      }
    }
  }
}
</script>

<style scoped>
.listRenderingContainer {
  position: fixed;
  top: 10vh;
  left: 0;
  width: 100%;
  height: 90vh;
  font-family: Arial, Helvetica, sans-serif;
  overflow: scroll;
}
.listRenderingContainer::-webkit-scrollbar {
  display: none;
}

.title {
  transform: matrix(1,0,0,1, 700, 15);
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
  top: 480px;
  left: 130px;
  width: 80%;
  height: 47vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}
.codePiece {
  padding: 15px;
}

.codeBlock {
  background: #001B4C;
  color: #fff;
  border-radius: 3px;
}

.listContainer {
  width: 250px;
  height: 220px;
  position: absolute;
  top: 920px;
  left: 130px;
  /* border: 1px solid black; */
}

.listContainerFor {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: flex-start;
  width: 250px;
  height: 230px;
  position: absolute;
  top: 900px;
  left: 550px;
  /* border: 1px solid black; */
}

.listItem {
  list-style-type: none;
}

.manualTitle {
  position: absolute;
  top: 890px;
  left: 130px;
}

.forTitle {
  position: absolute;
  top: 890px;
  left: 550px;
}

.forOfText {
  position: absolute;
  top: 1140px;
  left: 130px;
}

.codeContainer2 {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  position: absolute;
  top: 1210px;
  left: 130px;
  width: 80%;
  height: 10vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}

.text2 {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 900);
}

.codeContainer3 {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  position: absolute;
  top: 1460px;
  left: 130px;
  width: 80%;
  height: 44vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}

.objectTitle {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 1330);
}

.objectContainer {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: flex-start;
  width: 250px;
  height: 120px;
  position: absolute;
  top: 1900px;
  left: 130px;
}

.objectItem {
  list-style-type: none;
}

.text3 {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 1500);
}

.codeContainer4 {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  position: absolute;
  top: 2120px;
  left: 130px;
  width: 80%;
  height: 15vh;
  background: #001B4C;
  color: #fff;
  border-radius: 10px;
  font-weight: bold;
  font-size: 15px;
}

.objectTitle2 {
  font-size: 18px;
  transform: matrix(1,0,0,1, 130, 1680);
}

.objectContainer2 {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: flex-start;
  width: 250px;
  height: 120px;
  position: absolute;
  top: 2300px;
  left: 130px;
}
</style>