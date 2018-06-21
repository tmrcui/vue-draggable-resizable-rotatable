<template>
  <div id="app">
    <div style="height: 500px; width: 500px; margin: 20px; border: 1px solid red; position: relative;">
      <button class="button1">cancel deselect 1</button>
      <button class="button2">cancel deselect 2</button>
      <VueDraggableResizableRotatable :x="50" :y="50" :w="400" :h="400" :parent="true" deselectCancel=".button1,.button2">
        <p>Component</p>
      </VueDraggableResizableRotatable>
    </div>
    <div style="height: 500px; width: 500px; margin: 20px; border: 1px solid red; position: relative;">
      <h2>Grid 30x30</h2>
      <VueDraggableResizableRotatable :x="50" :y="50" :w="400" :h="400" :grid="[30, 30]" :parent="true">
        <p>Component</p>
      </VueDraggableResizableRotatable>
    </div>
    <div style="height: 500px; width: 500px; margin: 20px; border: 1px solid red; position: relative;">
      <h2>Custom handler</h2>
      <VueDraggableResizableRotatable :x="50" :y="50" :w="150" :h="50" :parent="true" :resizable="false" :dragHandle="'.dragHandle'">
        <p>Component</p>
        <span class="dragHandle">
          =
        </span>
      </VueDraggableResizableRotatable>
    </div>
    <div style="height: 500px; width: 500px; margin: 20px; border: 1px solid red; position: relative;">
      <h2>Grid 30x30 and handler</h2>
      <VueDraggableResizableRotatable :x="50" :y="50" :w="150" :h="50" :parent="true" :grid="[30, 30]" :resizable="false" :dragHandle="'.dragHandle'">
        <p>Component</p>
        <span class="dragHandle">
          =
        </span>
      </VueDraggableResizableRotatable>
    </div>
  </div>
</template>

<script>
import VueDraggableResizableRotatable from './components/vue-draggable-resizable-rotatable'
export default {
  name: 'app',
  components: {
    VueDraggableResizableRotatable
  }
}
</script>

<style>
  h2 {
    opacity: 0.3;
    padding: 0 0 0 20px;
    z-index: -1;
  }
  .dragHandle {
    position: absolute;
    top: 0;
    right: 0;
    padding: 5px;
    font-size: 20px;
    background-color: lightgrey;
  }
  .vdr {
    background: white;
  }
</style>
