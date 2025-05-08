<script setup>
    import {ref} from 'vue'
    let text = ref('');
    
</script>
<template>
    <div class="matte">
        <div class="text_box">
            <textarea  name="note"></textarea>
            <div class="buttons">
                <button>save</button>
                <button>cancel</button>

            </div>
        </div>
    </div>
</template>