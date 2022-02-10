<template>
    <div class="container">
        <div class="row">
            <div v-for="(element, index) in schede"
            :key="index"
            class="ms_scheda col">
                <div class="box">
                    <img :src="element.src" alt="">
                    <p>{{element.titolo}}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import schededata from "../../data/dataSchede";
export default {
    name:"Schede",
    data(){
        return{
            schede: schededata
        }
    }
}
</script>

<style scoped lang="scss" >
@import "../../assets/style/vars.scss";

    .container{
        margin-top: 50px;
        box-sizing: border-box;
        height: 300px;
        .row{
            text-align: center;
        }
    }

    .ms_scheda{
        margin: 0px 10px;
        height: 200px;
        background-color: $background-schede;
        text-align: center;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        transition: all .3s ease-out;

        &:hover{
            color: white;
            background-color: $color-hover;
            transform: translate(0, -5px);
        }

        p{
            margin: 20px 0;
            font-weight: bold;
        }
    }
</style>