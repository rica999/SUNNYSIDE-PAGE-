<template>
  <div id="app">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <div>
        <Navbar></Navbar>
        <Header></Header>
        <Content></Content>
        <Clients></Clients>
        <Prefooter></Prefooter>
        <Footer/>
    </div>
    <router-view/>
  </div>
</template>
<script>
import Navbar from '@/components/Navbar.vue'
import Header from '@/components/Header.vue'
import Content from '@/components/Content.vue'
import Clients from '@/components/Clients.vue'
import Prefooter from '@/components/Previus-footer.vue'
import Footer from '@/components/Footer.vue'

export default {
    name:'App',
    components:{
        Navbar,
        Header,
        Content,
        Clients,
        Prefooter,
        Footer
    }
}
</script>
<style>
    @import url('https://fonts.googleapis.com/css2?family=Barlow:wght@600;700;900&family=Fraunces:wght@700;900&display=swap');
    #app{
      margin:0;
      padding: 0;
    }
</style>