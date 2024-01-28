<!-- the script is where the js code goes -->
<script setup>
import { ref } from "vue";

const message = ref('Click the button to win a million dollars!');
const titleText = ref('Christopher Mina Website');
const buttonColor = ref('red');

// Function to handle button click
const handleButtonClick = () => {
  message.value = 'Congratulations! You won a million dollars!';
  // Change button color on each click
  buttonColor.value = getRandomColor();
};

// Function to handle reset button click
const handleResetClick = () => {
  message.value = 'Click the button to win a million dollars!';
  buttonColor.value = 'red';
};

// Function to get a random color
const getRandomColor = () => {
  const colors = ['red', 'green', 'blue', 'yellow', 'purple', 'orange'];
  return colors[Math.floor(Math.random() * colors.length)];
};
</script>

<!-- the template is where the html code goes -->
<template>
  <div>
    <div id="navbar" class="container">  
      <div id="title">{{ titleText }}</div>
      <div id="logo">
        <img src="./Animation.gif">
      </div>
    </div>

    <div id="flex">
      <!-- Your content in the flex div goes here -->
    </div>

    <div id="buttonContainer">
      <button id="myButton" :style="{ backgroundColor: buttonColor }" @click="handleButtonClick">Click me!</button>
      <button id="resetButton" @click="handleResetClick">Reset</button>
    </div>

    <div id="messageContainer">
      {{ message }}
    </div>
  </div>
</template>

<!-- style is where the css code goes -->
<style scoped>
body {
  margin: 30%;
}

div {
  box-sizing: border-box;
}

#logo {
  height: 100%;
  width: auto;
  position: left;
}

#flex {
  display: flex;
  height: calc(100vh - 50px);
  float: right;
}

#title {
  width: 100%;
  float: left;
  font-size: 24px;
  text-align: center;
}

#navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 50px;
  border: 1px solid red;
}

#logo {
  width: 30%;
}

#buttonContainer {
  margin-top: 20px;
  text-align: center;
}

#myButton, #resetButton {
  margin: 0 10px;
  color: white;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
}

#messageContainer {
  margin-top: 20px;
  color: green;
  font-weight: bold;
  text-align: center;
}
</style>