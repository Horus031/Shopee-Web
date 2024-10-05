<template>
    <v-app light >
        <header class="header" style="height: 120px; background-image: linear-gradient(-180deg, #f53d2d, #f63)">
            <div class="grid">
                <nav class="header__navbar d-flex justify-space-between">
                    <v-list style="background-color: transparent;" class="pa-0">
                        <v-list-item class="pa-0 mt-n2" >
                            <v-list-item-content class="pa-0 ">
                                <v-list-item-title style="width: fit-content;" class="header__navbar-item header__navbar-item--separator">
                                    <v-hover v-slot="{ hover }">
                                        <a href="" 
                                        style="font-size: 14px;" 
                                        class="text-decoration-none pa-2"
                                        :style="hover ? 'color:#ffffffb3' : 'color:#fff'"
                                    >
                                        Kênh Người Bán
                                    </a>
                                    </v-hover>
                                </v-list-item-title>
                            </v-list-item-content>
                            <v-list-item-content class="pa-0 ">
                                <v-list-item-title style="width: fit-content;" class="header__navbar-item header__navbar-item--separator">
                                    <v-hover v-slot="{ hover }">
                                        <a href="" 
                                        style="font-size: 14px;" 
                                        class="text-decoration-none pa-2"
                                        :style="hover ? 'color:#ffffffb3' : 'color:#fff'"
                                    >
                                        Trở thành Người bán Shopee
                                    </a>
                                    </v-hover>
                                </v-list-item-title>
                            </v-list-item-content>
                            <v-list-item-content class="pa-0" >
                                <v-list-item-title style="width: fit-content;" class="header__navbar-item header__navbar-item--separator">
                                    <v-hover v-slot="{ hover }">
                                        <a href="" 
                                        style="font-size: 14px;" 
                                        class="text-decoration-none pa-2"
                                        :style="hover ? 'color:#ffffffb3' : 'color:#fff'"
                                    >
                                        Tải ứng dụng
                                    </a>
                                    </v-hover>
                                </v-list-item-title>
                            </v-list-item-content>
                            <v-list-item-content class="pa-0" >
                                <v-list-item-title style="width: fit-content;" class="header__navbar-item">
                                    <span href="" style="font-size: 14px; color: white;" class="text-decoration-none py-2 pl-2 pr-1">Kết nối</span>
                                    <a href="" style="margin-top: -1px; margin-right: 6px;">
                                        <v-icon dense color="white">mdi mdi-facebook</v-icon>
                                    </a>

                                    <a href="" style="margin-top: -1px;">
                                        <v-icon dense color="white">mdi mdi-instagram</v-icon>
                                    </a>



                                </v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>
                    </v-list>

                    <v-list style="background-color: transparent;" class="pa-0">
                        <v-list-item class="pa-0 mt-n2" >
                            <v-list-item-content class="pa-0 ">
                                <v-list-item-title style="width: fit-content;" class="header__navbar-item d-flex align-center pa-2">
                                    <a href="" class="pt-1">
                                        <svg style="width: 14px; height: 18px;" viewBox="3 2.5 14 14" x="0" y="0" class="shopee-svg-icon icon-help-center"><path d="m17 15.6-.6-1.2-.6-1.2v-7.3c0-.2 0-.4-.1-.6-.3-1.2-1.4-2.2-2.7-2.2h-1c-.3-.7-1.1-1.2-2.1-1.2s-1.8.5-2.1 1.3h-.8c-1.5 0-2.8 1.2-2.8 2.7v7.2l-1.2 2.5-.2.4h14.4zm-12.2-.8.1-.2.5-1v-.1-7.6c0-.8.7-1.5 1.5-1.5h6.1c.8 0 1.5.7 1.5 1.5v7.5.1l.6 1.2h-10.3z"></path><path d="m10 18c1 0 1.9-.6 2.3-1.4h-4.6c.4.9 1.3 1.4 2.3 1.4z"></path></svg>  
                                    </a>
                                    <a
                                    href="" 
                                    style="font-size: 14px;"
                                    class="text-decoration-none pa-1 white--text"
                                    >   
                                    Thông báo
                                    </a>
                                </v-list-item-title>
                            </v-list-item-content>
                            <v-list-item-content class="pa-0 ">
                                <v-list-item-title style="width: fit-content;" class="header__navbar-item d-flex align-center pa-2">
                                    <a href="" class="pt-1">
                                        <svg style="color: white;" height="16" viewBox="0 0 16 16" width="16" class="shopee-svg-icon icon-help-center"><g fill="none" fill-rule="evenodd" transform="translate(1)"><circle cx="7" cy="8" r="7" stroke="currentColor"></circle><path fill="currentColor" d="m6.871 3.992c-.814 0-1.452.231-1.914.704-.462.462-.693 1.089-.693 1.892h1.155c0-.484.099-.858.297-1.122.22-.319.583-.473 1.078-.473.396 0 .715.11.935.33.209.22.319.517.319.902 0 .286-.11.55-.308.803l-.187.209c-.682.605-1.1 1.056-1.243 1.364-.154.286-.22.638-.22 1.045v.187h1.177v-.187c0-.264.055-.506.176-.726.099-.198.253-.396.462-.572.517-.451.825-.737.924-.858.275-.352.418-.803.418-1.342 0-.66-.22-1.188-.66-1.573-.44-.396-1.012-.583-1.716-.583zm-.198 6.435c-.22 0-.418.066-.572.22-.154.143-.231.33-.231.561 0 .22.077.407.231.561s.352.231.572.231.418-.077.572-.22c.154-.154.242-.341.242-.572s-.077-.418-.231-.561c-.154-.154-.352-.22-.583-.22z"></path></g></svg>
                                    </a>
                                    <a href="" style="font-size: 14px;" class="text-decoration-none pa-1 white--text">Hỗ trợ</a>
                                </v-list-item-title>
                            </v-list-item-content>
                            <v-list-item-content class="pa-0" >
                                <v-list-item-title style="width: fit-content;" class="header__navbar-item d-flex align-center pa-2">
                                    <a href="" class="pt-1">
                                        <svg style="color: white;" width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M8.00065 14.6667C11.6825 14.6667 14.6673 11.6819 14.6673 8.00004C14.6673 4.31814 11.6825 1.33337 8.00065 1.33337C4.31875 1.33337 1.33398 4.31814 1.33398 8.00004C1.33398 11.6819 4.31875 14.6667 8.00065 14.6667Z" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"></path><path d="M5.33464 8.00004C5.33464 11.6819 6.52854 14.6667 8.0013 14.6667C9.47406 14.6667 10.668 11.6819 10.668 8.00004C10.668 4.31814 9.47406 1.33337 8.0013 1.33337C6.52854 1.33337 5.33464 4.31814 5.33464 8.00004Z" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"></path><path d="M1.33398 8H14.6673" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"></path></svg>
                                    </a>
                                    <a href="" style="font-size: 14px;" class="text-decoration-none pa-1 white--text">
                                        Tiếng Việt
                                        <v-icon dense color="white">mdi mdi-chevron-down</v-icon>
                                    </a>
                                </v-list-item-title>
                            </v-list-item-content>
                            <v-list-item-content class="pa-0" >
                                <v-list-item-title style="width: fit-content;" class="header__navbar-item d-flex align-center">
                                    <span href="" style="font-size: 14px;" class="text-decoration-none pa-2 white--text header__navbar-item--separator">Đăng ký</span>
                                </v-list-item-title>
                            </v-list-item-content>
                            <v-list-item-content class="pa-0" >
                                <v-list-item-title style="width: fit-content;" class="header__navbar-item white--text d-flex align-center">
                                    <span href="" style="font-size: 14px;" class="text-decoration-none pa-2">Đăng nhập</span>
                                </v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>
                    </v-list>

                    
                </nav>    
            </div>
        </header>
    </v-app>
</template>

<script>
  export default {
    data () {
      return 
    }
  }
</script>

<style scoped>

:root {
    --white-color: #fff;
    --black-color: #000;
    --text-color: #333;
    --star-gold-color: #ffce3e;
    --primary-color: #ee4d2d;
    --border-color: #dbdbdb;
    --navbar-height: 34px;
    --header-height: 120px;
    --header-with-search-height: calc(var(--header-height) - var(--navbar-height));
}

* {
    box-sizing: inherit;
}

.grid {
    width: 1200px;
    max-width: 100%;
    margin: 0 auto;
}

.v-list-item__title, .v-list-item__subtitle {
    overflow: visible !important;
}

.v-list-item__content {
    flex: none;
}

.header__navbar-item--separator::after {
    content: "";
    display: block;
    position: absolute;
    width: 1px;
    height: 13px;
    background-color: #fb9086;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
}

.header__navbar-item {
    position: relative;
}

a:not(.on-hover) {
    fill: #fff;
 }

</style>