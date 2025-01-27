<template>
  <div class="">
    <v-sheet class="mx-auto" elevation="8" max-width="800">
      <v-slide-group
        v-model="modelFirst"
        class="py-2"
        selected-class="bg-success"
        show-arrows
      >
        <v-slide-group-item
          v-for="product in products"
          :key="product"
          v-slot="{ isSelected, toggle, selectedClass }"
        >
   
        <v-avatar icon="$vuetify" :image="product.image" size="80"></v-avatar>
        </v-slide-group-item>
      </v-slide-group>
    </v-sheet>

    <v-sheet class="mx-auto" elevation="8" max-width="800">
      <v-slide-group
        v-model="modelImage"
      class="py-2"
  
      >
        <v-slide-group-item
          v-for="product in productsImages"
          :key="product"
          v-slot="{ isSelected, toggle, selectedClass }"
        >
         
            <v-img :src="product.image" height="200"     width="100%" cover></v-img>
    
        </v-slide-group-item>
      </v-slide-group>
    </v-sheet>

    <v-sheet elevation="8" >
      <v-slide-group
        v-model="model"
        class="py-2"
        selected-class="bg-success"
        show-arrows
      >
        <v-slide-group-item
          v-for="product in products"
          :key="product"
          v-slot="{ isSelected, toggle, selectedClass }"
        >
          <v-card
            :class="['ma-2', selectedClass]"
            color="grey-lighten-1"
            height="150"
            width="100"
            @click="toggle"
          >
            <v-img :src="product.image" height="100" cover></v-img>
            <v-card-text class="">
              {{ product.name }}
              <span class="description">{{ product.description }}</span>
            </v-card-text>
            <v-card-actions>
              <v-btn color="primary" icon="mdi mdi-cart-outline"></v-btn>
              <!-- @click="addToCart(product)" -->
            </v-card-actions>
            <div class="d-flex h-24 align-center justify-center">
              <v-scale-transition> </v-scale-transition>
            </div>
          </v-card>
        </v-slide-group-item>
      </v-slide-group>
    </v-sheet>
  </div>
</template>

<script>
export default {
  data (){
    return{
    model: null,
    modelImage:null,
    modelFirst:null,
    
    productsImages:[ {
        id: 1,
        name: "Product 1",
        description: "Description  of  Agarbatti",
        image: "/image.jpeg",
      },
      {
        id: 2,
        name: "Product 2",
        description: "Description of Agarbatti",
        image: "/scroll1.jpeg",
      },
      {
        id: 3,
        name: "Product 2",
        description: "Description of Agarbatti",
        image: "/scroll4.jpeg",
      },
      {
    id: 4,
    name: "Product 2",
    description: "Description of Agarbatti",
    image: "/scroll.jpeg",
  },  {
    id: 5,
    name: "Product 2",
    description: "Description of Agarbatti",
    image: "/scroll1.jpeg",
  },
  {
    id: 6,
    name: "Product 2",
    description: "Description of Agarbatti",
    image: "/scroll3.jpeg",
  },  {
    id: 7,
    name: "Product 2",
    description: "Description of Agarbatti",
    image: "/scroll4.jpeg",
  },
     ],
    products: [
      {
        id: 1,
        name: "Product 1",
        description: "Description  of  Agarbatti",
        image: "/agarabathi.jpg",
      },
      {
        id: 2,
        name: "Product 2",
        description: "Description of Agarbatti",
        image: "/agarabathi2.jpeg",
      },
      {
        id: 1,
        name: "Product 1",
        description: "Description  of  Agarbatti",
        image: "/agarabathi.jpg",
      },
      {
        id: 2,
        name: "Product 2",
        description: "Description of  Agarbatti",
        image: "agarabathi2.jpeg",
      },
      {
        id: 1,
        name: "Product 1",
        description: "Description  of  Agarbatti",
        image: "agarabathi2.jpeg",
      },
      {
        id: 2,
        name: "Product 2",
        description: "Description of  Agarbatti",
        image: "agarabathi2.jpeg",
      },
      // Add more products as needed
    ],
  }
},
};
</script>

<style scoped>
.description {
  font-size: x-small;
}

.v-card-text {
  padding: 0.5rem;
}

:deep(.v-slide-group__prev ){
   
    min-width: 10px !important;

}
:deep(.v-slide-group__next)
{
   
   min-width: 10px !important;

}
:deep(.bg-grey-lighten-1 ){
  background-color: #94bda0e0 !important;
    color: #0d0c0c !important;
}
</style>
