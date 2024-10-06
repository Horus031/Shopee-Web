<template>
    <div>
        cc
        <h1>Data from API</h1>
        <li v-for="post in posts" :key="post.id">{{ post.title }}</li>
    </div>
    </div>
</template>

<script>
export default {
    async asyncData({ $axios }) {
        try {
            const posts = await $axios.$post('/user/find'); // Sử dụng $get để gọi API
            console.log(posts);
            return { posts };
        } catch (error) {
            console.error('Error fetching posts:', error);
            return { posts: [] }; // Trả về mảng rỗng nếu có lỗi
        }
    },
}
</script>
