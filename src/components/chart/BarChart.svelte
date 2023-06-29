<script>
    import { Bar } from "svelte-chartjs";
    import { barData as data } from "./barData.js";
    import { Card } from "flowbite-svelte";
    import {
        Chart,
        Title,
        Tooltip,
        Legend,
        BarElement,
        CategoryScale,
        LinearScale,
    } from "chart.js";

    Chart.register(
        Title,
        Tooltip,
        Legend,
        BarElement,
        CategoryScale,
        LinearScale
    );
</script>

<!-- <Card size="lg"> -->
<Bar {data} options={{ responsive: true }} style="height:20vh; width:39vw" />
<!-- </Card> -->
