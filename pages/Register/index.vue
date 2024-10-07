<template>
    <div class="container">
        <h1>{{ name }}</h1>
        <h1>{{ email }}</h1>
        <h1>{{ password }}</h1>
        <form @submit.prevent="callApi">
            <input v-model="name" name="name" placeholder="name" type="text" />
            <input v-model="email" name="email" placeholder="email" type="text" />
            <input v-model="password" name="password" placeholder="mật khẩu" type="password" />
            <v-btn type="submit">Gửi</v-btn>
        </form>
        <v-btn color="green">
            <NuxtLink class="white--text text-decoration-none" to="/">
                Home page
            </NuxtLink>
        </v-btn>
    </div>
</template>

<script setup>
import { useContext } from '@nuxtjs/composition-api';
import { ref } from 'vue';
const { $axios } = useContext(); // Truy cập vào axios từ context của Nuxt

const name = ref('');
const email = ref('');
const password = ref('');

const callApi = async () => {
    try {
        const result = await $axios.post('/auth/register', {
            name: name.value,
            email: email.value,
            password: password.value
        });
        alert('registration successful')
        console.log('result:', result);
    } catch (err) {
        console.log('Error:', err);
    }
};
</script>
