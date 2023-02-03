<script>
	import Form from './form.svelte';
	import NavigationBar from './navigationBar.svelte';
  import UserManagement from "./../userManagement.svelte";
  import TableComponent from './tableComponent.svelte';
  
  

  let isClicked=false;

  const addUser =()=>{
    isClicked=true;
  }

</script>

<div class="container-fluid">
<nav class="navbar navbar-expand-lg navbar-light bg-primary">
  <span class="navbar-brand1">
    <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAACXBIWXMAAAsTAAALEwEAmpwYAAABtklEQVR4nO2ZPShFYRjHf5dEsriSrAwWGViUkiQMRh8Li7JZZVDko5QySBYGCzIZZRZyDcrHjUSxiluyuK7u0VvnLqeLc895OM/N+dV/fHuf3zmn932f80JISEhQ1ABDwBywAiwBE0ALECEP6ASOAeubHABRFDMPpH+QyOQBWAUaUMaoSwFn3oFhlFAOvHgUMUkB9Shg0IdEJmsoYFNA5BoFxAREPoDioEVuBERMyoIWuRUSKQ1a5EhAwqx6gbMjIHKKAqYFRJZRQI+ASC8KaBQQaUIBewIiuyjgUkDkAgVsCYhsoICOHPqQbDFj21FCtw+RLpRx50HCHG/UsehBxIxRRy2QzLEzrEMps/n+NjJEXO4r90Ahyom5EImTB5y4ELkiD4i7/EGnmiLg0YXIK1CCYqZyWLUWUEgUWPdw5jL/xCpRQBUw6fJz+ipPwAxQHYRAq/0033wIOJMEtoG2375DKbB76zPB4r/KOdBvzylK8x8JWFmEzNwijNgHPCugpOwafDHgs/uTShro83OB86xAwrKTACq8iIwrKN5yZMyLyKGCwi1H9r2IJBQUbmXZPENCQv4rn6Ej5y2yxDtPAAAAAElFTkSuQmCC" width="50" height="50" class="d-inline-block align-top" alt="">
    User Management
  </span>
  <div class="container">
    <span class="navbar-brand" on:click={addUser}>Add User</span>
  </div>
</nav>
</div>
{#if isClicked===true}
<Form/>
{:else}
<TableComponent />
{/if}

<style>
 
  .container-fluid{
    margin: 0px;
    padding: 0px;
  }
 
 .navbar-brand1{
  margin-top: 20px;
  font-size: 26px;
  font-weight: bold;
  color: white;
 }

 .navbar-brand{
    cursor: pointer;
    text-align: right;
    text-align: center;
    margin-left: 90%;
    color: white;
    font-size: 24px;
    border-radius: 10px;
 }

 

</style>
