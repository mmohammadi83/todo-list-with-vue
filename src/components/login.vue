<script setup>
    import {ref} from 'vue'
    import navbar from './navbar.vue';
    let login = ref(true);
    function make_login(){
        login.value = !login.value;
    }

    

</script>
<template>
    <navbar/>
    <div class="todo_text">
        <p >todo list</p>
        <h1>login</h1>
    </div>
    <div class="login_form">
        <form action="#">
            <input type="email" name="email" placeholder="email">
            <input type="password" name="password" placeholder="password">
            <div id="login_button">
                <input type="button" value="exit">
                <input type="button" value="login">
            </div>
            <p>are you have not an account? <a >create account</a></p>
        </form>
    </div>
</template>