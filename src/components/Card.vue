<template>
  <router-link :to="`checkout=${donation.id}`"  class="text-decoration font"> 
    <div id='card' class='donations-card'>
      <h5 class="mdc-typography--headline5 ">{{donation.school}}</h5>
      <h6 class="mdc-typography--subtitle1">{{donation.name}}</h6>
      <!-- <h5 class="mdc-typography--headline5 text-underline">Items</h5> -->
      <!-- <ul class="mdc-list">
        <li class="mdc-list-item text-decoration">{{ donation.supply_name }}</li>
      </ul>  -->
    </div>
  </router-link>    
</template>

<script>
export default {
  name: "Card",
  props: ['donation']
};
</script>

<style>
.font {
  color: #000000;
}
.text-decoration{
  text-decoration: none;
}
.text-underline{
  text-decoration:underline;
}
.donations-card {
  color: black;
  background-image: linear-gradient(rgba(255,255,255,0.9), rgba(0,0,0,0));
  height: 15vw;
  width: 20vw;
  margin: 16px;
  padding: 3%;
  border-radius: 5px;
}

.donations-card:hover {
  	box-shadow: inset 0 0 0 3px  black;
}
.donations-card:active {
  background-image: linear-gradient(rgba(255,255,255,0.6), rgba(0,0,0,0));
  box-shadow: inset 0 0 0 3px  rgba(0,0,0,0.5);
}
</style>