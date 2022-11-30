<script>
import axios from 'axios';
export default{
    data(){
        return{
            Characters:[],
        }
    },
    created(){
        axios.get('https://www.breakingbadapi.com/api/characters').then((resp)=>{
            this.Characters=resp.data;
            console.log(this.Characters);
        });
    }
}
</script>
<template>
    <div class="card-grid">
        <div class="ms-card" v-for="character in Characters">
            <div class="card-img">
                <img :src="character.img" alt="">
            </div>
            <div class="card-name">
                {{character.name}}
            </div>
            <div class="category">
                {{character.category}}
            </div>
            <div class="status">
                {{character.status}}
            </div>
        </div>
       
    </div>
</template>

<style lang="scss" scoped>
    .card-grid{
        width: 1200px;
        margin: auto;
        background-color: white;
        padding: 20px;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        
    }
    .ms-card{
        width: calc(100%/5 - 20px);
        padding: 20px;
        background-color: #2e3a46;
        margin-bottom: 20px;
    }
    .card-name{
        color: white;
        text-align: center;
        text-transform: uppercase;
    }
    .category , .status{
        text-align: center;
        color: gray;
    }
    img{
        width: 100%;
    }
</style>