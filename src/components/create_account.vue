<script setup>
    import navbar from './navbar.vue';
</script>
<template>
    <navbar/>
    <div class="todo_text">
        <p >todo list</p>
        <h1 id="create">create account</h1>
    </div>
    <div class="login_form">
        <form action="#">
            <input type="email" name="email" placeholder="email">
            <input type="password" name="password" placeholder="password">
            <input type="password" name="con_password" placeholder="confirm password">
            <div id="login_button">
                <input type="button" value="exit">
                <input type="button" value="login">
            </div>
            <p>are you have an account? <a >login</a></p>
        </form>
    </div>
</template>