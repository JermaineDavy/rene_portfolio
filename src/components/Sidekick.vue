<template>
    <section class="sidekick">
        <div class="points-block">
            <div class="points-container">
                <div class="point">
                    <div class="point-icon">
                        <i class="fas fa-dumbbell"></i>
                        <span>Hard Working</span>
                    </div>

                    <hr>

                    <div class="point-describe">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                    </div>
                </div>

                <div class="point">
                    <div class="point-icon">
                        <i class="fas fa-comments-dollar"></i>
                        <span>Excel at Sales</span>
                    </div>

                    <hr>

                    <div class="point-describe">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                    </div>
                </div>

                <div class="point">
                    <div class="point-icon">
                        <i class="fas fa-people-carry"></i>
                        <span>Awesome Support</span>
                    </div>

                    <hr>

                    <div class="point-describe">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">

.sidekick{
    height:511px;
    background-color: rgb(235, 235, 235);
    position: relative;
    top: -90px;

    .points-block{
        width: 100%;
        display: flex;
        justify-content: center;

        .points-container{
            position: absolute;
            bottom: 20px;
            height: 250px;
            width: 1000px;
            display: flex;
            align-items: center;
            justify-content: center;
            justify-content: space-around;

            .point{
                height: 100%;
                width: 260px;
                display: flex;
                flex-direction: column;
                align-items: center;

                .point-icon{
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    height: 30%;
                    padding-top: 5%;

                    i{
                        font-size: 2.3em;
                        color: rgba(221, 160, 221, 1);
                    }

                    span{
                        font-size: 1.3em;
                        margin-top: 0.5em;
                    }
                }

                .point-describe{
                    text-align: center;
                }

                hr{
                    width: 50px;
                    border:2px solid silver;
                    border-radius: 20px;
                    color: silver;
                    margin: 10% 0;
                }
            }

            .point:hover{
                .point-icon{
                    span{
                    color: rgba(221, 160, 221, 1);
                    }
                }
            }
        }
    } 
}

</style>