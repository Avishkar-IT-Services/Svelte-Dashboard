<script>
    import { PolarArea } from "svelte-chartjs";
    import { data } from "./polarData.js";

    import {
        Chart as ChartJS,
        Title,
        Tooltip,
        Legend,
        ArcElement,
        RadialLinearScale,
    } from "chart.js";

    ChartJS.register(Title, Tooltip, Legend, ArcElement, RadialLinearScale);
</script>

<PolarArea {data} options={{ responsive: true }} />
