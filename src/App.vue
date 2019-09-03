<template>
  <div class = "hexagonA"><span>test</span></div>
  
</template>

<style lang="scss" scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

$hexagon_diameter: 0.5;

.hexagonA {
  margin: 0 auto;
  width: 155px * $hexagon_diameter;
  height: 90px * $hexagon_diameter;
  display: block;
  position: relative;
  background: #ddd;
  transition: all 0.2s linear;
  border-left: solid 1pt black;
  border-right: solid 1pt black;
}
.hexagonA span {
  width: 100%;
  height: 90px * $hexagon_diameter;
  line-height: 90px * $hexagon_diameter;
  color: #000;
  text-align: center;
  display: block;
  position: relative;
  z-index: 1;
}
.hexagonA:before,
.hexagonA:after {
  content: '';
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  position: absolute;
  background: #ddd;
  transition: all 0.2s linear;
  z-index: 0;
  border-left: solid 1pt black;
  border-right: solid 1pt black;
}
.hexagonA:before {
  transform: rotate(60deg);
}
.hexagonA:after {
  transform: rotate(120deg);
}
.hexagonA:hover,
.hexagonA:hover:before,
.hexagonA:hover:after {
  background: #bbb;
}
</style>
