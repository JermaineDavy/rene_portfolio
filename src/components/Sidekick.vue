<template>
    <section class="sidekick">
        <div class="points-block">
            <div class="points-container">
                <div class="point">
                    Point 1
                </div>

                <div class="point">
                    Point 2
                </div>

                <div class="point">
                    Point 3
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">

.sidekick{
    height:561px;
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
            height: 220px;
            width: 1000px;
            background-color:red;
            display: flex;
            align-items: center;
            justify-content: center;
            justify-content: space-around;

            .point{
                height: 100%;
                width: 260px;
                background-color: green;
            }
        }
    } 
}

</style>