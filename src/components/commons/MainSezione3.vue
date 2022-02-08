<template>
    <div class="container">
        <div class="row">
            <div class="ms_text col-12">
                <h1>Popular Online Courses</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis aliquam praesentium harum et. Laborum, veniam?</p>
            </div>
            <div class="ms_displayflex row">
                <div
                v-for="(element, index) in schede"
                :key="index"
                class="ms_box col-3">
                <div class="box_img">
                    <img class="ms_img" :src="element.src" alt="">
                </div>
                    <div class="ms_textbutton">
                        <div class="ms_flex">
                            <h6>{{element.titolo}}</h6>
                            <span class="rounded-circle">{{element.price}}</span>
                        </div>
                        <span class="ms_lorem">{{element.name}}</span>
                        
                    </div>
                    <div class="ms_lorem">
                        <p>{{element.text}}</p>
                    </div>
                    <div class="ms_text2">
                        <span><i class="fa-thin fa-user"></i>{{element.utenti}}</span>
                        <span><i class="fa-thin fa-4"></i>{{element.tag}}</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    
</template>

<script>
import dataSchedebox from "../../data/dataSchedebox";
export default {
    name:"MainSezione3",
    components: {
    },
    data(){
        return{
            currentText: 0,
            schede: dataSchedebox,
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

    .ms_displayflex{
        display: flex;
        justify-content: space-evenly;
    }
    .ms_text{
        text-align: center;
        margin-top: 100px;
        h1{
            color: black;
        }
        p{
            color: $color-gray;
        }
    }
    .ms_box{
            height: 400px;
            padding: 0;
            border: 1px solid black;
            margin:5px 15px;
        h6{
            font-weight: 900;
            font-size: 20px;
        }
        .ms_flex{
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            margin-top: 15px;
            padding: 0 10px;
            span{
                padding: 5px 10px;
                background-color:green;
                border-radius: 80%;
            }
            
        }
        img{
            width: 100%
        }
    }

    .ms_text2{
        span{
            margin: 0px 10px;
            font-size: 15px;
            color:$color-gray ;
        }
    }

    .ms_lorem{
        padding: 10px;
        }
</style>