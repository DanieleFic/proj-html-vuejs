<template>
    <div class="ms_container">
        <div class="container">
            <div class="row">
                <div
                v-for="(element, index) in schede"
                :key="index"
                :class="iscorrentebox(index)"
                @click="currentText = index"
                class="ms_box col-12">
                    <span>{{element.section}}</span>
                </div>
            </div>
                <div
                v-for="(element, index) in schede"
                :class="iscorrente(index)"
                :key="index" class="ms_text col-10">
                    <h1>{{element.titolo}}</h1>
                    <p>{{element.testo}}</p>
                    <ul>
                        <li
                        v-for="(element, index) in schede[index].lista"
                        :key="index">
                        <i class="fas fa-check"></i>{{element}}
                        </li>
                    </ul>
                </div>
                
        </div>
    </div>
</template>

<script>
import schededataTabella from "../../data/dataSchedeTabella";
export default {
    name:"Tabella",
    data(){
        return{
            currentText: 0,
            schede: schededataTabella,
        }
    },
    methods: {
        iscorrente: function(indiceimmagine){
            if(indiceimmagine == this.currentText){
                return "active";
            }
                return "dnone";
        },
        iscorrentebox: function(indiceimmagine){
            if(indiceimmagine == this.currentText){
                return "activeblue";
            }
                return "noactive";
        },
    }
    
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";
    .ms_container{
        margin-top: 50px;
        
        .container{
            display: flex;
            flex-direction: row;
        }
    }
    .row{
        display: flex;
        flex-direction: column;
        width: 20%;
        
        .ms_box{
            padding: 20px;
            border: 1px solid rgb(211, 204, 204);
            font-weight: 900;
            color: rgb(114, 109, 109) ;
        }
    }

    .ms_text{
        width: 50%;
        margin-left: 100px;
        margin-top:30px;
        font-weight: 900;
        h1{
            color: black;
        }
        p{
            color: $color-gray;
        }

        .fa-check{
                color:$text-azurine;
                margin-right: 20px;
            }

        ul{
            padding: 0;
            li{
                list-style: none;
                padding:10px;
                color:$color-gray ;
            }

            
        }
    }

    .active{
        display: block;
    }

    .dnone{
        display: none;
    }
    
    .activeblue{
        border-left: 5px solid $text-azurine!important ;
        background-color:rgb(211, 209, 209) ;
        
        span{
            color: $text-azurine;
        }
    }

</style>