<script setup>
import NewsItem from '@/components/News/NewsItem.vue'

const props = defineProps({
    items: Array,
    required: true,
    default: []
})
</script>

<template>
    <div class="container">
        <NewsItem 
           v-for="item in items"
           :item="item"
           :key="item.date"
        />
    </div>
</template>


<style lang="scss" scoped>
.container { 
    position: relative;   
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 64px 20px ;
    padding: 64px 100px 200px 100px;
}
</style>