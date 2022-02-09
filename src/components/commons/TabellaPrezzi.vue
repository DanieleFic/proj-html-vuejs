<template>
    <div class="container-fluid">
        <div class="container">
            <div class="row">
                <div class="ms_textcenter col-12">
                    <h1>Pricing Plans</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa, fugit!</p>
                </div>
            </div>
        </div>
        <table class="table table-bordered">
            <thead>
                <tr>
                    <th class="ms_tablewidth1" scope="col-1">Save up to 40%  by paying  weekly</th>
                    <th class="ms_tablewidth" scope="col">
                        <img src="../../assets/img/icon-tabella-2.png" alt="">
                        <p>Standard</p>
                        <p>$12</p>
                    </th>
                    <th class="ms_tablewidth" scope="col">
                        <img src="../../assets/img/icon-tabella-3.png" alt="">
                        <p>Professional</p>
                        <p>$59</p>
                    </th>
                    <th class="ms_tablewidth" scope="col">
                        <img src="../../assets/img/icon-tabella-1.png" alt="">
                        <p>Advanced</p>
                        <p>$88</p>
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <th scope="row"> <h6>Number of Courses</h6> </th>
                    <td><h6>2</h6></td>
                    <td><h6>4</h6></td>
                    <td><h6>6</h6></td>
                </tr>
                <tr>
                    <th scope="row"><h6>Time</h6></th>
                    <td><h6>15 Days</h6></td>
                    <td><h6>30 Days</h6></td>
                    <td><h6>30 Days</h6></td>
                </tr>
                <tr>
                    <th scope="row"><h6>Web Design</h6></th>
                    <td><i class="fas fa-check"></i></td>
                    <td><i class="fas fa-check"></i></td>
                    <td><i class="fas fa-check"></i></td>
                </tr>
                <tr>
                    <th scope="row"> <h6>Human-Centered Design</h6> </th>
                    <td><i class="fas fa-check"></i></td>
                    <td><i class="fas fa-check"></i></td>
                    <td><i class="fas fa-check"></i></td>
                </tr>
                <tr>
                    <th scope="row"> <h6>Basic Marketing</h6> </th>
                    <td><i class="fas fa-times"></i></td>
                    <td><i class="fas fa-check"></i></td>
                    <td><i class="fas fa-check"></i></td>
                </tr>
                <tr>
                    <th scope="row"> <h6>Python for Everybody</h6> </th>
                    <td><i class="fas fa-times"></i></td>
                    <td><i class="fas fa-check"></i></td>
                    <td><i class="fas fa-check"></i></td>
                </tr>
                <tr>
                    <th scope="row"> <h6>Android Developer</h6> </th>
                    <td><i class="fas fa-times"></i></td>
                    <td><i class="fas fa-times"></i></td>
                    <td><i class="fas fa-check"></i></td>
                </tr>
                <tr>
                    <th scope="row"> <h6>Business English</h6> </th>
                    <td><i class="fas fa-times"></i></td>
                    <td><i class="fas fa-times"></i></td>
                    <td><i class="fas fa-check"></i></td>
                </tr>
                <tr>
                    <th class="noborder" scope="row"></th>
                    <td><button type="button" class="btnwhite btn-primary">GET IT NOW</button></td>
                    <td><button type="button" class="btnblue btn-primary">GET IT NOW</button></td>
                    <td><button type="button" class="btnwhite btn-primary">GET IT NOW</button></td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
import schededataTabella from "../../data/dataSchedeTabella";
export default {
    name:"TabellaPrezzi",
    data(){
        return{
            schede: schededataTabella,
        }
    },
    methods: {
        
    }
    
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

    .ms_container{
        margin-top: 50px;
    }
    .ms_textcenter{
        text-align: center;
        h1{
            font-weight: 900;
        }
        p{
            color: $color-gray;
        }
    }

    table{
        text-align: center;

        th{
            padding: 15px;
        }

        td{
            padding: 15px;
        }

        h6{
            color:$color-gray;
            font-weight: 900;
        }

        .ms_tablewidth{
            width: 15%;
            font-size: 25px;
            margin-top: 30px;
        }
        .ms_tablewidth1{
            width: 10%;
            font-size: 25px;
            margin-top: 30px;
        }
    }

    .fa-check{
        color:$text-azurine;
        margin-right: 20px;
        }
    .fa-times{
        color:$color-gray;
        margin-right: 20px;
        }
    
    .btnblue{
        padding: 10px 35px;
        background-color:$main-color ;
        border: none;
        border-radius: none;
        font-weight: 900;
        }

    .btnwhite{
        padding: 10px 35px;
        background-color:white ;
        border: 1px solid $color-gray;
        border-radius: 1px solid $color-gray;
        font-weight: 900;
        color:$color-gray;

        &:hover{
            background-color:$main-color;
            border: 1px solid $main-color;
        }
        }
    
</style>