<template>
    <div class="d-flex justify-content-center">
        <div class="title">
            <h1>WE ARE CREATIVES</h1>
            <!--<img src="@/../images/icon-arrow-down.svg" alt="Arrow">-->
        </div>
        <div v-if="tamañoVentana >= 980">
            <img src="@/../images/desktop/image-header.jpg" alt="Orange" width="100%">
        </div>
        <div v-else>
            <img src="@/../images/mobile/image-header.jpg" alt="Orange" width="100%">
        </div>
    </div>
</template>
<script>
export default {
    name:"Header",
    computed:{
        tamañoVentana(){
            return window.innerWidth;
        }
    }
}
</script>
<style scoped>
    .d-flex{
        flex-direction: column;
    }
    .title{
        margin-bottom: -15em;
        z-index: 1;
    }
    h1{
        font-family: 'Fraunces', serif;
        color: white;
        background-color: #3DBEFF;
        margin: 0;
        text-align: center;
        font-size: 4em;
        padding-top: 1em;
    }
    img[alt="Arrow"]{
        position: absolute;
        top: 28.220858895705522vw;
        font-size: 3px;
    }
    @media screen and (max-width:980px) {
        h1{
        font-size: 3em;
        letter-spacing: 5px;
    }
    }
</style>