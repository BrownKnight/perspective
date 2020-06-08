<template>
    <svg id="main" viewBox="0 0 500 500" width="1000" height="1000"></svg>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import * as d3 from "d3";

@Component
export default class Flag extends Vue {
    private msg!: string;

    private svg!: d3.Selection<d3.BaseType, unknown, HTMLElement, any>;

    mounted() {
        this.svg = d3.select("svg");
        console.log("blah");

        this.svg
            .append("rect")
            .attr("x", 100)
            .attr("y", 100)
            .attr("width", 100)
            .attr("height", 100)
            .style("fill", "blue");
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
// #main {
//     width: 50%;
//     height: auto;
// }
</style>
