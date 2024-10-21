<template>
    <div>
        <nav class="header__navbar d-flex justify-space-between" style="height:34px">
            <v-list class="pa-0" color="transparent">
                <v-list-item class="pa-0 mt-n2" >
                    <v-list-item-content class="pa-0 ">
                        <v-list-item-title class="header__navbar-item header__navbar-item--separator">
                            <v-hover v-slot="{ hover }">
                                <a href="" 
                                style="font-size: 13px;" 
                                class="text-decoration-none pa-2"
                                :style="hover ? 'color:#ffffffb3' : 'color:#fff'"
                            >
                                Kênh Người Bán
                            </a>
                            </v-hover>
                        </v-list-item-title>
                    </v-list-item-content>
                    <v-list-item-content class="pa-0 ">
                        <v-list-item-title class="header__navbar-item header__navbar-item--separator">
                            <v-hover v-slot="{ hover }">
                                <a href="" 
                                style="font-size: 13px;" 
                                class="text-decoration-none pa-2"
                                :style="hover ? 'color:#ffffffb3' : 'color:#fff'"
                            >
                                Trở thành Người bán Shopee
                            </a>
                            </v-hover>
                        </v-list-item-title>
                    </v-list-item-content>
                    <v-list-item-content class="pa-0" >
                        <v-list-item-title class="header__navbar-item header__navbar-item--separator">
                            <v-menu
                                open-on-hover
                                bottom
                                offset-y
                            >
                                <template v-slot:activator="{ on, attrs }">
                                    <v-hover v-slot="{ hover }">
                                        <a
                                            href=""
                                            style="font-size: 13px; position:relative;"
                                            class="text-decoration-none pa-2 d-inline-block"
                                            :style="hover ? 'color:#ffffffb3' : 'color:#fff'"
                                            v-bind="attrs"
                                            v-on="on"
                                        >
                                            Tải ứng dụng
                                        </a>
                                    </v-hover>
                                </template>

                                <v-list class="pa-0">
                                    <v-list-item class="pa-0">
                                        <v-list-item-content style="max-width:180px">
                                            <v-img
                                                src="https://deo.shopeemobile.com/shopee/shopee-pcmall-live-sg/assets/5b6e787c2e5ee052.png"
                                                height="180px"
                                            >
                                            </v-img>

                                            <v-sheet 
                                                color="transparent" 
                                                class="d-flex justify-space-between flex-wrap" 
                                                style="padding: 0 15px 5px 15px;"
                                            >
                                                <div class="pt-1">
                                                    <v-img
                                                        class="d-flex"
                                                        :src="require('@/assets/img/appstore_qrcode.png')"
                                                        height="18px"
                                                        width="70px"
                                                        position="left center"
                                                        contain
                                                    >
                                                    </v-img>
                                                </div>
                                                <div class="pt-1">
                                                    <v-img
                                                        class="d-flex"
                                                        :src="require('@/assets/img/googleplay_qrcode.png')"
                                                        height="18px"
                                                        width="70px"
                                                        position="left center"
                                                        contain
                                                    >
                                                    </v-img>
                                                </div>
                                                <div class="pt-1">
                                                    <v-img
                                                        class="d-flex"
                                                        :src="require('@/assets/img/appgallery_qrcode.png')"
                                                        height="18px"
                                                        width="70px"
                                                        position="left center"
                                                        contain
                                                    >
                                                    </v-img>
                                                </div>
                                            </v-sheet>
                                        </v-list-item-content>
                                    </v-list-item>
                                </v-list>
                            </v-menu>
                        </v-list-item-title>
                    </v-list-item-content>
                    <v-list-item-content class="pa-0" >
                        <v-list-item-title class="header__navbar-item">
                            <span 
                                class="text-decoration-none py-2 pl-2"
                                style="font-size: 13px; 
                                color: white;" 
                            >
                                Kết nối
                            </span>
                            <a href="" style="margin-top: -1px;">
                                <v-icon dense color="white">mdi mdi-facebook</v-icon>
                            </a>

                            <a href="" style="margin-top: -1px;">
                                <v-icon dense color="white">mdi mdi-instagram</v-icon>
                            </a>



                        </v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>

            <v-list color="transparent" class="pa-0">
                <v-list-item class="pa-0 mt-n2" >
                    <v-list-item-content class="pa-0">
                        <v-list-item-title class="header__navbar-item d-flex align-center ">
                            <v-menu
                                transition="scale-transition"
                                origin="top right"
                                open-on-hover
                                bottom
                                offset-y
                                nudge-left="305"
                            >
                            
                                <template v-slot:activator="{ on, attrs }">
                                    <v-hover v-slot="{ hover }">
                                        <a 
                                            href="" 
                                            class="text-decoration-none white--text d-flex align-center pa-2"
                                            style="font-size: 13px;"
                                            :style="hover ? 'fill:#ffffffb3' : 'fill:#fff'"
                                            v-bind="attrs"
                                            v-on="on"
                                        >
                                            <svg 
                                                style="width: 18px; 
                                                height: 18px;" 
                                                viewBox="3 2.5 14 14" x="0" y="0" 
                                                class="pr-1"
                                            >
                                                <path d="m17 15.6-.6-1.2-.6-1.2v-7.3c0-.2 0-.4-.1-.6-.3-1.2-1.4-2.2-2.7-2.2h-1c-.3-.7-1.1-1.2-2.1-1.2s-1.8.5-2.1 1.3h-.8c-1.5 0-2.8 1.2-2.8 2.7v7.2l-1.2 2.5-.2.4h14.4zm-12.2-.8.1-.2.5-1v-.1-7.6c0-.8.7-1.5 1.5-1.5h6.1c.8 0 1.5.7 1.5 1.5v7.5.1l.6 1.2h-10.3z"></path>
                                                <path d="m10 18c1 0 1.9-.6 2.3-1.4h-4.6c.4.9 1.3 1.4 2.3 1.4z"></path>
                                            </svg>  
                                        
                                            <span :style="hover ? 'color:#ffffffb3' : 'color:#fff'">Thông báo</span>
                                        </a>
                                    </v-hover>
                                </template>

                                <v-list class="pa-0 d-flex align-center" width="400px" height="310px">
                                    <v-list-item class="pa-0 d-flex justify-center align-center ">
                                        <v-list-item-content>
                                            <v-img
                                                :src="require('@/assets/img/notify-nologin.png')"
                                                height="100px"
                                                width="100px"
                                                postion="center center"
                                                contain
                                            >
                                                
                                            </v-img>
                                            <v-list-item-title 
                                                class="subtitle-2 text-center font-weight-light mt-4"
                                            >
                                                Đăng nhập để xem Thông báo
                                            </v-list-item-title>
                                        </v-list-item-content>
                                    </v-list-item>
                                </v-list>
                                <v-list class="d-flex pa-0" color="white" height="40px" width="auto">
                                    <v-list-item class="pa-0">
                                        <v-list-item-content class="pa-0 col-12 mb-2">
                                            <v-btn 
                                                depressed 
                                                class="rounded-0 col-6 subtitle-2 font-weight-light text-capitalize"
                                                min-height="40px"
                                                to="/signup"
                                            >
                                                Đăng ký
                                            </v-btn>
                                            <v-btn 
                                                depressed 
                                                class="rounded-0 col-6 subtitle-2 font-weight-light text-capitalize"
                                                min-height="40px"
                                                to="/login"
                                            >
                                                Đăng nhập
                                            </v-btn>
                                        </v-list-item-content>
                                    </v-list-item>
                                </v-list>
                            </v-menu>
                        </v-list-item-title>
                    </v-list-item-content>
                    <v-list-item-content class="pa-0 ">
                        <v-list-item-title class="header__navbar-item d-flex align-center pa-2">
                            <v-hover v-slot="{ hover }">
                                <a 
                                    href="" 
                                    class="text-decoration-none white--text d-flex align-center"
                                    style="font-size: 13px;"
                                    :style="hover ? 'fill:#ffffffb3' : 'fill:#fff'"
                                >
                                    <svg height="22" viewBox="0 0 16 16" width="22" class="shopee-svg-icon icon-help-center pr-1">
                                        <g fill="none" fill-rule="evenodd" transform="translate(1)">
                                            <circle :style="hover ? 'stroke:#ffffffb3' : 'stroke:#fff'" cx="7" cy="8" r="7" stroke="currentColor"></circle>
                                            <path :style="hover ? 'fill:#ffffffb3' : 'fill:#fff'" fill="currentColor" d="m6.871 3.992c-.814 0-1.452.231-1.914.704-.462.462-.693 1.089-.693 1.892h1.155c0-.484.099-.858.297-1.122.22-.319.583-.473 1.078-.473.396 0 .715.11.935.33.209.22.319.517.319.902 0 .286-.11.55-.308.803l-.187.209c-.682.605-1.1 1.056-1.243 1.364-.154.286-.22.638-.22 1.045v.187h1.177v-.187c0-.264.055-.506.176-.726.099-.198.253-.396.462-.572.517-.451.825-.737.924-.858.275-.352.418-.803.418-1.342 0-.66-.22-1.188-.66-1.573-.44-.396-1.012-.583-1.716-.583zm-.198 6.435c-.22 0-.418.066-.572.22-.154.143-.231.33-.231.561 0 .22.077.407.231.561s.352.231.572.231.418-.077.572-.22c.154-.154.242-.341.242-.572s-.077-.418-.231-.561c-.154-.154-.352-.22-.583-.22z">
                                            </path>
                                        </g>
                                    </svg>
                                    
                                    <span :style="hover ? 'color:#ffffffb3' : 'color:#fff'"  >Hỗ trợ</span>
                                </a>
                            </v-hover>
                        </v-list-item-title>
                    </v-list-item-content>
                    <v-list-item-content class="pa-0" >
                        <v-list-item-title class="header__navbar-item d-flex align-center pa-2">
                                <v-menu
                                    transition="scale-transition"
                                    open-on-hover
                                    origin="150px 0"
                                    offset-y
                                    bottom
                                    nudge-left="90"
                                >
                                    <template v-slot:activator="{ on, attrs }">
                                        <v-hover v-slot="{ hover }">
                                            <a 
                                                href="" 
                                                class="text-decoration-none d-flex align-center"
                                                style="font-size: 13px;"
                                                v-bind="attrs"
                                                v-on="on"
                                                
                                            >
                                                <svg class="pr-1" width="20" height="20" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                    <path :style="hover ? 'stroke:#ffffffb3' : 'stroke:#fff' " d="M8.00065 14.6667C11.6825 14.6667 14.6673 11.6819 14.6673 8.00004C14.6673 4.31814 11.6825 1.33337 8.00065 1.33337C4.31875 1.33337 1.33398 4.31814 1.33398 8.00004C1.33398 11.6819 4.31875 14.6667 8.00065 14.6667Z" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"></path>
                                                    <path :style="hover ? 'stroke:#ffffffb3' : 'stroke:#fff' " d="M5.33464 8.00004C5.33464 11.6819 6.52854 14.6667 8.0013 14.6667C9.47406 14.6667 10.668 11.6819 10.668 8.00004C10.668 4.31814 9.47406 1.33337 8.0013 1.33337C6.52854 1.33337 5.33464 4.31814 5.33464 8.00004Z" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"></path>
                                                    <path :style="hover ? 'stroke:#ffffffb3' : 'stroke:#fff' " d="M1.33398 8H14.6673" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"></path>
                                                </svg>
                                            
                                                <span :style="hover ? 'color:#ffffffb3' : 'color:#fff'">Tiếng Việt</span>

                                                <v-icon dense :color="hover ? '#ffffffb3' : '#fff'">mdi mdi-chevron-down</v-icon>
                                            </a>
                                        </v-hover>
                                    </template>

                                    <v-list class="pa-0" width="200px">
                                        <v-list-item class="pa-0">
                                            <v-list-item-content>
                                                <a href="" class="subtitle-2 text-decoration-none black--text" style="padding: 10px;">Tiếng Việt</a>
                                                <a href="" class="subtitle-2 text-decoration-none black--text" style="padding: 10px;">English</a>
                                            </v-list-item-content>
                                        </v-list-item>
                                    </v-list>

                                </v-menu>
                            
                        </v-list-item-title>
                    </v-list-item-content>
                    <v-list-item-content class="pa-0">
                        <v-list-item-title class="header__navbar-item d-flex align-center">
                            <v-hover v-slot="{ hover }">
                                <RouterLink 
                                    to="./signup"
                                    href="" 
                                    style="font-size: 13px;" 
                                    class="text-decoration-none pa-2 header__navbar-item--separator"
                                    :style="hover ? 'color:#ffffffb3' : 'color:#fff'"
                                >
                                    Đăng Ký
                                </RouterLink>
                            </v-hover>
                        </v-list-item-title>
                    </v-list-item-content>
                    <v-list-item-content class="pa-0" >
                        <v-list-item-title class="header__navbar-item d-flex align-center">
                            <v-hover v-slot="{ hover }">
                                <RouterLink 
                                    to="/login"
                                    href="" 
                                    style="font-size: 13px;" 
                                    class="text-decoration-none pa-2"
                                    :style="hover ? 'color:#ffffffb3' : 'color:#fff'"
                                >
                                    Đăng Nhập
                                </RouterLink>
                            </v-hover>
                        </v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'headerNavbar',
}
</script>

<style scoped>
.v-list-item__title, .v-list-item__subtitle {
    overflow: visible !important;
}

.v-list-item__content {
    flex: none;
    align-self: normal;
    padding: 6px 0;
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

.v-menu__content {
    overflow: hidden;
}
</style>