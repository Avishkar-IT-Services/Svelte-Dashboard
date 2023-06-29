<script>
  import { Router, Link, Route } from "svelte-routing";
  import "./app.postcss";
  import Header from "./components/Header.svelte";
  import Sidebar from "./components/Sidebar.svelte";
  import DashboardChart from "./components/DashboardChart.svelte";
  import Contact from "./components/Contact.svelte";
</script>

<Header />
<Sidebar />
<Router>
  <Route path="/" component={DashboardChart} />
  <Route path="/contact" component={Contact} />
</Router>

<style>
  @import "../global.css";
</style>
