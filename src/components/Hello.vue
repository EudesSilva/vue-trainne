<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <div>
      <ul>
          <li v-for="user in users">
           {{user.firstName}} {{user.lastName}}
          </li> 
      </ul>
    </div>

  <hr />
     <div>
        <input type="text" v-model="digitValue">
    </div>
    <div>
        Digit Value: <span v-text="digitValue" />
    </div> 
    <hr />
       <div>
           <button v-on:click="numberClicks++">Click number {{numberClicks}}</button>
       </div>
  </div>
</template>

<script>
export default {
  name: 'hello',

  data () {
    return {
      msg: 'Welcome to Your Vue',

      users:[
              { firstName:'Maria', lastName:'souza' },
              { firstName:'Jose', lastName:'maria' }
           ],

      digitValue:'',

      numberClicks:0
    }
  }
}
</script>


<style scoped> 
</style>
