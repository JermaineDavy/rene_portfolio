<template>
    <section class="hero">
        <img src="/images/undraw_quality_time_wiyl.svg" alt="">

        <div class="hero-message">
            <div class="quote">
                Whatever you do, do it well.
            </div>

            <div class="quote-from">
                - Walt Disney
            </div>
        </div>
    </section>
</template>

<style lang="scss">

.hero{
    height:760px;
    width: 120%;
    background-color: #ffbcbc;
    transform: rotate(-5deg);
    position: relative;
    left: -50px;
    z-index:8;
    overflow: hidden;
    display: flex;
    flex-direction: row;

    img{
        height: 70%;
        width:35%;
        margin: 150px 0 0 120px;
        transform: rotate(5deg);
        animation: hero-image-fade 2.4s;
    }

    .hero-message{
        color: whitesmoke;
        text-align: center;
        transform: rotate(5deg);
        margin: 285px 0 0px 0px;
        width: 35%;
        display: flex;
        flex-direction: column;
        animation: hero-message-fade 4s;

        .quote{
            font-size: 5em;
        }

        .quote-from{
            font-size: 3em;
            text-align: right;
        }
    }
}



@media screen and (max-width: 768px){
    .hero{
        height: 70vh;

        img{
            display: none;
        }

        .hero-message{
            width: 100%;
            font-size: 0.6em;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
        }
    }
}

@keyframes hero-image-fade {
    from{
        opacity: 0.1;
        margin-left: -1000px;
        margin-top:-450px;
    }

    to{
        opacity: 1;
        margin: 150px 0 0 120px;
    }
}

@keyframes hero-message-fade{
    from{
        opacity: 0;
    }

    to{
        opacity: 1;
    }
}
</style>