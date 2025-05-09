<script setup>
import { ref } from "vue";
let text = ref('');
let title = ref('');
let iseditmode = ref(false);
const reverse = ()=> {
  iseditmode.value = !iseditmode.value;
}
class note{
    constructor(title , text){
      this.title = title
      this.text = text
    }
  }
const emit= defineEmits(['data']);

function savefunc(){
  if(text.value == ''){
    alert('the text cant be empty');
  }
  else{
    const node = new note(title.value , text.value);
    emit('data' , node);
    text.value = '';
    title.value = '';
    reverse();
    
  }
}

function cancelfunc(){
  text.value = '';
  title.value = '';
  reverse();
}


</script>
<template>
  <Transition>
    <div v-if="iseditmode" class="matte">
      <div class="text_box">
        <input v-model="title" type="text" placeholder="title ">
        <textarea v-model="text" name="note"></textarea>
        <div class="buttons">
          <button @click="savefunc()">save</button>
          <button @click="cancelfunc()">cancel</button>
        </div>
      </div>
    </div>

  </Transition>
  <button @click="reverse()" class="addnote">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      width="70"
      height="70"
      viewBox="0 0 512 512"
    >
      <path
        fill="none"
        stroke="#008000ff"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="32"
        d="M256 112v288m144-144H112"
      />
    </svg>
  </button>
</template>

<style lang="sass">
.v-enter-active,
.v-leave-active 
  transition: opacity 0.2s ease


.v-enter-from,
.v-leave-to 
  opacity: 0

</style>