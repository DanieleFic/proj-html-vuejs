<template>
<div>
    <div class="ms_container">
        <div class="container">
            <div class="row">
                <div class="ms_text col-12">
                    <h1>Popular Online Courses</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis aliquam praesentium harum et. Laborum, veniam?</p>
                </div>
                <div class="row justify-content-around">
                    <div
                    v-for="(element, index) in schede"
                    :key="index"
                    :class="iscorrente(index)"
                    class="ms_box col-3">
                    <div class="box_img">
                        <img class="ms_img" :src="element.src" alt="">
                    </div>
                        <div class="ms_textbutton">
                            <div class="d-flex justify-content-between align-items-center ms_scheda">
                                <h6>{{element.titolo}}</h6>
                                <span class="rounded-circle">{{element.price}}</span>
                            </div>
                            <span class="ms_lorem">{{element.name}}</span>
                            
                        </div>
                        <div class="ms_lorem">
                            <p>{{element.text}}</p>
                        </div>
                        <div class="ms_text2">
                            <span><i class="fa fa-user"></i>{{element.utenti}}</span>
                            <span><i class="fa fa-tag"></i>{{element.tag}}</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="ms_button">
                <span class="dots"><span class="dot" @click="corrente = 1"></span></span>
                <span class="dots"><span class="dot" @click="corrente = 3"></span></span>
                <span class="dots"><span class="dot" @click="corrente = 6"></span></span>
                <span class="dots"><span class="dot" @click="corrente = 9"></span></span>
                <span class="dots"><span class="dot" @click="corrente = 10"></span></span>
            </div>
        </div>
    </div>
    <div class="container">
        <TabellaPrezzi/>
    </div>
</div>
</template>

<script>
import dataSchedebox from "../../data/dataSchedebox";
import TabellaPrezzi from "../commons/TabellaPrezzi.vue"
export default {
    name:"MainSezione3",
    components: {
        TabellaPrezzi
    },
    data(){
        return{
            corrente: 1,
            schede: dataSchedebox,
        }
    },

    methods: {
        iscorrente: function(indiceimmagine){
            if(indiceimmagine == this.corrente || indiceimmagine == this.corrente + 1 || indiceimmagine == this.corrente  - 1 ){
                return "active";
            }
                return "dnone";
        },
    }

}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";
    .ms_container{
        border-top: 1px solid $color-gray;
        border-bottom: 1px solid $color-gray;
        padding-bottom: 50px;
        background-image: url("../../assets/img/background-pattern.jpg");
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
            margin:50px 15px;
            animation: fade 2s forwards;
            @keyframes fade {
            from {
            opacity: 0;
            bottom: 300px;
            transform: translateX(200px);
                }
            to {
                opacity: 1;
        
                }
            }
        h6{
            font-weight: 900;
            font-size: 20px;
        }
        .ms_scheda{
            margin-top: 15px;
            padding: 0 10px;
            span{
                padding: 5px 10px;
                background-color:yellow;
                border-radius: 80%;
            }
        }
        img{
            width: 100%
        }
    }
    .ms_button{
        text-align: center;
        margin-top: 50px;
        .dot {
        cursor: pointer;
        background-color:$color-pallini;
        height: 12px;
        width: 12px;
        margin: 0 2px;
        border-radius: 50%;
        display: inline-block;
        transition: background-color 0.6s ease;
        }
    }
    

    .ms_text2{
        span{
            margin: 0px 10px;
            font-size: 15px;
            color:$color-gray ;
        }
    }

    .attivo{
        background-color: black;
    }

    .ms_lorem{
        padding: 10px;
    }

    .active{
        display: block;
    }

    .dnone{
        display:none;
    }

</style>