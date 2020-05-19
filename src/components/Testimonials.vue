<template>
    <section class="testimonials">
        <div class="testimonial-background">
            <div class="testimonial-container">
                <div class="slide">
                    <img :src="getSlideImage" alt="">

                    <div class="caption">
                        {{ getSlideCaption  }}
                    </div>
                </div>

                <a class="previous-slide" @click="changeSlide(-1)">&#10094;</a>
                <a class="next-slide" @click="changeSlide(1)">&#10095;</a>
            </div>

            <div class="slide-dots">
                <span v-for="(slide, index) in slides" :key="index" @click="selectSlide(index)" v-bind:class="[(index == (currentSlide-1)) ? 'slide-dot active-dot': 'slide-dot']"></span>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data(){
        return {
            currentSlide: 1,
            slides: [
                {
                    id: 1,
                    image: '/images/undraw_profile_pic_ic5t.svg',
                    caption: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Lectus magna fringilla urna porttitor rhoncus dolor purus non enim.'
                },
                {
                    id: 2,
                    image: '/images/undraw_male_avatar_323b.svg',
                    caption: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Gravida neque convallis a cras semper. Nisl condimentum id venenatis a condimentum vitae sapien.'
                },
                {
                    id: 3,
                    image: '/images/undraw_female_avatar_w3jk.svg',
                    caption: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Suscipit tellus mauris a diam maecenas sed. Commodo viverra maecenas accumsan lacus vel facilisis volutpat est velit.'
                }
            ]
        };
    },

    methods: {
        changeSlide(slideDirection){
            if(this.currentSlide == 1 && slideDirection == -1){
                this.currentSlide = this.slides.length;
            }else if(this.currentSlide == this.slides.length && slideDirection == 1){
                this.currentSlide = 1;
            }else{
                this.currentSlide = this.currentSlide + slideDirection;
            }
        },

        selectSlide(slideId){
            this.currentSlide = slideId + 1;
        }
    },

    computed: {
        getSlideImage(){
            return this.slides[this.currentSlide - 1].image;
        },

        getSlideCaption(){
            return this.slides[this.currentSlide - 1].caption;
        },

        getSlideDotClass(index){
            if(this.currentSlide == index){
                return 'slide-dot active';
            }

            return 'slide-dot';
        }
    }
}
</script>

<style lang="scss">

.testimonials{
    height: 600px;
    width: 100%;
    background: url(/images/nathalie-spehner-vR6gQ52qe-E-unsplash.jpg);
    background-size: 100%;

    .testimonial-background{
        width: 100%;
        height: 100%;
        background-color: rgba(221, 160, 221, 0.452);
        position: relative;

        .slide-dots{
            text-align: center;

            .slide-dot{
                cursor: pointer;
                width: 15px;
                height: 15px;
                margin: 0 8px;
                background-color: #bbb;
                border-radius: 50%;
                display: inline-block;
                transition: background-color 0.6s ease;
            }

            .active-dot, .slide-dot:hover{
                background-color: #717171;
            }
        }
    }
}

.testimonial-container{
    .slide{
        animation: fade 1.5s;
        width: 40%;
        position: relative;
        margin:auto;
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 190px 0 50px 0;
        
        img{
            width: 130px;
            height: 130px;
            border: 5px solid whitesmoke;
            border-radius:50%;
            margin-bottom: 20px;
        }

        .caption{
            color: whitesmoke;
        }
    }

    .previous-slide, .next-slide{
        cursor: pointer;
        position: absolute;
        top: 50%;
        width: auto;
        margin-top: -22px;
        padding: 16px;
        font-weight: bold;
        font-size: 26px;
        transition: 0.6s ease;
        border-radius: 0 3px 3px 0;
        user-select: none;
    }

    .previous-slide:hover, .next-slide:hover{
        background-color: rgba(0,0,0,0.8);
    }

    .next-slide{
        right: 0;
        border-radius: 3px 0 0 3px;
    }
}

@keyframes fade {
    from{
        opacity: 0.4;
    }

    to{
        opacity: 1;
    }
}

@media screen and (max-width: 768px){
    .testimonial-container{
        .slide{
            padding: 110px 0 110px 0;
        }
    }
}

</style>