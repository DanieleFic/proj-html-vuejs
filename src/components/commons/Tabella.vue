<template>
    <div class="ms_container">
        <div class="container">
            <div class="row">
                <div
                v-for="(element, index) in schede"
                :key="index" class="ms_box col-2">
                    {{element.titolo}}
                </div>
                
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
            schede: schededataTabella
        }
    },
    
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";
    .ms_container{
        margin-top: 50px;
    }
    .row{
        display: flex;
        flex-direction: column;
        
        .ms_box{
            padding: 20px;
            border: 1px solid;
            font-weight: 900;
        }
    }
    
</style>