<script>
    import { Router, Link, Route } from "svelte-routing"
    import index from "./routes/index.svelte"
    import about from "./routes/about.svelte"
    import contact from "./routes/contact.svelte"

    export let url = ""
</script>

<Router url="{url}">
  <nav>
    <Link to="/">Index</Link>
    <Link to="about">About</Link>
    <Link to="contact">Contact</Link>
  </nav>
  <div>
    <Route path="/" component="{index}" />
    <Route path="/about" component="{about}" />
    <Route path="/contact" component="{contact}" />
    <Route path="/"><index /></Route>
  </div>
</Router>