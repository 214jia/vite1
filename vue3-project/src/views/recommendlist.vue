<script setup>
import {ref} from 'vue'
let recommendlist = ref([
    {id:1,name:'北京首都宾馆',img_url:'1.jpg',transport:'天安门/王府井 | 距市中心直线310米',starimg_url:'star5.png',tag:['网球场','商务中心','会议厅']},
    {id:2,name:'北京京伦饭店',img_url:'2.jpg',transport:'国贸CBD | 距市中心直线4.1公里',starimg_url:'star4.png',tag:['停车场','健身室','SPA']},
    {id:3,name:'北京新世界中心同派酒店',img_url:'3.jpg',transport:'前门/天坛公园/崇文门 | 距市中心直线1公里',starimg_url:'star4.png',tag:['桌球室','闪住','酒吧','行李寄存']},
])

</script>

<template>
    <div class="recommend-list">
        <ul>
            <li v-for="v in recommendlist" :key="v.id">
                <div class="list-left">
                    <div class="list-left-img">
                        <img :src="`/src/assets/images/${v.img_url}`" alt="">
                    </div>
                <div class="list-left-title ">
                    <div class="list-left-tagandtitle">
                        <h4>{{v.name}}</h4>
                         <img :src="`/src/assets/images/${v.starimg_url}`" alt="">
                        <span class="badge-thumb"></span>
                    </div>
                    <div class="list-left-transport">
                        <p>{{v.transport}}</p>
                    </div>
                    <div class="list-left-tag">
                        <el-tag class="ml-2" type="danger" effect="plain" v-for="(k,i) in v.tag" :key="i">{{k}}</el-tag>
                    </div>
                </div>
                </div>
                 <div class="list-right">
                <div class="list-right-comment">
                    <div class="list-right-describe">
                        <p>好</p>
                        <a href="#">3333条点评</a>
                    </div>
                    <div class="list-right-score">
                        <p>4.5</p>
                    </div>
                </div>
                <div class="list-right-price">
                    <p>￥3333</p>
                     <el-button type="primary">查看详情</el-button>
                </div>
            </div>
            </li>
        </ul>

    </div>
   
</template>

<style scoped>

</style>
