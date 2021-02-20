<template>
  <b-container class="Shop">
  
    <b-card
      title=" "
      :img-src="image"
      img-alt="Image"
      img-top
      tag="article"
      style="max-width: 20rem;"
      class="mb-2"
      img-height = "250"
    >
      
     {{h1}}<br /> <br />


     
     <b-button  @click="reduceclick">
        - <b-badge variant="light"></b-badge
      ></b-button>
      &nbsp; &nbsp;{{ count }}&nbsp; &nbsp;
      <b-button  @click="addclick">
        + <b-badge variant="light"></b-badge></b-button
      >
    
    </b-card>
     
    <br /> <br />
  
  
  

  </b-container>

</template>

<script>
export default {
  props: {
    image: String,
    title: String,
    tag: String,
    h1:String,
  },
  data() {
    return {
      count: 0,
     
    };
  },
  methods: {
    addclick() {
      this.count++;
      this.$emit("callbackcount");
      this.$emit("callbacksugar");
    },
   
    reduceclick() {
      this.count--;
      this.$emit("callbackcount1");
    },
  },
};
</script>
