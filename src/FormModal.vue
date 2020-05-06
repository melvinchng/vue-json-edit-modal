<template>
  <div class="modal-window"> 
    <div>
      <h1>Edit</h1>
      <form class="pure-form">
        <div class="pure-u-1">
          <textarea v-if="type == 'key'"
            class="pure-input-1" 
            rows="5" 
            v-model="data.name" 
          />

          <input v-if="type == 'value' && data.type == 'number'"
            v-model.number="data.remark"
            type="number"
            class="pure-input-1"
          />

          <textarea v-if="type == 'value' && data.type == 'string'"
            class="pure-input-1" 
            rows="5" 
            v-model="data.remark" 
          />
        </div>

        <div style="padding-top: 10px">
          <button type="button" class="pure-button pure-button-primary" @click="$emit('close')">Close</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "FormModal",
  props: {
    data: [Object, String, Number, Boolean],
    type: String,
  }
}
</script>

<style scoped>
.modal-window {
  position: fixed;
  background-color: rgba(200, 200, 200, 0.75);
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 999;
  opacity: 1;
  pointer-events: auto;
  -webkit-transition: all 0.3s;
  -moz-transition: all 0.3s;
  transition: all 0.3s;
}

.modal-window>div {
  width: 400px;
  position: relative;
  margin: 10% auto;
  padding: 2rem;
  background: #fff;
  color: #444;
}

.modal-window header {
  font-weight: bold;
}

.modal-close {
  color: #aaa;
  line-height: 50px;
  font-size: 80%;
  position: absolute;
  right: 0;
  text-align: center;
  top: 0;
  width: 70px;
  text-decoration: none;
}

.modal-close:hover {
  color: #000;
}

.modal-window h1 {
  font-size: 150%;
  margin: 0 0 15px;
}
</style>