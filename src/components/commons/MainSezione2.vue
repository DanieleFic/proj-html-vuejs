<template>
<div>
    <div class="container-fluid">
        <div class="row">
            <div v-for="(element, index) in testo"
                :key="index"
                v-show="index == currentText"
                class="ms_profile col-6">
                <div class="ms_person">
                    <img :src="element.src" alt="">
                </div>
                <p>
                    {{element.text}}
                </p>
                <h3>
                    {{element.name}}
                </h3>
                <h4>
                    {{element.role}}
                </h4>
            </div>
        </div>
        <div class="ms_button">
            <span  class="dots">
                <span 
                v-for="(element, index) in testo" 
                :key="index" 
                :class="{ attivo: index == currentText }" class="dot"   
                @click="currentText = index"></span>
                </span>
        </div>
    </div>
    <Tabella/>
</div>
    
    
</template>

<script>
import Tabella from "./TabellaClassica.vue";
export default {
    name:"MainSezione2",
    components: {
    Tabella
    },
    data() {
        return {
            currentText: 0,
        testo: [
            {   
                src:require("../../assets/img/instructor-img-6.jpg"),
                text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam vel nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,",
                name: "Joan Collins",
                role: "Student"
            },
            {   
                src:require("../../assets/img/instructor-img-2.jpg"),
                text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam vel nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,",
                name: "Stefania Rossi",
                role: "Ceo"
            },
            {   
                src:require("../../assets/img/instructor-img-1.jpg"),
                text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam vel nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,",
                name: "Marco Esposito",
                role: "Dev"
            }
            ],
        }   
    },
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";
    .container-fluid{
        margin-top: 50px;
        height: 600px;
        background-image: url("../../assets/img/h5-parallax-img-1.png");
        text-align: center;
        color: white;
        .ms_profile{
            margin-top: 200px;
            animation: fade 2s forwards;
            @keyframes fade {
            from {
            opacity: 0;
            bottom: 300px;
            transform: translateY(-200px);
                }
            to {
                opacity: 1;
                }
            }
        }
        .row{
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .ms_person{
            height: 100px;
            margin-bottom: 30px;
            
            
            img{
                height: 100%;
                border-radius: 50%;
            }
        }
    }
    .dot {
        cursor: pointer;
        height: 12px;
        width: 12px;
        margin: 0 2px;
        background-color: $color-pallini;
        border-radius: 50%;
        display: inline-block;
        transition: background-color 0.6s ease;
        }

    .attivo{
            background-color: white;
        }

</style>