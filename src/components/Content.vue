<template>
    <div>
        <div class="content">
            <div class="rows">
                <div class="description-content1">
                    <h2>Transform your brand</h2>
                    <p>We are a full-service creative agency specializing in helping brands grow fast. Engage your clients through compelling visuals that do most of the marketing for you.</p>
                    <a href="" class="1">LEARN MORE</a>
                </div>
                <div class="images-content">
                    <img src="@/../images/desktop/image-transform.jpg" alt="Egg">
                </div>
            </div>
            <div class="rows">
                <div class="images-content">
                    <img src="@/../images/desktop/image-stand-out.jpg" alt="Cup">
                </div>
                <div class="description-content2">
                    <h2>Stand out to the right audience</h2>
                    <p>Using a collaborative formula of designers, researchers, photographers, videographers, and copywriters, we’ll build and extend your brand in digital places.</p>
                    <a href="" class="2">LEARN MORE</a>
                </div>
            </div>
            <div class="rows">
                <div class="images-content">
                    <div v-if="tamañoVentana >= 980"><img src="@/../images/desktop/image-graphic-design.jpg" alt="Cherry"></div>
                    <div v-else class="content-mobile">
                        <img src="@/../images/mobile/image-graphic-design.jpg" alt="Egg">
                        <div class="content-mobile-description1">
                            <h4>Graphic design</h4>
                            <p>Great design makes you memorable. We deliver artwork that underscores your brand message and captures potential clients’ attention.</p>
                        </div>
                    </div>
                </div>
                <div class="images-content">
                    <div v-if="tamañoVentana >= 980"><img src="@/../images/desktop/image-photography.jpg" alt="Mandarine"></div>
                    <div v-else class="content-mobile">
                        <img src="@/../images/mobile/image-photography.jpg" alt="Mandarine">
                        <div class="content-mobile-description2">
                            <h4>Photography</h4>
                            <p>Increase your credibility by getting the most stunning, high-quality photos that improve your business image.</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="rows absolute" id="absolute" v-if="tamañoVentana >= 980">
                <div class="absolute-1">
                    <h4>Graphic design</h4>
                    <p>Great design makes you memorable. We deliver artwork that underscores your brand message and captures potential clients’ attention.</p>
                </div>
                <div class="absolute-2">
                    <h4>Photography</h4>
                    <p>Increase your credibility by getting the most stunning, high-quality photos that improve your business image.</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name:'Content',
    computed:{
        tamañoVentana(){
            return window.innerWidth;
        }
    }
}
</script>
<style scoped>
    .rows{
        display: grid;
        grid-template-columns: 1fr 1fr;
    }
    .description-content1 ,.description-content2{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: left;
        box-sizing: border-box;
    }
    .images-content{
        padding: 0;
    }
    img{
        width: 100%;
    }
    h2{
        font-family: 'Fraunces', serif;
        font-weight: 900;
        margin-bottom: 1em;
        padding-left: 4em;
        padding-right: 5em;
    }
    p{
        font-family: 'Barlow', sans-serif;
        margin-bottom: 2em;
        color: hsl(213, 9%, 39%);
        padding-left: 8em;
        padding-right: 5em;
    }
    .description-content2 p, .description-content2 a{
        padding-left: 6em;
        padding-right: 9em;
    }
    .description-content2 h2{
        padding-left: 3em;
    }
    a{
        font-family: 'Fraunces', serif;
        font-weight: 700;
        text-decoration: none;
        color: black;
        padding-left: 8em;
    }
    a[class="1"]:hover{
        text-decoration: underline #fed000 7px;
        text-underline-offset: -4.2px;
        color: black;
    }
    a[class="2"]:hover{
        text-decoration: underline #ff7465 7px;
        text-underline-offset: -4.2px;
        color: black;
    }
    .absolute{
        text-align: center;
        margin-top: -160px;
        margin-bottom: 9em;
    }
    .absolute p{
        font-size: 16px;
        padding: 0 6em;
    }
    h4{
        font-family: 'Fraunces', serif;
        font-weight: 700;
        font-size: 25px;
    }
    @media screen and (max-width:980px) {
        .rows{
            grid-template-columns: 1fr;
        }
        .description-content1,.description-content2,.absolute{
            padding: 2em;
            justify-content: center;
            text-align: center;
        }
        h2,p,a{
            padding: 0;
        }
        .description-content2 h2,.description-content2 p, .description-content2 a{
            padding: 0;
        }
        .content-mobile div{
            text-align: center;
            padding: 1em;
        }
        .content-mobile-description1{
            margin-top: -14em;
        }
        .content-mobile-description2{
            margin-top: -11em;
            margin-bottom:6em;
        }
        .content-mobile p{
            margin: 0;
        }
    }
    </style>