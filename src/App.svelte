<script>
  import NetworkGraphSvelteSVG from "./NetworkGraphSvelteSVG.svelte";

  import data from "./data.js";

  const graphList = [
    { name: "NetworkGraphSvelteSVG", component: NetworkGraphSvelteSVG },
  ];

  let currentGraph = graphList[0];
</script>

<div class="chart">
  <svelte:component this={currentGraph.component} graph={data} />
</div>

<style>
  .chart {
    width: 100%;
    height: calc(100% - 4em);
    min-height: 280px;
    max-height: 480px;
    margin: 0 auto;
  }
</style>
