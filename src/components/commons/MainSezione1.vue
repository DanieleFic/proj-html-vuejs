<template>
    <div class="ms_sezione1 container">
        <button onclick="topFunction()" id="myBtn" title="Go to top">Top</button>
        <div class="row">
            <div class="col-12">
                <h1>The Trusted Name <br>
                    for In-Home Tutoring.
                </h1>
                <p>
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Distinctio error natus quas amet recusandae, 
                    eum dicta hic obcaecati magnam nemo, quis veniam tempore, facilis pariatur quia rem voluptatibus blanditiis a beatae? 
                    Porro tenetur id quisquam, atque in amet et magnam.</p>
                <span>
                    LEARN MORE
                </span>
            </div>
            <div class="ms_borderbottom col-12">
                <img src="../../assets/img/h5-img-1.jpg" alt="">
            </div>
            <div class="ms_sotto container">
                <div class="row">
                    <div class="col-6">
                        <img class="ms_imgworld" src="../../assets/img/hand-world.png" alt="">
                    </div>
                    <div class="col-6">
                        <h1>Empowering Children to Reach Their Potenital.</h1>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio, repudiandae veniam asperiores ipsum sequi minus amet.
                            Blanditiis a ipsam, aut facilis veritatis, quidem aliquid, voluptatem quasi culpa eligendi ipsa corporis!</p>
                        <div class="ms_number container">
                            <div class="row">
                                <div class="col-6">
                                <h1>
                                    168
                                </h1>
                                <span>
                                    User Stories
                                </span>
                                
                                </div>
                                <div class="col-6">
                                <h1>
                                    347
                                </h1>
                                <span>
                                    Events
                                </span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
        </div>
    </div>
</template>

<script>
export default {
    name:"MainSezione1"
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";
    .container{
        
        h1{
            font-weight: 900;
        }
        p{
            color: gray
        };
        span{
            font-weight: 900;
            color: $text-azurine;
        }

        .ms_borderbottom{
            border-bottom: 1px solid gray;
        }
    }

    .ms_sotto{
        margin-top: 150px;
        .ms_imgworld{
        width: 400px;
        }
        h1{
            font-size: 70px;
        }
    }

    .ms_number{
        h1{
            color:$text-azurine
        }
    }
    
</style>