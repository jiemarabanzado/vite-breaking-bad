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

</template>

<style>
</style>