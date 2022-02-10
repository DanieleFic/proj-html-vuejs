<template>
    <div>
        <div v-for="(element, index) in testo"
            :key="index"
            v-show="index == currentText"
            class="ms_textmain">
            <!-- <img :src="element.src" alt="">  -->
            <h1>{{element.title}}</h1>
            <p>
                {{element.text}}
            </p>
            
            <button type="button" class="btn btn-primary">REGISTER NOW</button>
        </div>
        <div class="ms_button">
            <span  class="dots">
                <span 
                v-for="(element, index) in testo" 
                :key="index" 
                :class="{ attivo: index == currentText }" class="dot"   
                @click="currentText = index">
                </span>
            </span>
        </div>
    </div> 
</template>

<script>

export default {
    name:"SlideTesto",
    data() {
        return {
            currentText: 0,
            isActive: false,
        testo: [
            {   
                src: require("../../assets/img/instructor-img-1.jpg"),
                title: "Contemporary Ideas",
                text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam vel nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,"
            },
            {   
                src: require("../../assets/img/instructor-img-2.jpg"),
                title: "Registrati subito",
                text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam vel nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,Lorem ipsum dolor,nihil ipsam aperiamLorem ipsum dolor,nihil "
            },
            {   
                src: require("../../assets/img/instructor-img-6.jpg"),
                title: "Subito Registrati",
                text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam vel nihil ipsam aperiam distinctio ex?Lorem ipsum dolor,Lorem ipsum dolor,nihil "
            },
            ],
        }   
    },
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
                font-weight: 900;
                color: white;
            }

            p{
                font-weight: 900;
                color: white;
                padding-top: 10px;
            }
        }
        .btn{
                padding: 20px 35px;
                background-color:$main-color ;
                border: none;
                border-radius: none;
                font-weight: 900;
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