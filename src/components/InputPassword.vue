<script setup>
import { ref, computed } from 'vue';
    const password = ref('password');
   
    function changePass(){
        (password.value == `password`) ? password.value = 'name': password.value = 'password';
    }
    
</script>

<template>
    <div class="container text-center input-password">
        <h1 class="my-3">Exercise Input Password</h1>
        <input :type="password" name="" id="password" class="form-control">
        <div class="d-block">
            <span id="show-password" class="mt-2 btn btn-primary" @click="changePass()">Show Password</span>
        </div>
    </div>
</template>

<style lang="css" scoped>
    #show-password:hover {
        cursor: pointer;
        user-select: none;
    }
</style>