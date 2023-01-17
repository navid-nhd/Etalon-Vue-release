<template>
    <section class="bg-zinc-900 w-full" id="brands">
      <div class="container mx-auto">
          <div class="brands-holder">
              <ul class="list-none flex justify-between items-center">
                  <li v-for="item in brandsData">
                    <a :href="item.address"                      :title="item.title" 
                    class="block py-3 md:py-7 lg:py-9"
                    target="_blank">
                        <img :src="`src/image/${item.url}`" :alt="item.alt" class="block h-2.5 md:h-7 lg:h-9">
                    </a>
                  </li>
              </ul>
          </div>
      </div>
  </section>
</template>
<script>
    export default{
        components: {

        },
        data(){
            return{
                brandsData : [
                    {
                        url: 'Adidas-group-logo-fr.svg',
                        title: 'Adidas',
                        address: 'https://www.adidas.nl/',
                    },
                    {
                        url: 'Prada-Logo.svg',
                        title: 'PRADA',
                        address: 'https://www.prada.com/',
                    },
                    {
                        url: 'Logo_NIKE.svg',
                        title: 'NIKE',
                        address: 'https://www.nike.com/',
                    },
                    {
                        url: 'H&M-Logo.svg',
                        title: 'H&M',
                        address: 'https://www2.hm.com/',
                    },
                    {
                        url: 'Gucci_Logo.svg',
                        title: 'Gucci',
                        address: 'https://www.gucci.com/',
                    },
                    {
                        url: 'Blk_sports_logo.svg',
                        title: 'Blk',
                        address: 'https://blksport.com/',
                    },
                ]
            }
        },
        methods: {

        }
    }
</script>
<style scoped>

</style>