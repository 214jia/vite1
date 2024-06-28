<script setup>
import {ref} from 'vue'
import Banner from './banner.vue'
import Recommendlist from './recommendlist.vue'
</script>

<template>
<div class="recommend">
    <div class="recommend-left">
        <h2>推荐酒店</h2>
        <Recommendlist/>
    </div>
    <div class="recommend-right">
        <Banner/>
    </div>
</div>
</template>

<style scoped>

</style>
