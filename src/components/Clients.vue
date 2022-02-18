<template>
    <div>
        <p>CLIENT TESTIMONIALS</p>
        <div class="clients">
          <div class="clients-content">
            <img src="@/../images/image-emily.jpg" alt="photo-emily">
            <p>We put our trust in Sunnyside and they delivered, making sure our needs were met and deadlines were always hit.</p>
            <h5>Emily R.</h5>
            <p>Marketing Director</p>
          </div>
          <div class="clients-content">
            <img src="@/../images/image-thomas.jpg" alt="photo-thomas">
            <p>Sunnyside’s enthusiasm coupled with their keen interest in our brand’s success made it a satisfying and enjoyable experience.</p>
            <h5>Thomas S.</h5>
            <p>Chief Operating Officer</p>
          </div>
          <div class="clients-content">
            <img src="@/../images/image-jennie.jpg" alt="photo-jennie">
            <p>Incredible end result! Our sales increased over 400% when we worked with Sunnyside. Highly recommended!</p>
            <h5>Jennie F.</h5>
            <p>Business Owner</p>
          </div>
        </div>
    </div>
</template>
<script>
export default {
    name:"Clients"
}
</script>
<style scoped>
  .clients{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    text-align: center;
  }
  img{
    border-radius: 100px;
    width: 30%;
    margin-bottom: 3em;
  }
  p{
    margin-top: 0;
    margin-bottom: 3em;
    text-align: center;
    color: hsl(213, 9%, 39%);
    font-family: 'Barlow', sans-serif;
  }
  p:first-child{
    font-family: 'Fraunces', serif;
    font-size: 20px;
    letter-spacing: 4px;
    color: hsl(232, 10%, 55%);
  }
  h5{
    font-family: 'Fraunces', serif;
    font-weight: 900;
  }
  .clients-content{
    margin-bottom: 3em;
    padding: 4em;
  }
  .clients-content p:last-child{
    color: hsl(210, 4%, 67%);
  }
  @media screen and (max-width:980px) {
        .clients{
            grid-template-columns: 1fr;
            padding: 0 2em;
        }
        .clients-content{
            margin-bottom: 2em;
            padding: 0;
        }
  }
</style>