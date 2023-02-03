<script>
   let fname=''
   let lname=''


</script>



<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-GLhlTQ8iRABdZLl6O3oVMWSktQOp6b7In1Zl3/Jr59b6EGGoI1aFkw7cmDA6j6gD" crossorigin="anonymous">
<div class="container-xl">
<h1>Registration</h1><br>
<label for="Name">First Name</label>
<input type="text" bind:value={fname} ><br><br>
<label for="Name">Last Name</label>
<input type="text" bind:value={lname} ><br><br>

{#if fname!='' && lname!=''}
<button type="button" class="btn btn-outline-success btn-lg">Submit</button>
    <h1>{fname} {lname}</h1>
{/if}

</div>

