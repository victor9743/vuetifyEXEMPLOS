<template >
  <v-app style="background-color: #ffe0cc">
  
   

  

    <v-form id="area_login" ref="form" v-model="valid" lazy-validation class="rounded-xl">
      <v-parallax src="https://cdn.vuetifyjs.com/images/parallax/material.jpg" class="rounded-xl">
      <div class="nome rounded-xl" >
       <v-text-field
        v-model="name"
        :counter="10"
        :rules="nameRules"
        label="Usuário"
        required
        
      ></v-text-field>

    </div>

    <div class="nome rounded-xl">
      <v-text-field
        v-model="email"
        :rules="emailRules"
        label="E-mail"
        required
      ></v-text-field>

    </div>

    <div class="nome rounded-xl">

       <v-checkbox
        v-model="checkbox"
        :rules="[v => !!v || 'You must agree to continue!']"
        label="Do you agree?"
        required
      ></v-checkbox>

    </div>
     
      <div id="footer">

        <v-btn
          :disabled="!valid"
          color="success"
          class="mr-4"
          @click="validate"
        >
          Validate
          </v-btn>

        <v-btn
          color="red darken-3"
          class="mr-4"
          @click="reset"
        >
          Reset Form
        </v-btn>

      </div>
      </v-parallax>
  
     </v-form>
  
  
  </v-app>
</template>

<script>


export default {

  data: () => ({
    //
  }),
};
</script>
<style lang="css">


    #area_login{
   
      margin: auto;
      height: 500px;      
      
    }
    .nome{
      margin-top:20px;
      margin-left: 5%;
      margin-right:5%;
      padding:10px;
      background-color: #fff0e6
    }
    #footer{
      margin-top: 30px;
      padding:20px;
    }
  

</style>
