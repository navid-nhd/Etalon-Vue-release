<template>
    <section class="best-sellers w-full" id="best-sellers">
            <div class="container mx-auto">
                <div class="title-holder relative flex justify-between px-4">
                    <h2 class="section-title">Best Sellers</h2>
                    <div class="nav-shopping-cart flex justify-center items-center w-10 h-10 rounded-full bg-amber-300 hover:bg-amber-100">
                        <router-link to="#" class="nav-shopping-cart-icon realtive" title="Go to Shopping Cart" target="_blank">
                            <img class="top-header-image" src="@/image/shopping-cart-logo.svg" alt="cart">
                            <span class="shopping-cart-indicator absolute text-white bg-red-700 rounded-full font-black text-sm flex justify-center items-center">
                                {{ counterStore.count }}
                            </span>
                        </router-link>
                    </div>
                </div>
                <div class="best-sellers-holder">
                    <ul class="sellers-list flex lg:flex-nowrap overflow-x-scroll pb-9">
                        <li v-for="item in bestSellersInfo" class="sellers-item flex-shrink-0 md:w-1/4 flex flex-wrap">
                            <div class="sellers-image-holder w-full flex justify-center items-center relative rounded-3xl bg-white g-0">
                                <img :src="`src/image/${item.url}`" alt="Backpack" class="seller-image w-full">
                                <button title="Add to Favorite" @click="changeStatus()" class="favorite-icon-link block absolute">
                                     <img :src="`src/image/${src}`" alt="favorite"  class="fav-icon-white">
                                </button>    
                            </div>
                            <div class="sellers-details w-full flex justify-between items-center pt-4">
                                <div class="sellers-name-price">
                                    <div class="sellers-name font-medium capitalize">
                                        {{ item.name }}
                                    </div>
                                    <div class="sellers-price font-light capitalize opacity-60">
                                        {{ item.price }}
                                    </div>
                                </div>
                                <button @click="counterStore.increment()"  class="sellers-buying-link flex justify-center items-center rounded-md 2xl:mr-9">
                                    <router-link to="/" title="Go to Shop">
                                        <img src="src/image/shopping-cart.svg">
                                    </router-link>
                                </button>
                            </div>
                        </li>
                    </ul>
                </div>
                <div class="sellers-btn hidden lg:block text-center">
                    <router-link  to="/" title="load more products" class="btn text-white inline-block bg-zinc-900 hover:text-white hover:bg-zinc-700">Load More Products</router-link>
                </div>
            </div>
        </section>
</template>
<script>
import { mapStores,mapActions } from 'pinia';
import { useCounterStore } from '@/stores/counter';
    export default{ 
        methods: {
            ...mapActions(useCounterStore,['increment']),
            changeStatus() {
                this.src = this.src === 'heart-logo.svg' ? 'filled-heart.svg' : 'heart-logo.svg' ;
            },
        },
        computed: {
            ...mapStores(useCounterStore)
        },
        components: {

        },
        data() {
            return{
                src: 'heart-logo.svg',
                bestSellersInfo : [
                    {
                        url : 'bag.jpg',
                        name: 'Fjallraven Backpack',
                        price: '$109.95'
                    },
                    {
                        url : 'jacket.jpg',
                        name: 'Mens Cotton Jacket',
                        price: '$55.99'
                    },
                    {
                        url : 't-shirt.jpg',
                        name: 'Slim Fit T-Shirts',
                        price: '$22.3'
                    },
                    {
                        url : 'slim-shirt.jpg',
                        name: 'Mens Casual Slim Fit',
                        price: '$11.25'
                    },
                ]
            }
        }
    }
</script>
<style scoped>
   
/* ------- BEST SELLERS ------*/
.best-sellers {
        background-color: #e9e9e9;
    }
.section-title {
    font-size: 32px;
    line-height: 32px;
    padding: 32px 0;
}
.sellers-item {
    width: 250px;
    padding: 17.5px;
}
.sellers-image-holder {
    width: 227px;
    height: 220px;
}
.seller-image {
    width: 132px;
    height: 148px;
}
.favorite-icon-link {
    width: 24px;
    height: 21px;
    top: 18px;
    right: 16px;
}
.fav-icon-white {
    display: block;
}
.fav-icon-black {
    display: none;
}
.sellers-image-holder a:hover img.fav-icon-white{
    display: none;
}
.sellers-image-holder a:hover img.fav-icon-black{
    display: block;
}
.sellers-name {
    font-family: var(--etalon-font-secondry);
    font-size: 16px;
    line-height: 19px;
}
.sellers-price {
    font-family: var(--etalon-font-secondry);
    font-size: 14px;
    line-height: 16px;
}
.sellers-buying-link {
    background-color: var(--etalon-yellow);
    width: 30px;
    height: 30px;
}
.sellers-buying-link > a{ 
    display: block;
    padding: 7px;
}
.sellers-buying-link > a:hover{ 
    background-color: var(--etalon-yellow-hover);
}
.sellers-btn {
    padding: 35px 0 70px;
}
@media  screen and (min-width : 992px) {
    .sellers-item {
        width: 25%;
    }
    .section-title {
        font-size: 48px;
        line-height: 48px;
        padding: 70px 0;
    }
    .sellers-list {
        flex-wrap: wrap;
        overflow: clip;
        justify-content: space-between;
    }
    .sellers-image-holder {
        width: 250px;
        height: 260px;
        flex-shrink: 1;
    }
    .sellers-name {
        font-size: 18px;
        line-height: 21px;
    }
    .sellers-price {
        font-size: 16px;
        line-height: 19px;
    }
    .sellers-buying-link {
        width: 40px;
        height: 40px;
    }
    .sellers-buying-link > a{ 
        padding: 11px;
    }
    .nav-shopping-cart {
    margin-top: 70px;
    }
}
@media  screen and (min-width : 1200px) { 
    .sellers-image-holder {
        width: 303px;
        height: 347px;
    }
    .seller-image {
        width: 214px;
        height: 238px;
    }
   
}
.shopping-cart-indicator{
    top: 25px;
    right:0px;
    width: 25px;
    height: 25px;
}
.nav-shopping-cart {
    margin-top: 35px;
}
</style>