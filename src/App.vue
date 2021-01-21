<template>
  <!-- at place of this you can also use v-text="name" -->
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
  <h1 v-if="isShowing"> this is showing on is showing v-if property </h1>
  <!-- this does not delete the element from dom it make its css display property to none  -->
  <h4 v-if="isShowing"> this is showing on is v-show property </h4>
  <!-- if else if -->
  this don't remove it
  <h1 v-if="isShowing" v-html="html"> </h1>
  <!-- === 3 equal how you say equal here -->
  <h3 v-else-if="isShowing === null"> This is v-else-if</h3>
  <!-- this is final if else in if else -->
  <h2 v-else> This is v-else</h2>
  <h1 v-show="isShowing"> {{count}}</h1>
  <!-- this is used when we want to show something once and not update the value of it -->
  <h1>  This will be showed once no update on dom <br>
    <span>Count is:</span>
    {{count}}
  </h1>
</template>

<script>
export default {
  data() { // this will return an object that will store the state
    return {
      name: "Hello is it working",
      number: 12,  
      html: "<h1> This is html </h1>", // checking how to get html as variable
      isShowing: true, // it is good to use is in the start of a boolean variable
      count: 1, // we are trying out showing number with v-show
    };
  },
  // mounted(){
  //   setInterval(() => {
  //     this.count ++;
  //   }, 1000);
  // }
}
</script> 