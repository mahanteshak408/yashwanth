<template>
    <v-footer
    class="bg-indigo-lighten-1 text-center d-flex flex-column"
 
    >
    <div class="flex flex-column">
    <span v-for="icon in icons" :key="icon.id" class="flex flex-column">  
       <!-- <div  > -->
        <v-btn
          :icon="icon.icon"
          
          class="mx-2"
          variant="text"
          @click="openUrl(icon)"
        ></v-btn>
      <!-- </div> -->
      </span>
   
  
      <!-- <div class="pt-0">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
      </div> -->
  
      <v-divider></v-divider>
  
      <div>
        {{ new Date().getFullYear() }} — <strong>Nakshatra</strong>
      </div>
      </div>
    </v-footer>
  </template>


  <script>
  export default {
    data(){
      return {
      icons: [
       { id:1,icon:'mdi-facebook',link:"https://www.facebook.com/share/1ALLp5jTsr/?mibextid=qi2Omg"},
        {id:2,icon:'mdi-twitter',link:"https://www.threads.net/@naksh.atra860"},
        {id:3,icon:'mdi-linkedin',link:"https://www.linkedin.com/in/shreenivasa-enterprises-160b4932b?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app"},
        {id:4,icon:'mdi-twitter',link:"https://wa.me/919353255860"},
        {id:4,icon:'mdi-instagram',link:"https://www.instagram.com/naksh.atra860/profilecard/?igsh=MTJnY3M0eHNwOHY4aQ=="},
      ],
    
     }
    },
     methods:{
      openUrl(icon){
        window.open(icon.link, '_blank');

      }
     }
  }
</script>