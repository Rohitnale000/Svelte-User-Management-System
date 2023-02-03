<script>
import { onMount } from "svelte";


let getDataArray=[];
onMount( () => {
     fetch(`http://localhost:3000/api/user`)
      .then(r => r.json())
      .then(data =>  getDataArray = data);
  })
  
 
  
</script>


<div class="row">
    <table class="table table-striped w-lg" style="border: 2px;" id="dtBasicExample">
      <thead>
        <tr>
          <th scope="col">ID</th>
          <th scope="col">First</th>
          <th scope="col">Middle</th>
          <th scope="col">Last</th>
          <th scope="col">Email</th>
          <th scope="col">Gender</th>
          <th scope="col">Birth Date</th>
          <th scope="col">Address</th>
          <th scope="col">Action</th>
        </tr>
      </thead>
      <tbody>
        {#each getDataArray as item }
        <tr>
          <td>{item.id}</td>
          <td>{item.firstName}</td>
          <td>{item.middleName}</td>
          <td>{item.lastName}</td>
          <td>{item.email}</td>
          <td>{item.gender}</td>
          <td>{item.address}</td>
          <td>{item.dateOfBirth}</td>
          <td>
            <button type="button" class="btn btn-outline-success">Update</button>
            <button type="button" class="btn btn-outline-danger">Delete</button>
          </td>
        </tr>
        {/each}
       
      </tbody>
    </table>
  </div>
  

  <style>

#myTable{
    font-size: 20px;
  }

.row{
  text-align: center;
}

  </style>