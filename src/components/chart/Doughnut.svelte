<script>
    import { Doughnut } from "svelte-chartjs";
    import { doughData } from "./doughData.js";
    import { Card } from "flowbite-svelte";
    let data = doughData;
    import {
        Chart as ChartJS,
        Title,
        Tooltip,
        Legend,
        ArcElement,
        CategoryScale,
    } from "chart.js";

    ChartJS.register(Title, Tooltip, Legend, ArcElement, CategoryScale);
</script>

<Doughnut {data} options={{ responsive: true }} />
