<template>
    <div class="header">
        <div class="ms_jumbo container-fluid">
            <div class="container-fluid">
                <div class="row">
                    <div class="col-2">
                        <img class="ms_logo" src="../../assets/img/logo-light.png" alt="">
                    </div>
                    <div class="ms_nav col-8">
                        <div class="col" >
                        HOME
                        </div>
                        <div class="col">
                        COURSE
                        </div>
                        <div class="col">
                        INSTRUCTORS
                        </div>
                        <div class="col">
                        EVENTS
                        </div>
                        <div class="col">
                        PAGES
                        </div>
                        <div class="col">
                        ELEMENTS
                        </div>
                    </div>
                    <div class="col-2">
                        <div class="ms_icon">
                            <i class="fas fa-search"></i>
                            <i class="fas fa-shopping-basket"></i>
                            <i class="fas fa-bars"></i>
                        </div>
                    </div>
                    <div class="ms_textmain">
                        <h1>Contemporary Ideas</h1>
                        <p>
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
                            Totam vel nihil ipsam aperiam distinctio ex?Lorem ipsum dolor, 
                            sit amet consectetur adipisicing elit. Illum, neque.
                        </p>
                        <button type="button" class="btn btn-primary">REGISTER NOW</button>
                    </div>
                </div>
            </div>
        </div>
    <Schede/>
    </div>
    
</template>

<script>
import Schede from "../commons/SchedeHeader.vue"
export default {
    name: "Header",
    components: {
    Schede
    }
}
</script>

<style lang="scss">
@import "../../assets/style/vars.scss";

    .ms_jumbo{  
        height: 700px;
        position: relative;
        background-image: url("../../assets/img/jumbo.jpg");
        background-size: cover;
        background-repeat: no-repeat;
        text-align: center;

        .ms_textmain{
            margin: 0 auto;
            width: 50%;
            text-align: center;
            margin-top: 170px;
            margin-bottom: 50px;

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
    }

    .row{
        height: 50px;
        display: flex;
        flex-direction: row;

        .ms_nav{
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: white;
        }

        .ms_logo{
            display: flex;
            align-items: center;
            height: 30px;
            margin-top:10px
        }

        .ms_icon{
            padding-top: 15px;
            display: flex;
            flex-direction: row;
            justify-content: space-evenly;
            color: white;
            
        }
    }

</style>