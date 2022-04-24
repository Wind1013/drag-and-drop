<template>
  <div id="app">
    <main class="flexbox">
      <board-element id="board-1">
        <card-element id="card-1" draggable="true">
          <p>Card one</p>
        </card-element>
      </board-element>
      <board-element id="board-2">
        <card-element id="card-2" draggable="true">
          <p>Card two</p>
        </card-element>
      </board-element>
    </main>
  </div>
</template>

<script>
/* eslint-disable */
import BoardElement from "./components/Board.vue";
import CardElement from "./components/Card.vue";

export default {
  name: "App",
  components: {
    BoardElement,
    CardElement,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: #f3f3f3;
}

.flexbox {
  display: flex;
  justify-content: space-between;
  width: 100%;
  max-width: 768px;
  height: 100vh;

  overflow: hidden;

  margin: 0 auto;
  padding: 15px;
}

.flexbox .board {
  display: flex;
  flex-direction: column;

  width: 100%;
  max-width: 300px;

  background-color: #313131;

  padding: 15px;
}

.flexbox .board .card {
  padding: 15px 25px;
  background-color: #f3f3f3;

  cursor: pointer;
  margin-bottom: 15px;
}
</style>
