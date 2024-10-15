<template>
  <v-container class="grid">
    <v-row>
      <v-col cols="12" sm="3">
        <v-list>
          <v-list-item>
            <v-list-item-content>Tài Khoản Của Tôi</v-list-item-content>
          </v-list-item>
          <v-list-item v-for="(item, index) in menuItems" :key="index">
            <v-list-item-content>{{ item }}</v-list-item-content>
          </v-list-item>
        </v-list>
      </v-col>

      <v-col cols="12" sm="9">
        <v-card class="pa-4">
          <v-card-title>Hồ Sơ Của Tôi</v-card-title>
          <v-card-subtitle>Quản lý thông tin hồ sơ để bảo mật tài khoản</v-card-subtitle>
          <v-divider></v-divider>

          <v-card-text>
            <v-form class="profile-form">
              <div class="left-column">
                <p>Tên đăng nhập</p>
                <p class="mb-4">Tên</p>
                <p>Email</p>
                <p>Số Điện Thoại</p>
                <p>Giới tính</p>
                <p class="mb-0">Ngày sinh</p>
              </div>
              <div class="right-column">
                <p>hoangphuc__</p>
                <v-text-field v-model="name" :rules="[rules.required]" dense outlined hide-details></v-text-field>
                <a href="#" @click.prevent="gotoEmail">Thêm</a>
                <p class="mt-2">
                  *********52
                  <a href="#" @click.prevent="goToPhone">Thay Đổi</a>
                </p>
                <v-radio-group v-model="gender" row>
                  <v-radio label="Nam" value="male"></v-radio>
                  <v-radio label="Nữ" value="female"></v-radio>
                  <v-radio label="Khác" value="other"></v-radio>
                </v-radio-group>
                <v-row>
                  <v-col cols="4">
                    <v-select v-model="selectedDay" :items="days" dense outlined hide-details></v-select>
                  </v-col>
                  <v-col cols="4">
                    <v-select v-model="selectedMonth" :items="months" dense outlined hide-details></v-select>
                  </v-col>
                  <v-col cols="4">
                    <v-select v-model="selectedYear" :items="years" dense outlined hide-details></v-select>
                  </v-col>
                </v-row>
              </div>
            </v-form>
          </v-card-text>

          <div class="text-center">
            <v-avatar size="100">
              <img
                src="https://storage.googleapis.com/a1aa/image/HCTfYQcAmS0kb6O69PiMZd1vefE2rM1rhFqGROhZISpQUQJnA.jpg"
                alt="Profile picture"
              />
            </v-avatar>
            <v-btn color="primary" class="mt-3">Chọn Ảnh</v-btn>
            <p class="caption grey--text">
              Dung lượng file tối đa 1 MB
              <br />Định dạng: .JPEG, .PNG
            </p>
          </div>

          <v-btn color="orange" class="mt-4" @click="saveProfile">Lưu</v-btn>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      phone: "",
      gender: "",
      selectedDay: null,
      selectedMonth: null,
      selectedYear: null,
      rules: {
        required: value => !!value || "Vui lòng nhập tên"
      },
      days: Array.from({ length: 31 }, (v, k) => k + 1),
      months: [
        "Tháng 1",
        "Tháng 2",
        "Tháng 3",
        "Tháng 4",
        "Tháng 5",
        "Tháng 6",
        "Tháng 7",
        "Tháng 8",
        "Tháng 9",
        "Tháng 10",
        "Tháng 11",
        "Tháng 12"
      ],
      years: Array.from({ length: 100 }, (v, k) => 2024 - k),
      menuItems: [
        "Hồ Sơ",
        "Ngân Hàng",
        "Địa Chỉ",
        "Đổi Mật Khẩu",
        "Cài Đặt Thông Báo",
        "Những Thiết Lập Riêng Tư"
      ]
    };
  },
  methods: {
    goToPhone() {
      this.$router.push("/phone");
    },
    gotoEmail() {
      this.$router.push("/email");
    },
    saveProfile() {
      // Logic to save profile
    }
  }
};
</script>

<style scoped>
.grid {
  max-width: 1200px;
  margin: 0 auto;
}

li {
  list-style: none;
  margin: 10px 0;
}

.left-column {
  margin-right: 30px;
}

.right-column {
  flex-grow: 1;
}

.profile-form {
  display: flex;
  justify-content: space-between;
}

.v-application .v-avatar {
  background-color: #e9e9e9;
}

.v-btn {
  width: 100px;
}
</style>