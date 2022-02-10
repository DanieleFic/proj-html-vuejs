<template>
    <div>
        <NavHeader/>
        <Schede/>
    </div>
</template>

<script>
import Schede from "../commons/SchedeHeader.vue"
import NavHeader from "../commons/NavHeader.vue"
export default {
    name: "Header",
    components: {
    Schede,
    NavHeader,
    },
    methods: {
        /* iscorrentedot: function(indiceimmagine){
            if(indiceimmagine == this.currentText){
                return "white";
            } else{
                return "gray";
            }
                
        }, */
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";
        .ms_textmain{
            margin: 0 auto;
            width: 50%;
            text-align: center;
            margin-top: 170px;
            margin-bottom: 50px;
            animation: fade 2s forwards;

            @keyframes fade {
            from {
            opacity: 0;
            bottom: 300px;
            transform: translateX(-1000px);
                }
            to {
                opacity: 1;
                }
            }
            h1{
                font-size: 80px;
                
                color: white;
            }
            p{
                color: white;
                padding-top: 10px;
            }
        }
        .btn{
                padding: 20px 35px;
                background-color:$main-color ;
                border: none;
                border-radius: none;
            }
        .ms_button{
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
        }
        .dot {
            cursor: pointer;
            background-color: white;
            height: 12px;
            width: 12px;
            margin: 0 2px;
            border-radius: 50%;
            display: inline-block;
        }
        .attivo{
            background-color: $main-color;
        }
</style>