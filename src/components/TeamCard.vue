<template>
  <div>
    
        <div
          class="card  border-info"
          style="width: 18rem;"
          
        >
          <img class="card-img-top" :src="member.image" />
          <div class="card-body">
            <h5 class="card-title">{{ member.nombre }} - {{member.codigo}}</h5>
            <p class="card-text">
              {{ member.descripcion }}
            </p>
            <p class="card-text">
              {{ member.rol }}
            </p>
          </div>
        </div>
      
  </div>
</template>

<script>
export default {
  name: "TeamCard",
  props: ["member"],
};
</script>

<style scoped></style>
