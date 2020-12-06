<template>
  <div id="app">
    <Api></Api>
    <div class="container mt-3">
      <div class="row justify-content-between">
        <div class="col " v-for="(member, index) of member" :key="index">
          <TeamCard :member="member"></TeamCard>
        </div>
      </div>
    </div>

    <PageFooter></PageFooter>
  </div>
</template>

<script>
import PageFooter from "./components/PageFooter";
import TeamCard from "./components/TeamCard";
import Api from "./components/Api";
export default {
  name: "App",
  components: {
    PageFooter,
    TeamCard,
    Api,
  },

  data() {
    return {
      member: [
        {
          codigo: 1,
          nombre: "Diego Huertas",
          descripcion:
            "Amo de casa que subió 14 kilos durante la pandemia. Le gusta visitar ciudades y dormir",
          rol: "Desarrollador FrontEnd",
          image: "https://placeimg.com/210/200/people",
        },
        {
          codigo: 2,
          nombre: "Efrain Perdomo",
          descripcion:
            "Herrero apasionado por la ocarina. Se ha casado tres veces y le gusta ir a la playa.",
          rol: "Desarrollador Frontend",
          image: "https://placeimg.com/190/200/people",
        },
        {
          codigo: 3,
          nombre: "Libny Lopez",
          descripcion:
            "Alquimista de profesión que caza cuervos en su tiempo libre. También inventó la rueda.",
          rol: "Desarrollador backend",
          image: "https://placeimg.com/210/200/people",
        },
      ],
    };
  },
};
</script>
