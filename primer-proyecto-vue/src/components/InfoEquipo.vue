<template>
  <div>
    <h4>Nombre del equipo: {{ this.equipo }}</h4>
    <h3>Nombre corto: {{ this.shortName }}</h3>
    <h2>Año de formacion: {{ this.anio }}</h2>
    <h2>Deporte: {{ this.deporte }}</h2>
    <h2>Liga: {{ this.liga }}</h2>
    <ol></ol>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      equipo: '',
      shortName: '',
      anio: '',
      deporte: '',
      liga: '',
    };
  },
  props: ['id'],
  watch: {
    id: {
      async handler() {
        console.log('handler working');
        await this.getTeamInfo();
      },
      inmediate: true,
    },
  },
  methods: {
    async getTeamInfo() {
      return axios
        .get(
          `https://www.thesportsdb.com/api/v1/json/1/searchteams.php?t=${this.id}`
        )
        .then((response) => {
          console.log(response.data.teams[0]);
          this.equipo = response.data.teams[0].strTeam;
          this.shortName = response.data.teams[0].strTeamShort;
          this.anio = response.data.teams[0].intFormedYear;
          this.deporte = response.data.teams[0].strSport;
          this.liga = response.data.teams[0].strLeague;
        });
    },
  },
};
</script>

<style></style>
