<script lang="ts">
    interface propsContent{
        MainText:String,
        Alt:string
    }
    export default {
        name:"TooltipButtom",
        props:{
            MainText:String,
            Alt:String
        }
    }
</script>

<template>
    <div class="tooltip-container">
        <span class="tooltip">{{Alt}}</span>
        <span class="text">{{MainText}}</span>
    </div>
</template>

<style scoped>

    /* Style for the tooltip container */
.tooltip-container {
  --background-light: #ff5555; /* Red */
  --background-dark: #000000; /* Black */
  --text-color-light: #ffffff;
  --text-color-dark: #ffffff;
  --bubble-size: 12px;
  --glow-color: rgba(255, 255, 255, 0.5); /* Brighter glow color */
  text-align: center;
  position: relative;
  background: var(--background-light);
  cursor: pointer;
  transition: all 0.5s;
  font-size: 17px;
  padding: 0.7em 1.8em;
  color: var(--text-color-light);
  border-radius: 8px; /* Rounded edges */
}

/* Style for the bubble tooltip */
.tooltip {
  width: 100%;
  position: absolute;
  top: -100%; /* Initially hidden above the container */
  left: 50%;
  transform: translateX(-50%);
  padding: 0.6em 1em;
  opacity: 0;
  visibility: hidden;
  pointer-events: none;
  transition: all 0.1s;
  border-radius: var(--bubble-size);
  background: var(--background-light);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* Triangle arrow for the bubble tooltip */
.tooltip::before {
  content: "";
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translate(-50%);
  border-style: solid;
  border-width: 8px 8px 0;
  border-color: var(--background-light) transparent transparent;
}

/* Tooltip appearance on hover */
.tooltip-container:hover {
  background: var(--background-dark);
  color: var(--text-color-dark);
  box-shadow: 0 0 20px var(--glow-color); /* Brighter glow effect */
}

.tooltip-container:hover .tooltip {

  top: -100%; /* Adjusted position for the bubble tooltip */
  opacity: 1;
  visibility: visible;
  pointer-events: auto;
}
</style>