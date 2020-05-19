<template>
    <footer>
        <section class="footer-info">
            ads
        </section>

        <section class="copyright">
            <p>Copyright 2020 - <a href="https://github.com/JermaineDavy/rene_portfolio" target="_blank">Jermaine Davy</a>. All rights Reserved.</p>
        </section>
    </footer>
</template>

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

</style>