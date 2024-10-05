<template>
  <v-container class="grid">
    <v-row>
      <v-col cols="12" md="2">
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>Tài Khoản Của Tôi</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item v-for="(item, index) in menuItems" :key="index">
            <v-list-item-title>{{ item }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-col>

      <v-col col="12" md="10">
        <v-card>
          <v-card-title>Hồ sơ của tôi</v-card-title>
          <v-card-subtitle>Quản lý thông tin hồ sơ để bảo mật tài khoản</v-card-subtitle>
          <v-divider insert></v-divider>
          <v-card-text>
            <v-form>
              <!--Username-->
              <div>
                <v-row>
                  <v-col cols="4">
                    <p>Tên đăng nhập</p>
                  </v-col>
                </v-row>
              </div>
              <!--Name-->
              <v-row class="align-center">
                <v-col cols="2">
                  <p class="mb-0">Tên</p>
                </v-col>
                <v-col cols="8">
                  <v-text-field
                    v-model="name"
                    :rules="[rules.required]"
                    required
                    dense
                    single-line
                    outlined
                  ></v-text-field>
                </v-col>
              </v-row>
              <!--Email-->
              <v-row>
                <v-col cols="2">
                  <p>Email</p>
                </v-col>
                <v-col cols="8">
                  <a href="email.vue" @click.prevent="gotoEmail">Thêm</a>
                </v-col>
              </v-row>
              <!--Phone-->
              <v-row>
                <v-col cols="2">
                  <p>Số Điện Thoại</p>
                </v-col>
                <v-col cols="8">
                  <a href="phone.vue" @click.prevent="gotoPhone">Thay đổi</a>
                </v-col>
              </v-row>
              <!--Gender-->
              <v-row>
                <v-col cols="2">
                  <p>Giới tính</p>
                </v-col>
                <v-col cols="8">
                  <v-radio-group v-model="gender" row>
                    <v-radio label="Nam" value="male"></v-radio>
                    <v-radio label="Nữ" value="female"></v-radio>
                    <v-radio label="Khác" value="other"></v-radio>
                  </v-radio-group>
                </v-col>
              </v-row>
              <!--Birthday-->
              <v-row class="align-center">
                <v-col cols="2">
                  <p class="mb-0">Ngày sinh</p>
                </v-col>
                <v-col cols="2">
                  <v-select v-model="selectedDay" :items="days" label="Ngày" dense outlined></v-select>
                </v-col>
                <v-col cols="2">
                  <v-select
                    v-model="selectedMonth"
                    :items="months"
                    label="Tháng"
                    dense
                    outlined
                    @change="onMonthOrYearChange"
                  ></v-select>
                </v-col>
                <v-col cols="2">
                  <v-select
                    v-model="selectedYear"
                    :items="years"
                    label="Năm"
                    dense
                    outlined
                    @change="onMonthOrYearChange"
                  ></v-select>
                </v-col>
              </v-row>
            </v-form>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      rules: {
        required: value => !!value || "Vui lòng nhập tên"
      },
      menuItems: [
        "Hồ Sơ",
        "Ngân Hàng",
        "Địa Chỉ",
        "Đổi Mật Khẩu",
        "Cài Đặt Thông Báo",
        "Những Thiết Lập Riêng Tư"
      ],
      selectedDay: null,
      selectedMonth: null,
      selectedYear: null,
      // Mảng chứa các giá trị cho ngày
      days: [],
      // Mảng các tháng
      months: [
        { text: "Tháng 1", value: 1 },
        { text: "Tháng 2", value: 2 },
        { text: "Tháng 3", value: 3 },
        { text: "Tháng 4", value: 4 },
        { text: "Tháng 5", value: 5 },
        { text: "Tháng 6", value: 6 },
        { text: "Tháng 7", value: 7 },
        { text: "Tháng 8", value: 8 },
        { text: "Tháng 9", value: 9 },
        { text: "Tháng 10", value: 10 },
        { text: "Tháng 11", value: 11 },
        { text: "Tháng 12", value: 12 }
      ],
      // Mảng chứa các năm (hiện tại lùi về trước 100 năm)
      years: Array.from({ length: 100 }, (_, i) => new Date().getFullYear() - i)
    };
  },
  methods: {
    goToPhone() {
      this.$router.push("/phone");
    },
    gotoEmail() {
      this.$router.push("/email");
    },
    getDaysInMonth(month, year) {
      if (!month || !year) return []; // Nếu chưa chọn tháng hoặc năm, không hiển thị ngày
      const daysInMonth = new Date(year, month, 0).getDate(); // Lấy số ngày của tháng
      return Array.from({ length: daysInMonth }, (_, i) => i + 1); // Tạo mảng ngày
    },
    onMonthOrYearChange() {
      if (this.selectedMonth && this.selectedYear) {
        this.days = this.getDaysInMonth(this.selectedMonth, this.selectedYear); // Cập nhật số ngày theo tháng và năm
        this.selectedDay = null; // Reset lại ngày đã chọn (nếu trước đó đã chọn)
      }
    },
    created() {
      // Khởi tạo mảng ngày ban đầu là rỗng
      this.days = [];
    }
  }
};
</script>

<style>
.grid {
  width: 1200px;
  max-width: 100%;
  margin: 0 auto;
}
</style>