<template>
  <canvas ref="barChart" id="myBarChart" width="400" height="400"></canvas>
</template>

<script>
export default {
  props: ["propsdata"],
  mounted() {
    // const ctx = document.getElementById("myBarChart");
    const ctx = this.$refs.barChart;
    const myBarChart = new this.$_Chart(ctx, {
      type: "bar",
      data: {
        labels: ["Red", "Blue", "Yellow", "Green", "Purple", "Orange"],
        datasets: this.propsdata,
      },
      options: {
        scales: {
          y: {
            beginAtZero: true,
          },
        },
      },
    });
    console.log(myBarChart);
  },
};
</script>

<style></style>
