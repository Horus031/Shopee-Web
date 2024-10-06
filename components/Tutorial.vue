<template>
    <div>
        <h1 style="color:wheat">{{ email }}</h1>
        <h1 style="color:wheat">{{ password }}</h1>
        <form @submit.prevent="callApi">
            <input v-model="email" name="email" style="color:aliceblue" placeholder="email" type="text" />
            <input v-model="password" name="password" style="color:aliceblue" placeholder="mật khẩu" type="password" />
            <v-btn type="submit" style="color:aliceblue">Gửi</v-btn>
            <h1 style="color:aliceblue">cc</h1>
        </form>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import axios from 'axios'; // Import axios directly

const email = ref('sycc@gmail.com');
const password = ref('sadasdasd');

const callApi = async () => {
    try {
        const { data } = await axios.post('http://localhost:3000/auth/login', {
            email: email.value,
            password: password.value,
        });
        console.log('Data received:', data);
    } catch (err) {
        console.error('Error:', err);
    }
};



</script>
