<template>
<div>
   <form @submit.prevent="formHandler">
    <div>
         <input class="myInput" type="email" name="email" id="email" v-model="email">
    <!-- <span v-text="email"></span> -->
    </div>
    <div>
        <input class="myInput" type="password" name="password" id="password" v-model="password">
    </div> 
    <button class="button button1" type="submit" >Green</button>
   </form>
   <h2> form data:</h2>
   <p>email:{{ email }}</p>
   <p>password:<span v-text="password"></span></p>

</div>
</template>

<script>
export default{
    data(){
       return{
        email:'example@gmail.com',
        password:'1234',

       }
    },
    methods:{
        // changeInput(event){
        //  this[event.target.name]= event.target.value;

            
        // },
        formHandler(){
            console.log(this.email , this.password);
        }
    }
}
</script>
<style>
.myInput{
    width: 300px;
    height: 50px;
    border-radius: 30px;

}
.button {
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  border-radius: 20px;
}

.button1 {background-color: #04AA6D;} /* Green */
.button2 {background-color: #008CBA;} /* Blue */
</style>