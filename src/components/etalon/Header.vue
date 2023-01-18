<template>
    
    <header class="top-0">
        <div class="container mx-auto">
            <div class="foo">
                <div class="font-black text-4xl">
                    <router-link :to="{
                            name : 'home',
                            query : {},
                        }" 
                        class="block py-3 px-6" 
                        title="Etalon homepage" 
                        target="_self">
                        Etalon
                    </router-link>
                </div>
                <div class="nav-shopping-cart flex justify-center items-center w-10 h-10 rounded-full bg-amber-300 hover:bg-amber-100">
                    <router-link to="#" class="nav-shopping-cart-icon realtive" title="Go to Shopping Cart" target="_blank">
                        <img class="top-header-image" src="@/image/shopping-cart-logo.svg" alt="cart">
                        <span class="shopping-cart-indicator absolute text-white bg-red-700 rounded-full font-black text-sm flex justify-center items-center">
                            {{ counterStore.count }}
                        </span>
                    </router-link>
                </div>
            </div>
        </div>
        <div class="flex md:hidden w-full h-12 fixed left-0 bottom-0 z-50 bg-amber-200">
            <div class="container mx-auto">
                <nav class="bottom-header-holder">
                    <ul class="mobile-nav-list">
                        <li v-for="item in menuLinkAddress"
                        class="list-none flex justify-between">
                            <router-link class="block py-3 px-4" to="#" :title="item.title" target="_blank">
                                <img :src="`src/image/${item.url}`" :alt="item.alt" class="nav-logo">
                            </router-link>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>
<script>

import { mapStores } from 'pinia'
import { useCounterStore } from '@/stores/counter.js';
    export default{
        computed:{
            ...mapStores(useCounterStore)
        },
        components:{

        },
        data(){
            return{
                menuLinkAddress : [{
                        url: 'phone-logo.svg',
                        alt: 'phone',
                        title: 'Contact Us',
                    },
                    {
                        url: 'first-badge-logo.svg',
                        alt: 'badge',
                        title: 'Our Honors',
                    },
                    {
                        url: 'home-logo.svg',
                        alt: 'home',
                        title: 'Etalon Home',
                    },
                    {
                        url: 'shop-logo.svg',
                        alt: 'shop',
                        title: 'Store',
                    },
                    {
                        url: 'shopping-cart-logo.svg',
                        alt: 'Cart',
                        title: 'Shopping Cart',
                    }
                ]
            }
        },
        methods:{

        }
    }
</script>
<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;
.foo {
    @apply hidden md:flex justify-between pt-6 items-center relative text-white z-50;
}
.shopping-cart-indicator{
    top: 25px;
    right:-15px;
    width: 25px;
    height: 25px;
}
.mobile-nav-list {
    list-style: none;
    display: flex;
    justify-content: space-between;
  }



</style>