<template>
  <div class="backgrnd">
    <Navbar />
    <Transition>
      <div v-if="cargando" class="spin">
        <img
          class="img"
          :src="'https://isys-assets-bucket.s3.amazonaws.com/logos/logo.png'"
        />
      </div>
    </Transition>
    <div
      v-show="!cargando"
      v-if="this.$store.state.user.type == 'Supervisor en Sitio'"
      class="general"
    >
      <h3>
        Dashboard
      </h3>

      <a
        class="navbar-option"
        @click="this.$router.push('/validate_evaluacions')"
        href="#"
        ><i class="fas fa-user-check"></i> Validar Afiliado</a
      >
      <a
        class="navbar-option"
        @click="this.$router.push('/listevalssupSitio')"
        href="#"
        ><i class="fas fa-list"></i> Jornadas</a
      >

      <!-- <button
        @click="this.$router.push('/evaluacions')"
        class="btn btn-success btn-sm"
        type="button"
      >
        <i class="fas fa-file" _mstvisible="2"></i> Evaluaciones
      </button> -->
      <br />
      <br />
    </div>
    <div
      v-show="!cargando"
      v-if="this.$store.state.user.type == 'Encargada de Verificación'"
      class="general"
    >
      <h3>
        Dashboard
      </h3>
      <a
        class="navbar-option"
        @click="this.$router.push('/listevalsencvalid')"
        href="#"
        ><i class="fas fa-list"></i> Listado de Evaluaciones</a
      >
      <br />
      <br />
    </div>
    <div
      v-show="!cargando"
      v-if="this.$store.state.user.type == 'Médico Nutricionista'"
      class="general"
    >
      <h3>
        Dashboard
      </h3>
      <a
        class="navbar-option"
        @click="this.$router.push('/listevalsmednutric')"
        href="#"
        ><i class="fas fa-list"></i> Listado de Evaluaciones</a
      >
      <br />
      <br />
    </div>
    <div
      v-show="!cargando"
      v-if="this.$store.state.user.type == 'Auditora Interna'"
      class="general"
    >
      <h3>
        Dashboard
      </h3>
      <a
        class="navbar-option"
        @click="this.$router.push('/evaluacionsprtscn')"
        href="#"
        ><i class="fas fa-list"></i> Jornadas</a
      >
      <br />
      <br />
    </div>
    <div
      v-show="!cargando"
      v-if="this.$store.state.user.type == 'Encargada de Facturación'"
      class="general"
    >
      <h3>
        Dashboard
      </h3>

      <a
        class="navbar-option"
        @click="this.$router.push('/encFactEvalsAuto')"
        href="#"
        ><i class="fas fa-list"></i> Autorizaciones</a
      >
      <br />
      <div id="embeddingContainer"></div>
      <br />
    </div>
    <div
      v-show="!cargando"
      v-if="this.$store.state.user.type == 'Analista de Datos'"
      class="general"
    >
      <h3>
        Dashboard
      </h3>

      <br />
      <div id="embeddingContainerAnalDats"></div>
      <br />
    </div>
    <div
      v-show="!cargando"
      v-if="this.$store.state.user.type == 'Auxiliar de Validación'"
      class="general"
    >
      <h3>
        Dashboard
      </h3>
      <a
        class="navbar-option"
        @click="this.$router.push('/listevalsauxvalid')"
        href="#"
        ><i class="fas fa-list"></i> Jornadas</a
      >
      <br />
      <br />
    </div>
    <div
      v-show="!cargando"
      v-if="
        this.$store.state.user.type ==
          'Subgerente de Promoción de la Salud y Prevención de la Enfermedad (P&P)'
      "
      class="general"
    >
      <h3>
        Dashboard
      </h3>
      <a
        class="navbar-option"
        @click="this.$router.push('/expediente')"
        href="#"
        ><i class="far fa-file-alt"></i> Expediente</a
      >
      <br />
      <br />
    </div>
    <div
      v-show="!cargando"
      v-if="this.$store.state.user.type == 'Supervisor General'"
      class="general"
    >
      <h3>
        Dashboard
      </h3>
      <a class="navbar-option" @click="this.$router.push('/centros')" href="#"
        ><i class="far fa-building"></i> Centros</a
      >
      <a
        class="navbar-option"
        @click="this.$router.push('/listevalssupGener')"
        href="#"
        ><i class="fas fa-list"></i> Jornadas</a
      >
      <br />
      <br />
    </div>
    <div
      v-show="!cargando"
      v-if="this.$store.state.user.type == 'Gerente de Operaciones'"
      class="general"
    >
      <h3>
        Dashboard
      </h3>
      <a class="navbar-option" @click="this.$router.push('/centros')" href="#"
        ><i class="far fa-building"></i> Centros</a
      >
      <a
        class="navbar-option"
        @click="this.$router.push('/evaluacionsprtscn')"
        href="#"
        ><i class="fas fa-list"></i> Jornadas</a
      >
      <br />
      <br />
    </div>
    <div
      v-show="!cargando"
      v-if="this.$store.state.user.type == 'Coordinador de Operaciones'"
      class="general"
    >
      <h3>
        Dashboard
      </h3>
      <a class="navbar-option" @click="this.$router.push('/centros')" href="#"
        ><i class="far fa-building"></i> Centros</a
      >
      <a
        class="navbar-option"
        @click="this.$router.push('/evaluacionsprtscn')"
        href="#"
        ><i class="fas fa-list"></i> Jornadas</a
      >
      <br />
      <br />
    </div>
    <div
      v-show="!cargando"
      v-if="this.$store.state.user.type == 'Auxiliar de Convocatoria'"
      class="general"
    >
      <h3>
        Dashboard
      </h3>
      <!-- <a
        class="navbar-option"
        @click="this.$router.push('/evaluacionscierre')"
        href="#"
        ><i class="fas fa-calendar-day"></i> Cierres</a
      > -->
      <br />
      <div id="embeddingContainerAuxConvoc"></div>
      <br />
      <br />
      <br />
    </div>
  </div>
</template>

<script lang="ts">
import Navbar from "@/components/Navbar.vue";
import { getDash } from "@/services/dashboard/dashboardService";
import { getUrl2 } from "@/services/isys/QuicksightService";
import numeral from "numeral";
import Pusher from "pusher-js";
import moment from "moment";
import {
  embedDashboard,
  embedVisual,
  embedSession,
  embedQSearchBar,
} from "amazon-quicksight-embedding-sdk";
export default {
  name: "DashboardView",
  components: {
    Navbar,
  },

  data() {
    return {
      polyline_points:
        "50,300 100,167.5 150,100 250,80 350,160 450,100 550,100 650,150 750,200 750,300",
      imageUrl: "",
      dias: [] as any,
      presupuesto: 400000,
      presupuesto2: 2335000,
      usuariosCant: [] as any,
      facturasCant: [] as any,
      factsGpedByCli: [] as any,
      mejorasPend: [] as any,
      totales: {} as any,
      cargando: false,
      capurl: "",
      capurlAuxConvoc: "",
      capurlAnalDats: "",
    };
  },

  methods: {
    //   Dashboard(embeddedURL: any) {
    //   var containerDiv = document.getElementById("dashboardContainer");
    //   var options = {
    //     url: embeddedURL,
    //     container: containerDiv,
    //     scrolling: "yes",
    //     height: "850px",
    //     width: "100%"
    //   };
    //   this.dashboard = QuicksightEmbedding.embedDashboard(options);
    // }

    async GetDashboardURL() {
      const url = await getDash();
      alert(url);
    },
    getCx(index: any) {
      return this.$store.state.user.valores2[index];
    },

    getImg() {
      let cedulaAfiliadoActual = this.$store.state.user.defaultStatus[0].cedula;
      let urlPartOne = cedulaAfiliadoActual.slice(0, 3);
      let urlPartTwo = cedulaAfiliadoActual.slice(4, 6);
      let urlPartThree = cedulaAfiliadoActual.slice(6, 8);
      this.imageUrl = `http://www.arssenasa.gov.do/Sistemas/afiliacion/fotos/${urlPartOne}/${urlPartTwo}/${urlPartThree}/${cedulaAfiliadoActual}.jpg`;
    },

    formatDatePlus(dateValue: Date) {
      let out = moment(dateValue).add(30, "days");
      return moment(out).format("D/MM/yyyy");
    },

    formatDate(dateValue: Date) {
      let out = moment(dateValue).add(0, "days");
      return moment(out).format("D/MM/yyyy");
    },

    numeroAFecha(numeroDeDias: any, esExcel = false) {
      var diasDesde1900 = esExcel ? 25567 + 1 : 25567 + 2;

      // 86400 es el número de segundos en un día, luego multiplicamos por 1000 para obtener milisegundos.
      return new Date((numeroDeDias - diasDesde1900) * 86400 * 1000);
    },

    formatTable(dif: number) {
      if (dif < 0) {
        return "der red";
      } else {
        return "der green";
      }
    },

    getMonth(month: number) {
      switch (month) {
        case 1:
          return "Enero";
        case 2:
          return "Febrero";
        case 3:
          return "Marzo";
        case 4:
          return "Abril";
        case 5:
          return "Mayo";
        case 6:
          return "Junio";
        case 7:
          return "Julio";
        case 8:
          return "Agosto";
        case 9:
          return "Septiembre";
        case 10:
          return "Octubre";
        case 11:
          return "Noviembre";
        case 12:
          return "Diciembre";

        default:
          return "Error";
      }
    },
    getARS(id_ars: string) {
      switch (id_ars) {
        case "5":
          return "ARS CMD";
        case "14":
          return "MAPFRE SALUD ARS, S.A.";
        case "8":
          return "FUTURO";
        case "12":
          return "META SALUD";
        case "23":
          return "YUNEN";
        case "17":
          return "RESERVAS";
        case "13":
          return "MONUMENTAL";
        case "4":
          return "ASEMAP";
        case "1":
          return "ARS APS S A";
        case "21":
          return "SIMAG";
        case "16":
          return "RENACER";
        case "59":
          return "GRUPO MEDICO ASOCIADO";
        case "9":
          return "GRUPO MEDICO ASOCIADO";
        case "24":
          return "PRIMERA  ARS DE HUMANO";
        case "22":
          return "UNIVERSAL";
        case "29":
          return "ALBA GAS S.R.L.";
        case "10":
          return "HUMANO SEGUROS";
        case "20":
          return "SENASA CONTRIBUTIVO";
        case "61":
          return "SENASA SUBSIDIADO";
        case "18":
          return "SEMMA";
        case "65":
          return "IDOPPRIL";
        default:
          return "ARS Descripcion";
      }
    },

    toColor(type: string) {
      if (type == "1 - Recibido por Auditoría Interna") {
        return "valor1";
      } else if (type == "2 - Verificado por Auditoría Interna") {
        return "valor2";
      } else if (type == "3 - Verificado por Auditoría Externa") {
        return "valor3";
      } else if (type == "4 - Recibido por Reclamaciones Médicas") {
        return "valor4";
      } else if (type == "5 - Verificado por Reclamaciones Médicas") {
        return "valor5";
      } else if (type == "6 - Cargado a Lote") {
        return "valor6";
      } else if (type == "7 - Enviado a la Aseguradora") {
        return "valor7";
      } else if (type == "Todos") {
        return "Todos";
      }
    },

    valorTotal() {
      this.totales.dias = this.dias.length;
      this.totales.cantProductos = this.dias.reduce(
        (accum: any, item: any) => accum + item.count,
        0
      );

      // this.totales.count = this.periodos.reduce(
      //   (accum: any, item: any) => accum + item.count,
      //   0
      // );
      // this.totales.cobertura = this.periodos.reduce(
      //   (accum: any, item: any) => accum + item.cobertura,
      //   0
      // );
      // this.totales.facturas = this.facturasCant.reduce(
      //   (accum: any, item: any) => accum + item.count,
      //   0
      // );
      // this.totales.facturas2 = this.factsGpedByCli.reduce(
      //   (accum: any, item: any) => accum + item.count,
      //   0
      // );
      // this.totales.cobertura2 = this.factsGpedByCli.reduce(
      //   (accum: any, item: any) => accum + item.cobertura,
      //   0
      // );
      // this.totales.cantClientes = this.factsGpedByCli.length;
    },

    pusherSubscribe() {
      // Start pusher subscribe
      var pusher = new Pusher("f2c972e55a9c9eac5f9a", {
        cluster: "us2",
      });

      var channel = pusher.subscribe("my-channel");
      channel.bind("my-event", (data: any) => {
        this.loadfacturasCant2();
        this.loadfactsGpedByCli2();
        // this.player.src = this.song.src;
        // this.player.play();
      });
      // End pusher subscribe
    },

    toggleLoading() {
      this.cargando = !this.cargando;
    },

    formatNumerInteger(value: number, decimal: boolean) {
      if (decimal == true) {
        return numeral(value).format("0");
      } else {
        return numeral(value).format("0");
      }
    },

    formatNumber(value: number, decimal: boolean) {
      if (decimal == true) {
        return numeral(value).format("0,0.00");
      } else {
        return numeral(value).format("0,0");
      }
    },

    formatNumberPcto(value: number, decimal: boolean) {
      if (decimal == true) {
        return numeral(value).format("0,0.00");
      } else {
        return numeral(value).format("0,0.00");
      }
    },

    async defineurlAnalDats() {
      try {
        const res = await getUrl2("ELDER_REPORTE_DATA_DASHBOARD_ID");
        this.capurlAnalDats = res.data;
        this.myEmbedVisualAnalDats();
      } catch (error) {
        console.log(error);
      }
    },

    async defineurlAuxConvoc() {
      try {
        const res = await getUrl2("ELDER_CIERRE_DIARIO_AUTO_DASHBOARD_ID");
        this.capurlAuxConvoc = res.data;
        this.myEmbedVisualAuxConvoc();
      } catch (error) {
        console.log(error);
      }
    },

    async defineurl() {
      try {
        const res = await getUrl2("ELDER_MTRZ_GEN_AUTO_DASHBOARD_ID");
        this.capurl = res.data;
        this.myEmbedVisual();
      } catch (error) {
        console.log(error);
      }
    },

    myEmbedVisual() {
      const containerDiv = document.getElementById("embeddingContainer");
      const options = {
        url: this.capurl,
        container: containerDiv,
        height: "800px",
      };

      const embeddedDashboardExperience = embedDashboard(options);
      // let embeddedVisualExperience;
      // embeddedVisualExperience = QuickSightEmbedding.embedDashboard(options);

      // embeddedVisualExperience.on("error", onerror);
      embeddedDashboardExperience.on("load", embedVisual);
    },

    myEmbedVisualAnalDats() {
      const containerDiv = document.getElementById(
        "embeddingContainerAnalDats"
      );
      const options = {
        url: this.capurlAnalDats,
        container: containerDiv,
        height: "800px",
      };

      const embeddedDashboardExperience = embedDashboard(options);
      // let embeddedVisualExperience;
      // embeddedVisualExperience = QuickSightEmbedding.embedDashboard(options);

      // embeddedVisualExperience.on("error", onerror);
      embeddedDashboardExperience.on("load", embedVisual);
    },

    myEmbedVisualAuxConvoc() {
      const containerDiv = document.getElementById(
        "embeddingContainerAuxConvoc"
      );
      const options = {
        url: this.capurlAuxConvoc,
        container: containerDiv,
        height: "800px",
      };

      const embeddedDashboardExperience = embedDashboard(options);
      // let embeddedVisualExperience;
      // embeddedVisualExperience = QuickSightEmbedding.embedDashboard(options);

      // embeddedVisualExperience.on("error", onerror);
      embeddedDashboardExperience.on("load", embedVisual);
    },
  },

  mounted() {
    if (this.$store.state.user.type == "Encargada de Facturación") {
      this.defineurl();
    }
    if (this.$store.state.user.type == "Auxiliar de Convocatoria") {
      this.defineurlAuxConvoc();
    }
    if (this.$store.state.user.type == "Analista de Datos") {
      this.defineurlAnalDats();
    }
  },
};
</script>

<style lang="css" scoped>
.bold {
  font-weight: bold;
}

.bg-secondary {
  background-color: white;
}

.der {
  text-align: right;
}

.red {
  color: red;
}

.green {
  color: green;
}

/* Start Tabla */
#customers {
  font-family: Arial, Helvetica, sans-serif;
  border-collapse: collapse;
  width: 100%;
}

#customers td {
  border: 1px solid #ddd;
  padding: 3px;
  /* cursor: pointer; */
}

#customers th {
  border: 1px solid #ddd;
  padding: 3px;
}

#customers tr:nth-child(even) {
  background-color: #f2f2f2;
}

#customers tr:hover {
  background-color: #ddd;
}

#customers th {
  padding-top: 8px;
  padding-bottom: 8px;
  text-align: center;
  background-color: rgb(82, 45, 109);
  color: white;
}

td,
th {
  font-size: 75%;
}

/* End Tabla */

/* Start Transition */
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
/* End Transition */

.valor1 {
  text-align: left;
  /* background-color: rgb(255, 0, 0); */
  margin: 1px;
  font-weight: bold;
  color: rgb(255, 0, 0);
}

.valor2 {
  text-align: left;
  /* background-color: rgb(255, 64, 0); */
  margin: 1px;
  font-weight: bold;
  color: rgb(255, 64, 0);
}

.valor3 {
  text-align: left;
  /* background-color: rgb(255, 128, 0); */
  margin: 1px;
  font-weight: bold;
  color: rgb(255, 128, 0);
}

.valor4 {
  text-align: left;
  /* background-color: rgb(255, 192, 0); */
  margin: 1px;
  font-weight: bold;
  color: rgb(255, 192, 0);
}

.valor5 {
  text-align: left;
  /* background-color: rgb(171, 187, 26); */
  margin: 1px;
  font-weight: bold;
  color: rgb(171, 187, 26);
}

.valor6 {
  text-align: left;
  /* background-color: rgb(86, 182, 53); */
  margin: 1px;
  font-weight: bold;
  color: rgb(86, 182, 53);
}

.valor7 {
  text-align: left;
  /* background-color: rgb(0, 176, 80); */
  margin: 1px;
  font-weight: bold;
  color: rgb(0, 176, 80);
}

.ta-r {
  text-align: right;
}
/* Tabla */
#customers {
  font-family: Arial, Helvetica, sans-serif;
  border-collapse: collapse;
  width: 100%;
}

#customers td,
#customers th {
  border: 1px solid #ddd;
  padding: 3px;
  /* cursor: pointer; */
}

#customers tr:nth-child(even) {
  background-color: #f2f2f2;
}

#customers tr:hover {
  background-color: #ddd;
}

.navbar-option:hover {
  color: rgb(160, 57, 149);
  font-size: 16px;
  font-weight: bold;
}

#customers th {
  padding-top: 8px;
  padding-bottom: 8px;
  text-align: center;
  background-color: rgb(82, 45, 109);
  color: white;
}

td,
th {
  font-size: 75%;
}

p {
  font-size: 75%;
  margin: 0;
}
/* -------------------------------Structure... -------------------------------*/
h4 {
  text-align: center;
}

/* * {
  margin: 0;
} */

.general {
  width: 100%;
  max-width: 1250px;
  margin: 0px auto;
  padding-top: 45px;
  /* background-color: rgb(242, 243, 243); */
}

.grid-small2 {
  display: grid;
  grid-auto-flow: dense;
  grid-template-rows: auto auto;
  gap: 4px;
  grid-template-columns: repeat(auto-fit, minmax(10rem, 1fr));
}
.grid-small {
  display: grid;
  grid-auto-flow: dense;
  grid-template-rows: auto auto;
  gap: 4px;
  grid-template-columns: repeat(auto-fit, minmax(10rem, 1fr));
}

.grid {
  display: grid;
  grid-auto-flow: dense;
  grid-template-rows: auto auto;
  gap: 3px;
  grid-template-columns: repeat(auto-fill, minmax(12rem, 1fr));
}

.navbar-option {
  margin: 7px;
  font-size: 15px;
  /* color: white; */
  /* font-family: "Agency FB Bold"; */
  text-decoration: none;
  margin-right: 20px;
}

.grid-2 {
  display: grid;
  grid-auto-flow: dense;
  grid-template-rows: auto auto;
  gap: 3px;
  grid-template-columns: repeat(auto-fit, minmax(40rem, 1fr));
}
/* -------------------------------**********-------------------------------*/
/* -------------------------------Loading... -------------------------------*/

@keyframes spinner {
  0% {
    transform: translate3d(-50%, -50%, 0) rotate(0deg);
  }
  100% {
    transform: translate3d(-50%, -50%, 0) rotate(360deg);
  }
}
.spin::before {
  animation: 1.5s linear infinite spinner;
  animation-play-state: inherit;
  border: solid 5px #cfd0d1;
  border-bottom-color: rgb(160, 57, 149);
  border-radius: 50%;
  content: "";
  height: 70px;
  width: 70px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate3d(-50%, -50%, 0);
  will-change: transform;
}

.img {
  pointer-events: none;
  width: 55px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.imgAfil {
  pointer-events: none;
  width: 150px;
}

.title {
  color: red;
}

.backgrnd {
  background-color: rgb(242, 243, 243);
}
/* -------------------------------**********-------------------------------*/

.card-body {
  /* overflow-x: scroll; */
  margin-top: 10px;
}

.graph {
  overflow-x: scroll;
}
/* graph */
.quiz-chartTip {
  padding: 5px 10px;
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  background-color: rgba(255, 255, 255, 0.9);
  box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.1);
  position: absolute;
  z-index: 50;
  max-width: 250px;
}

.quiz-graph {
  padding: 10px;
  height: 370px;
  width: 100%;
}

.quiz-graph .x-labels {
  text-anchor: middle;
}

.quiz-graph .y-labels {
  text-anchor: end;
}

.quiz-graph .quiz-graph-grid {
  stroke: #ccc;
  stroke-dasharray: 0;
  stroke-width: 1;
}

.label-title {
  text-anchor: middle;
  text-transform: uppercase;
  font-size: 12px;
  fill: gray;
}

.quiz-graph-dot,
.quiz-graph-start-dot {
  fill: rgba(160, 57, 149, 1);
  stroke-width: 2;
  stroke: white;
}
</style>
