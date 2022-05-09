<template>

  <div id="container__landing-page">
    
    <h1>
      Young Leaders Academy
    </h1>

    <h2>
      {{ (new Date().getHours() <= 16) && (new Date().getHours() >= 8) ? data.renderableContent[0].duringBusinessHours : data.renderableContent[0].outsideBusinessHours}}
    </h2>

  </div>

</template>

<script>
import data from '@/jsonData.json';
export default {
  name: 'LandingPage',
  data () {
    return {
      data: data
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
$regular-font: fangsong
h1,h2,h3
  font-family: $regular-font
h3 
  margin: 40px 0 0
ul 
  list-style-type: none
  padding: 0
li 
  font-family: $regular-font
  display: inline-block
  margin: 0 10px
a 
  color: #42b983
</style>