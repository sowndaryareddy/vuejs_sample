<template>
      <div id = "vue_det">
         <h1>Firstname : {{firstname}}</h1>
         <h1>Lastname : {{lastname}}</h1>
           <h1>{{ getFullName(firstname, lastname) }}</h1>
           <p>Computed reversed message: "{{ reversedMessage }}"</p>
           <input v-model="message" placeholder="enter message">
<p>Message is: {{ message }}</p>
           <ul>
<li v-for="item in items">{{item}}</li>
           </ul>
      </div>
       </template>
<script>
export default {
  name: 'User',
  data () {
    return {
      firstname: 'Welcome to Your ',
      lastname: 'Vue.js App',
        message: null,
        items:[
          'Laptop',
          'Charger',
          'Mouse'
        ]
    }
  },
  computed: {
    reversedMessage: function () {
      return this.firstname.split('').reverse().join('')
    }
  },
 methods: {
   
      getFullName: function(first,last) {
      return first+' '+last;
    }
  }
}
</script>



