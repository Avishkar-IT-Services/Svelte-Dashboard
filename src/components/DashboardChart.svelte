<script>
    import BarCart from "./chart/BarChart.svelte";
    import Layout from "./Layout.svelte";
    import Doughnut from "./chart/Doughnut.svelte";
    import LineChart from "./chart/LineChart.svelte";
    import RadarChart from "./chart/RadarChart.svelte";
    import PolarArea from "./chart/PolarArea.svelte";
</script>

<Layout>
    <div class="chart__parent" slot="content">
        <div class="chat__child1">
            <div class="chat__child1--child1">
                <div>Ticket Status</div>
                <div><Doughnut /></div>
            </div>
            <div class="chat__child1--child1">
                <div>Ticket Issue Type</div>
                <div><Doughnut /></div>
            </div>
        </div>
        <div>
            <div>Average Response Time</div>
            <div>
                <BarCart />
            </div>
        </div>
        <div>
            <div>Average Selling</div>
            <div>
                <LineChart />
            </div>
        </div>
        <!-- TODO - change the class name and style -->
        <div class="chat__child1">
            <div class="chat__child1--child1">
                <div>Ticket Status</div>
                <div><RadarChart /></div>
            </div>
            <div class="chat__child1--child1">
                <div>Ticket Issue Type</div>
                <div><PolarArea /></div>
            </div>
        </div>
    </div>
</Layout>

<style>
    .chart__parent {
        width: 84.5vw;
        height: 84vh;
        overflow-y: scroll;
    }

    .chart__parent > div:nth-child(1) {
        display: flex;
        width: 100%;
        height: 60%;
    }
    .chart__parent > div:nth-child(2) {
        width: 99%;
        height: 60%;
        border: 1px solid rgb(216, 215, 215);
        margin-top: 1%;
        padding: 1%;
    }
    .chart__parent > div:nth-child(3) {
        width: 99%;
        height: 60%;
        border: 1px solid rgb(216, 215, 215);
        margin-top: 1%;
        /* margin-bottom: 5%; */
        padding: 1%;
    }

    .chart__parent > div:nth-child(4) {
        display: flex;
        width: 99%;
        height: 60%;
        margin-top: 1%;
    }

    .chat__child1 > div:nth-child(1) {
        width: 49%;
        border: 1px solid rgb(216, 215, 215);
        height: 100%;
        padding: 1%;
        margin: 0 1% 0 0;
    }

    .chat__child1 > div:nth-child(2) {
        width: 49%;
        border: 1px solid rgb(216, 215, 215);
        height: 100%;
        padding: 1%;
    }

    .chat__child1--child1 > div:nth-child(1) {
        width: 100%;
        height: 10%;
        margin: 0 1% 0 0;
    }
    .chat__child1--child1 > div:nth-child(2) {
        width: 100%;
        height: 90%;
        margin: 0 1% 0 0;
    }
</style>
