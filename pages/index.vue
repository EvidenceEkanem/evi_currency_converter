<template>
    <div>
        <Main />
        <List />
        <Footer />
    </div>
</template>	
       
<script>
    import Main from "../components/Main.vue"
    import List from "../components/List.vue"
    import Footer from "../components/Footer.vue"

export default {
    components: {
        Main, 
        List,
        Footer
    },
    head () {
    return {
      script: [
 
      ],
      link: [

      ]
    }
  }
}
</script>

