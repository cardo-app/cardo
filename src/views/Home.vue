<template>
  <div class="home">
    <h1>Cardo</h1>
    <router-link to="/create">
      <div class="button">
        <svg
          class="button-border"
          viewBox="0 0 84 38"
          style="fill-rule:evenodd;clip-rule:evenodd;stroke-linecap:square;stroke-miterlimit:1.5;"
        >
          <g class='gold-layer'>
            <path d="M79.352,3.602l-75,0l0,30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M4.352,33.602l75,0l0,-30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
          <g class='gold-layer'>
            <path d="M7.352,35.852l69,0l0,-34.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M76.352,1.352l-69,0l0,34.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
          <g class='gold-layer'>
            <path d="M82.352,5.852l-81,0l0,25.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M1.352,31.352l81,0l0,-25.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
          <g class='green-layer'>
            <path d="M79.352,3.602l-75,0l0,30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M4.352,33.602l75,0l0,-30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
          <g class='green-layer'>
            <path d="M7.352,35.852l69,0l0,-34.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M76.352,1.352l-69,0l0,34.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
          <g class='green-layer'>
            <path d="M82.352,5.852l-81,0l0,25.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M1.352,31.352l81,0l0,-25.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
        </svg>
        <h3>Create</h3>
      </div>
    </router-link>
    <router-link to="/join">
      <div class="button">
        <svg
          class="button-border"
          viewBox="0 0 84 38"
          style="fill-rule:evenodd;clip-rule:evenodd;stroke-linecap:square;stroke-miterlimit:1.5;"
        >
          <g class='gold-layer'>
            <path d="M79.352,3.602l-75,0l0,30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M4.352,33.602l75,0l0,-30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
          <g class='gold-layer'>
            <path d="M7.352,35.852l69,0l0,-34.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M76.352,1.352l-69,0l0,34.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
          <g class='gold-layer'>
            <path d="M82.352,5.852l-81,0l0,25.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M1.352,31.352l81,0l0,-25.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
          <g class='green-layer'>
            <path d="M79.352,3.602l-75,0l0,30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M4.352,33.602l75,0l0,-30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
          <g class='green-layer'>
            <path d="M7.352,35.852l69,0l0,-34.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M76.352,1.352l-69,0l0,34.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
          <g class='green-layer'>
            <path d="M82.352,5.852l-81,0l0,25.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            <path d="M1.352,31.352l81,0l0,-25.5" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
          </g>
        </svg>
        <h3>Join</h3>
      </div>
    </router-link>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "home",
  components: {}
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Limelight|Montserrat:400,400i,700");
*,
*::before,
*::after {
  font-family: "Limelight", cursive;
  box-sizing: border-box;
}
.home {
  display: flex;
  align-items: center;
  flex-direction: column;
}
.button {
  width: 140px;
  height: 50px;
  font-size: 1rem;
  padding: 10px;
  margin: 20px 0;
  color: #2c666e;
  transition: 0.5s;
  position: relative;
  &:hover {
    color: #0a090c;
  }
  h3 {
    width: 100%;
    height: 125%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    padding: 0;
    margin: 0;
    top: 0;
    left: 0;
    z-index: -1;
  }
  .button-border {
    position: absolute;
    top: 0;
    left: 0;
    .gold-layer > path {
      stroke: #2c666e !important;
      transition: 1s cubic-bezier(0.57, 0.21, 0.25, 1);
    }
    .green-layer > path {
      stroke: #2c666e !important;
      opacity: .5;
    }
    &:hover {
      .gold-layer > path {
        stroke-dasharray: 160;
        stroke: #E1AD21 !important;
        animation: border-stroke .7s cubic-bezier(0.41, 0.29, 0.58, 1);
        animation-delay: .05s;
      }
      .green-layer > path {
        opacity: .5;
      }
    }
  }
}
a {
  text-decoration: none;
}

@keyframes border-stroke {
  from {
    stroke-dashoffset: 160
  }
  to {
    stroke-dashoffset: 0
  }
}
</style>
