<template>
  <div>
    <h1>Dashboard</h1>
    <v-row>
      <v-col v-for="(graph, index) in sales" :key="`${graph.title}-${index}`">
        <SalesGraph :sales="sales" />
      </v-col>
    </v-row>

    <v-row>
      <v-col v-for="statistic in statistics" :key="`${statistic.title}`">
        <StatisticCard :statistic="statistic" />
      </v-col>
    </v-row>
  </div>
</template>
<script>
import SalesGraph from "./component/SalesGraph.vue";

export default {
  name: "DashboardPage",
  components: {
    SalesGraph,
  },
  data() {
    return {};
  },
};
</script>
