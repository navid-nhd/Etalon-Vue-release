<template>
    <div>
        <div class="sellers-image-holder w-full flex justify-center items-center relative rounded-3xl bg-white g-0">
            <img :src="`src/image/${title.url}`" alt="Backpack" class="seller-image w-full">
            <button title="Add to Favorite" @click="changeStatus()" class="favorite-icon-link block absolute">
                    <img :src="`src/image/${src}`" alt="favorite"  class="fav-icon-white">
            </button>
        </div>
        
        <div class="sellers-details w-full flex justify-between items-center pt-4">
            <div class="sellers-name-price">
                <div class="sellers-name font-medium capitalize">
                    {{ title.name }}
                </div>
                <div class="sellers-price font-light capitalize opacity-60">
                    {{ title.price }}
                </div>
            </div>
            <button @click="counterStore.increment()"  class="sellers-buying-link flex justify-center items-center rounded-md 2xl:mr-9">
                <router-link to="/" title="Go to Shop">
                    <img src="src/image/shopping-cart.svg">
                </router-link>
            </button>
        </div>
    </div>
</template>
<script >

import { mapStores,mapActions } from 'pinia';
import { useCounterStore } from '@/stores/counter';

    export default{
        props: {
            title : {
                type: Object,
            }
        },
        methods: {
            ...mapActions(useCounterStore,['increment']),
            changeStatus() {
                this.src = this.src === 'heart-logo.svg' ? 'filled-heart.svg' : 'heart-logo.svg' ;
            },
        },
        computed: {
            ...mapStores(useCounterStore)
        },
        data() {
            return{
                src: 'heart-logo.svg',
                // bestSellersInfo : [
                //     {
                //         url : 'bag.jpg',
                //         name: 'Fjallraven Backpack',
                //         price: '$109.95'
                //     },
                //     {
                //         url : 'jacket.jpg',
                //         name: 'Mens Cotton Jacket',
                //         price: '$55.99'
                //     },
                //     {
                //         url : 't-shirt.jpg',
                //         name: 'Slim Fit T-Shirts',
                //         price: '$22.3'
                //     },
                //     {
                //         url : 'slim-shirt.jpg',
                //         name: 'Mens Casual Slim Fit',
                //         price: '$11.25'
                //     },
                // ]
            }
        }
    }
</script>
<style scoped>
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
</style>