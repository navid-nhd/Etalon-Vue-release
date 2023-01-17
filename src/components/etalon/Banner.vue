<template>
    <section class="banner">
            <div class="container mx-auto">
                <div class="flex">
                    <div class="w-full lg:w-1/2 relative z-40 text-white">
                        <div class="year-number pt-5 text-white italic font-normal text-3xl opacity-30">
                            2022
                        </div>
                        <div class="banner-title text-white font-black text-6xl capitalize py-2 lg:py-6 lg:tracking-widest">
                            Autumn <br> Jackets
                        </div>
                        <div class="banner-description text-white text-base lg:text-2xl opacity-80">
                            Autumn Sale / Up to 50% OFF
                        </div>
                        <div class="pt-4 lg:pt-12 text-zinc-900">
                            <router-link to="/" class="btn bg-amber-300  hover:bg-amber-100 inline-block" title="Open Collection" target="_blank">Open Collection</router-link>
                        </div>
                    </div>
                    <div class="w-full lg:w-1/2">
                        <div class="banner-image-holder absolute bottom-0 left-1/2">
                            <img class="banner-image block relative z-10 pointer-events-none" src="src/image/banner-picture.png" alt="jacket">
                            <div class="off-amount hidden lg:block bg-amber-300 rounded-full text-center absolute left-0">
                                <div class="off-text font-bold py-6 px-4"> 40%<br> OFF</div>
                            </div>
                            <div class="arrow-holder hidden lg:flex flex-row  flex-nowrap absolute gap-2">
                                <div class="right-arrow">
                                        <router-link to="/" title="next">
                                            <img src="src/image/arrow-small-left.svg" alt="arrow" class="d-block">
                                        </router-link>
                                </div>
                                <div class="left-arrow">
                                    <router-link to="/" title="next">
                                        <img src="src/image/arrow-small-left.svg" alt="arrow" class="d-block">
                                    </router-link>
                                </div>
                            </div>
                            <div class="price-holder hidden lg:block text-white text-center absolute">
                                <div class="text-4xl font-medium">$299</div>
                            </div>
                              <div class="gallery-pointer-holder flex absolute m-2">
                                <div v-for="item in 3" class="gallery-pointer rounded-full">
                                    <router-link to="/"></router-link>
                                </div>
                            </div> 
                        </div>
                    </div>
                </div>
            </div>
        </section>
</template>
<script>
    export default{
        components: {

        },
        data(){

        },
        methods:{

        }
    }
</script>
<style scoped>
.banner-title {
    line-height: 50px;
}
.banner-image-holder {
    transform: translateX(-50%);
}
.banner-image {
    width: 208px;
    height: 391px;
}
.off-amount {
    width: 110px;
    height: 110px;
    top: 115px;
    z-index: 11;
}
.off-text {
    font-size: 26px;
    line-height: 30px;
}
.price-holder {
    right: 320px;
    top: 80px;
}

.arrow-holder{
    bottom: 5%;
    left: 2%;
}
.left-arrow,
.right-arrow {
    border-radius: 50%;
    border: 2px solid white;
    width: 35px;
    height: 35px;
    opacity: 0.5;
}
.left-arrow:hover,
.right-arrow:hover{
    opacity: 1;
}
.right-arrow {
    transform: scaleX(-1);
}
.gallery-pointer-holder {
    bottom: 10px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 12;
}
.gallery-pointer {
    width: 18px;
    height: 18px;
    background-color: rgba(255,255,255,0.2);
}
.gallery-pointer:hover {
    opacity: 1;
}
@media  screen and (min-width : 992px) {
    .year-number {
        padding-top: 85px;
        font-size: 60px;
        line-height: 1.2;
    } 
    .banner-title {
        font-size: 112px;
        line-height: 100px;
    }
    .banner-image-holder {
        left: 70%;
    }
    .banner-image {
        width: 342px;
        height: 619px;
    }
    .banner-image-holder::after {
        width: 308px;
        height: 308px;
        bottom: 184px;
        left: 76px;
    }
    .banner-image-holder::before {
        width: 318px;
        height: 318px;
        bottom: 77px;
        right: 70px;
    } 
    
    .gallery-pointer-holder {
        flex-direction: column;
        position: absolute;
        left: 450px;
        bottom: 30%;
        transform: translateY(-50%);
        z-index: 12;
    }
    .gallery-pointer {
        width: 18px;
        height: 18px;
        background-color: var(--etalon-white);
        opacity: 0.2;
        border-radius: 50%;
        margin: 8px;
    }
}
</style>