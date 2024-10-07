<template>
    <div class="container">
        <div>
            <!-- Form đăng nhập -->
            <h1>{{ email }}</h1>
            <h1>{{ password }}</h1>
            <form @submit.prevent="callApi">
                <input style="color: black;" v-model="email" name="email" placeholder="email" type="text" />
                <input style="color: black;" v-model="password" name="password" placeholder="mật khẩu"
                    type="password" />
                <v-btn color="blue" type="submit">Đăng nhập</v-btn>
            </form>

            <v-btn color="green">
                <NuxtLink class="white--text text-decoration-none" to="/">Home page</NuxtLink>
            </v-btn>
        </div>

        <!-- Render token khi nhận được -->
        <div>
            <h5>Token: {{ token2 }}</h5>
        </div>

        <!-- Tìm kiếm tất cả người dùng -->
        <div v-show="token2">
            <h2>Tìm tất cả người dùng</h2>
            <v-btn color="blue" @click="findAllUsers">Tìm kiếm</v-btn>

            <!-- Hiển thị danh sách người dùng -->
            <div v-show="users.length">
                <h3>Danh sách người dùng:</h3>
                <template>
                    <v-simple-table dark>
                        <thead>
                            <tr>
                                <th class="text-left">
                                    Name
                                </th>
                                <th class="text-left">
                                    Email
                                </th>
                                <th class="text-left">
                                    Action
                                </th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr v-for="item in users" :key="item.name">
                                <td>{{ item.name }}</td>
                                <td>{{ item.email }}</td>

                                <td><v-btn @click="clickToDelete(item._id)" color="white"
                                        class="black--text text-capitalize">delete</v-btn>
                                    <v-btn @click="clickToUpdate(item._id)" color="white"
                                        class="black--text text-capitalize">Update</v-btn>
                                </td>
                            </tr>
                        </tbody>
                    </v-simple-table>
                    <v-dialog class="hidden" transition="dialog-bottom-transition" max-width="600">
                        <template v-slot:activator="{ on, attrs }">
                            <v-btn color="primary" v-bind="attrs" v-on="on">From the bottom</v-btn>
                        </template>
                        <template v-slot:default="dialog">
                            <v-card>
                                <v-toolbar color="primary" dark>Opening from the bottom</v-toolbar>
                                <v-card-text>
                                    <div> <v-text-field placeholder="update user" /></div>
                                </v-card-text>
                                <v-card-actions class="justify-end">
                                    <v-btn text @click="dialog.value = false">Close</v-btn>
                                </v-card-actions>
                            </v-card>
                        </template>
                    </v-dialog>
                    <v-btn v-show="token2" color="green">
                        <NuxtLink class="white--text text-decoration-none" to="/">Products</NuxtLink>
                    </v-btn>
                </template>

            </div>
        </div>
    </div>
</template>
<script>
import { mapFields } from "vuex-map-fields"
export default {

    computed: {
        ...mapFields('storeToken', ['tokenNe'])

    },
    data() {
        return {
            email: '',
            password: '',
            token2: '',  // Biến lưu token
            users: [],   // Lưu danh sách người dùng
        };
    },
    methods: {
        // Hàm tiện ích để thiết lập Authorization header
        setAuthToken(token) {
            this.$axios.defaults.headers.common['Authorization'] = `Bearer ${token}`;
        },
        // Hàm gọi API đăng nhập và lưu token
        async callApi() {
            try {
                const result = await this.$axios.post('/auth/login', {
                    email: this.email,
                    password: this.password,
                });

                // Lưu token vào biến
                this.token2 = result.data.token;
                let store = this.tokenNe
                store = result.data.token
                console.log(store, 'ccc')
                console.log("🚀 ~ callApi ~ token2:", this.token2);

                // Thiết lập Authorization header cho axios
                this.setAuthToken(this.token2);

            } catch (err) {
                console.log('Error:', err);
            }
        },
        // Hàm tìm tất cả người dùng
        async findAllUsers() {
            try {
                // Gọi setAuthToken trước khi gọi API nếu cần
                this.setAuthToken(this.token2);

                const response = await this.$axios.post('/user/find');  // Gửi yêu cầu tới API
                this.users = response.data;  // Lưu danh sách người dùng
                console.log("🚀 ~ findAllUsers ~ users:", this.users);
            } catch (err) {
                console.log('Error fetching users:', err);
            }
        },
        // Hàm xóa người dùng
        async clickToDelete(id) {
            try {
                // Gọi setAuthToken trước khi gọi API nếu cần
                this.setAuthToken(this.token2);

                const response = await this.$axios.post(`/user/delete/${id}`);  // Gửi yêu cầu xóa người dùng
                this.users = response.data;  // Lưu danh sách người dùng cập nhật
                console.log('Deleted user with ID:', id);
            } catch (err) {
                console.log('Error deleting user:', err);
            }
        },
        // Hàm cập nhật người dùng
        async clickToUpdate(id) {
            // Cập nhật người dùng theo ID
            console.log('Update user with ID:', id);
        }
    }
};
</script>

<style scoped>
.hidden {
    display: none;
}
</style>