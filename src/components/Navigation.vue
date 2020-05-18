<template>
    <nav>
        <div class="logo-container">
            <img src="/images/rene.svg" alt="">
        </div>
    </nav>
</template>

<style lang="scss">

nav{
    height: 100px;
    width: 100%;
    background-color: #ffbcbc;
    border-bottom: 1px solid #AFEEEE;
    position: fixed;
    z-index: 10;

    .logo-container{
        height: 100px;

        img{
            height: 90px;
        }
    }
}

@media screen and (max-width: 768px){
    nav{
        height: 70px;

        .logo-container{
            height: 80px;

            img{
                height: 80px;
                position: absolute;
                top: -8px;
            }
        }
    }
}

</style>