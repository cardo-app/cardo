<template>
  <div>
    <h1>Create</h1>
    <div>
      <DropDown :games="games" />
      <h4>Game Type</h4>
      <select name="gameType">
        <option value="golf">Golf</option>
      </select>
    </div>
    <div>
      <h4>Room Name</h4>
      <input type="text" placeholder="Room Name">
    </div>
    <div>
      <h4>Player Name</h4>
      <input type="text" placeholder="Player Name">
    </div>
    <div class="buttons-container">
      <router-link to="/">
        <div class="button">
          <svg
            class="button-border"
            viewBox="0 0 84 38"
            style="fill-rule:evenodd;clip-rule:evenodd;stroke-linecap:square;stroke-miterlimit:1.5;"
          >
            <g class="gold-layer">
              <path d="M79.352,3.602l-75,0l0,30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
              <path d="M4.352,33.602l75,0l0,-30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            </g>
            <g class="gold-layer">
              <path
                d="M7.352,35.852l69,0l0,-34.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
              <path
                d="M76.352,1.352l-69,0l0,34.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
            </g>
            <g class="gold-layer">
              <path
                d="M82.352,5.852l-81,0l0,25.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
              <path
                d="M1.352,31.352l81,0l0,-25.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
            </g>
            <g class="green-layer">
              <path d="M79.352,3.602l-75,0l0,30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
              <path d="M4.352,33.602l75,0l0,-30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            </g>
            <g class="green-layer">
              <path
                d="M7.352,35.852l69,0l0,-34.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
              <path
                d="M76.352,1.352l-69,0l0,34.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
            </g>
            <g class="green-layer">
              <path
                d="M82.352,5.852l-81,0l0,25.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
              <path
                d="M1.352,31.352l81,0l0,-25.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
            </g>
          </svg>
          <h3>Cancel</h3>
        </div>
      </router-link>
      <router-link to="/game">
        <div class="button">
          <svg
            class="button-border"
            viewBox="0 0 84 38"
            style="fill-rule:evenodd;clip-rule:evenodd;stroke-linecap:square;stroke-miterlimit:1.5;"
          >
            <g class="gold-layer">
              <path d="M79.352,3.602l-75,0l0,30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
              <path d="M4.352,33.602l75,0l0,-30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            </g>
            <g class="gold-layer">
              <path
                d="M7.352,35.852l69,0l0,-34.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
              <path
                d="M76.352,1.352l-69,0l0,34.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
            </g>
            <g class="gold-layer">
              <path
                d="M82.352,5.852l-81,0l0,25.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
              <path
                d="M1.352,31.352l81,0l0,-25.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
            </g>
            <g class="green-layer">
              <path d="M79.352,3.602l-75,0l0,30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
              <path d="M4.352,33.602l75,0l0,-30" style="fill:none;stroke:#000;stroke-width:0.75px;"></path>
            </g>
            <g class="green-layer">
              <path
                d="M7.352,35.852l69,0l0,-34.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
              <path
                d="M76.352,1.352l-69,0l0,34.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
            </g>
            <g class="green-layer">
              <path
                d="M82.352,5.852l-81,0l0,25.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
              <path
                d="M1.352,31.352l81,0l0,-25.5"
                style="fill:none;stroke:#000;stroke-width:0.75px;"
              ></path>
            </g>
          </svg>
          <h3>Start</h3>
        </div>
      </router-link>
    </div>
  </div>
</template>

<script>
import DropDown from '../components/DropDown.vue'
export default {
  name: "Create",

  components: {
    DropDown
  },

  data(){
    return{
      games: ["6 Card Golf","test","testy","testyTest"],
      test: 1
    }
    
  },

  computed: {
    selected:{ 
      get: function(){
      return this.games.findIndex(val => val ==="test")
      },
      set: function(game){
        return this.games.findIndex('test')
      }
    }
  },

  methods: {

  }
};
</script>

<style lang="scss" scoped>
input,
select,
h4 {
  font-family: "Montserrat", sans-serif;
  font-weight: 400;
}
input,
select {
  min-width: 290px;
}
.buttons-container {
  display: flex;
  justify-content: space-between;
  max-width: 290px;
  margin: 0 auto;
}
</style>