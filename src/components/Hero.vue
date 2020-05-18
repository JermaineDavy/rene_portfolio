<template>
    <section class="hero">
        <img src="/images/undraw_quality_time_wiyl.svg" alt="">

        <div class="hero-message">
            Welcome to my place.
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
        margin: 150px 0 0 150px;
        transform: rotate(5deg);
    }

    .hero-message{
        font-size: 6em;
        color: whitesmoke;
        text-align: center;
        transform: rotate(5deg);
        margin: 285px 0 0 60px;
    }
}

@media screen and (max-width: 768px){
    .hero{
        height: 80vh;

        img{
            display: none;
        }

        .hero-message{
            font-size: 2.4em;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
        }
    }
}

</style>