<script setup>
import {ref} from 'vue'
import NavMenu from './navMenu.vue'
import Header from './headerNav.vue'
import Searchlist from './searchlist.vue'
import Topfilter from './topfilter.vue'
import Recommend from './recommend.vue'

</script>

<template>
    <div class="common-layout">
        <el-container>
            <NavMenu/> 
            <el-container>
                <Header />
                <el-main>
                    <Searchlist />
                    <Topfilter/>
                    <Recommend/>
                </el-main>
            </el-container>
        </el-container>
    </div>
    
</template>

<style scoped>

</style>
