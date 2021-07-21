<template>
  <div id="sidebar">
    <img class="gif" src="../assets/gif2.gif" alt="" />
    <span v-on:click="$emit('play')" class="newGame">StartGame</span>
  </div>
  <audio loop volume="0.01" controls autoplay>
    <source src="../assets/Sayo-nara.mp3" type="audio/mpeg" />
    Your browser does not support the audio element.
  </audio>
</template>

<script>
export default {
  name: "page1",
};
</script>

<style scoped>
.gif {
  position: absolute;
  right: 0;
  top: 0;
  width: 100%;
  height: 100vh;
}
.newGame {
  position: absolute;
  left: 50%;
  top: 70%;
  transform: translate(-50%, -50%);
  color: coral;
  font-size: 80px;
}
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@1,900&display=swap");

body {
  padding: 0;
  margin: 0;
  font-family: "Poppins", sans-serif;
  background: black;
  height: 100vh;
  width: 100vw;
}

span {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  display: block;
  color: #cf1b1b;
  font-size: 100px;
  letter-spacing: 8px;
  cursor: pointer;
}

span::before {
  content: "StartGame";
  position: absolute;
  color: transparent;
  background-image: repeating-linear-gradient(
    45deg,
    transparent 0,
    transparent 2px,
    white 2px,
    white 4px
  );
  -webkit-background-clip: text;
  top: 0px;
  left: 0;
  z-index: -1;
  transition: 1s;
}

span::after {
  content: "StartGame";
  position: absolute;
  color: transparent;
  background-image: repeating-linear-gradient(
    135deg,
    transparent 0,
    transparent 2px,
    white 2px,
    white 4px
  );
  -webkit-background-clip: text;
  top: 0px;
  left: 0px;
  transition: 1s;
}

span:hover:before {
  top: 10px;
  left: 10px;
}

span:hover:after {
  top: -10px;
  left: -10px;
}

audio {
/*border-radius: 90px;*/
width: 120px;
height: 45px;
margin-top: 5px;
margin-bottom: 5px;
}
audio::-webkit-media-controls-timeline-container{
display: none !important;
}

audio::-webkit-media-controls-current-time-display{
display: none !important;
}

audio::-webkit-media-controls-time-remaining-display{
display: none !important;
}

audio::-webkit-media-controls-timeline{
display: none !important;
}

audio::-webkit-media-controls-seek-back-button{
display: none !important;
}

audio::-webkit-media-controls-seek-forward-button{
display: none !important;
}

audio::-webkit-media-controls-fullscreen-button{
display: none !important;
}

audio::-webkit-media-controls-rewind-button{
display: none !important;
}

audio::-webkit-media-controls-return-to-realtime-button{
display: none !important;
}

audio::-webkit-media-controls-toggle-closed-captions-button{
display: none !important;
}
audio::-webkit-media-controls-panel, video::-webkit-media-controls-panel {
  background-color: orange;
}

</style>
