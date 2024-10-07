<template>
    <div style="color:aliceblue">
        <!-- Nội dung để hiển thị danh sách users sau khi API được gọi -->
        <ul>
            <li v-for="user in users" :key="user.id">{{ user.name }}</li>
        </ul>
        cc
    </div>
</template>

<script setup>
import { useContext, onMounted } from '@nuxtjs/composition-api';
import { ref } from 'vue';

const { $axios } = useContext();  // Truy cập vào axios từ context của Nuxt

const users = ref([]);  // Biến để lưu danh sách users

// Hàm gọi API tìm tất cả users
const callApi = async () => {
    try {
        const result = await $axios.post('/user/find');
        console.log('Users found:', result.data);

        // Lưu danh sách users vào biến users
        users.value = result.data;
    } catch (err) {
        console.log('Error:', err);
    }
};

// Gọi hàm callApi ngay khi component được mounted
onMounted(() => {
    callApi();
});
</script>
