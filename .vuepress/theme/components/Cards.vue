<template>
<div class="flex flex-wrap lg:pt-5 lg:m-2 justify-center"> 
    <div v-for="item in $page.frontmatter.cards" class="lg:w-1/4 md:w-1/2 m-2 cursor-pointer bg-white rounded shadow-lg text-center" @click="goToRoute(item.link)">
        <img class="pt-5" :src="'./images/'+item.image+''" :alt="item.title">
        <div class="px-4 py-2">  
            <div class="text-blue-darkest font-bold text-xl mb-2">{{item.title}}</div>
                <p class="text-blue-darker">
                    {{item.blurb}}
                </p>
            </div>  
    </div>   
</div>
</template>
<script>
export default {
    name: 'Cards',
    methods: {
        goToRoute(link) {
            window.open(link,'_blank');
        }
    }
}
</script>
