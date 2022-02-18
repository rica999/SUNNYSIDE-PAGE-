<template>
    <div>
        <div class="images">
            <img src="@/../images/desktop/image-gallery-milkbottles.jpg" alt="Milkbottles">
            <img src="@/../images/desktop/image-gallery-orange.jpg" alt="Orange">
            <img src="@/../images/desktop/image-gallery-cone.jpg" alt="Icecream-cone">
            <img src="@/../images/desktop/image-gallery-sugarcubes.jpg" alt="Sugar-cubes">
        </div>
    </div>
</template>
<script>
export default {
    name:'Prefooter'
}
</script>
<style scoped>
    .images{
        display: grid;
        grid-template-columns: repeat(4,1fr);
    }
    img{
        width: 100%;
    }
    @media screen and (max-width:980px) {
        .images{
            grid-template-columns: 1fr 1fr;
        }
    }
</style>