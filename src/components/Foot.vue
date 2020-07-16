<template>
    <footer>
        <section class="footer-info">
            <!--
                Be sure to add the following somewhere in the footer.

                Designed by [Freepik](https://www.flaticon.com/search?author_id=1) from [FlatIcon](https://www.flaticon.com)

                This is the designer attribution for the favicon
            -->
        </section>

        <section class="copyright">
            <p>Copyright 2020 - <a href="https://github.com/JermaineDavy/rene_portfolio" target="_blank">Jermaine Davy</a>. All rights Reserved.</p>
        </section>

        <a href="#top" :class="floatingButtonClass">
            <i class="fas fa-arrow-up"></i>
        </a>
    </footer>
</template>

<script>
export default {
    data(){
        return {
            floatingButtonClass: 'floating-button'
        };
    },

    methods: {
        scrollHandler(){
            if(window.scrollY > 175){
                this.floatingButtonClass = 'floating-button show-floating-button';
            }else{
                this.floatingButtonClass = 'floating-button';
            }
        },
    },

    created(){
        window.addEventListener('scroll', this.scrollHandler);
    },

    destroyed(){
        window.removeEventListener('scroll', this.scrollHandler);
    }
}
</script>

<style lang="scss">
$copyrightHeight: 80px;

footer{
    width: 100%;
    height: 400px;
    background-color:#AFEEEE;

    .footer-info{
        width: 100%;
        height: 319px;
    }

    .copyright{
        width: 100%;
        height: $copyrightHeight;
        border-top: 1px solid whitesmoke;
        display: flex;
        align-items: center;
        justify-content: center;

        p{
            a, a:visited{
                color: #fd9999;
                text-decoration: none;
            }

            a:hover{
                color: #ffbcbc;
            }
        }
    }
}

.floating-button{
    position: fixed;
    bottom: 20px;
    right: 30px;
    width: 60px;
    height: 60px;
    background-color: rgba(221, 160, 221, 1);
    color: white;
    font-size: 30px;
    border: none;
    border-radius: 50%;
    display: none;
    justify-content: center;
    align-items: center;
    text-decoration: none;

    &:hover{
        background-color: rgb(255, 116, 255);
    }
}

.show-floating-button{
    display:flex;
}

</style>
