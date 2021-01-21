<template>
  <h2> {{ name }}</h2> <!-- we getting value of name from data -->
  <!-- to make it upper case but only work on text, .toUpperCase() is vannila java script-->
  <h2> {{ name.toUpperCase() }}</h2>
  <!-- and you can also do basic operations but you need to put value in {{}} -->
  <h3> {{number + 10}}  </h3>
  <!-- so this is not working  -->
  <h3> {{html}} </h3>
  <!-- we need to use v-html directive  giving direction to tell vue to treate it as a html coming in  -->
  <div v-html="html"></div>
  <!-- this is dangerous for risk xss attack -->
  <p> so what we can do </p>
  <h1> this is showing </h1>
  <!-- this will not show because isShowing prperty is inactive -->
  <h1 v-if="isShowing"> this is showing on is showing property </h1>
  <!-- if else if -->
  <h1 v-if="isShowing" v-html="html"> </h1>
  <h3 v-else-if="isShowing === null"> This is v-else-if</h3>

</template>

<script>
export default {
  data() { // this will return an object that will store the state
    return {
      name: "Hello is it working",
      number: 12,  
      html: "<h1> This is html </h1>", // checking how to get html as variable
      isShowing: true, // it is good to use is in the start of a boolean variable
    }
  }
}
</script> 