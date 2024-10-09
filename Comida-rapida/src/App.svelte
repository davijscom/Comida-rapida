<!-- App.svelte -->
<script>
    import { Router, Route, Link } from "svelte-routing";
    import Home from "./Home.svelte";
    import Login from "./Routes/Login.svelte";
    import Register from "./Routes/Register.svelte";
    import Perfil from "./Routes/Perfil.svelte";
    import Administrador from "./Routes/Administrador.svelte";
    import Combos from "./Routes/Combos.svelte";

</script>

<Router>
    

    <Route path="/" component={Home} />
    <Route path="/login" component={Login}/>
    <Route path="/register" component={Register}/>
    <Route path="/perfil" component={Perfil}/>
    <Route path="/administrador" component={Administrador}/>
    <Route path="/combos" component={Combos}/>

</Router>