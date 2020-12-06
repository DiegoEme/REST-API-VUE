<template>
  <div>
    <div class="container mt-3">
      <div class="row d-flex justify-content-around">
        <div
          class="card  border-info"
          style="width: 18rem;"
          v-bind:key="item.id"
          v-for="item in member"
        >
          <img class="card-img-top" :src="item.image" />
          <div class="card-body">
            <h5 class="card-title">{{ item.nombre }} - {{item.codigo}}</h5>
            <p class="card-text">
              {{ item.descripcion }}
            </p>
            <p class="card-text">
              {{ item.rol }}
            </p>
          </div>
        </div>
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
