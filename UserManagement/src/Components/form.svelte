<script>
	import TableComponent from './tableComponent.svelte';
  import NavigationBar from "./navigationBar.svelte";

  let firstName=''
  let middleName=''
  let lastName=''
  let email=''
  let password=''
  let gender=''
  let dateOfBirth=''
  let address='';

  let isClick=false;

  const doPost= ()=> {
    try {
      fetch('http://localhost:3000/api/user',{
      method:  'POST',
      headers: {
        'Content-Type': 'application/json',
        'Accept': 'application/json'
      },
      body: JSON.stringify({
      firstName:firstName,
      middleName:middleName,
      lastName: lastName,
      gender: gender,
      dateOfBirth:dateOfBirth,
      email: email,
      password: password,
      address: address,
      })
    })
      .then(response => response.json())
      .then(result => console.log(result))
      isClick=true
     
    } catch (error) {
      console.log(error);
    }
  }
 

</script>




<div class="container col-6">
    <div class="form-group">
        <label for="" class="allFormLebeal">First Name</label>
        <input bind:value={firstName} class="form-control form-control-lg" type="text" placeholder="Enter First Name">
      </div>
      <div class="form-group">
        <label for="" class="allFormLebeal">Middle Name</label>
        <input bind:value={middleName} class="form-control form-control-lg" type="text" placeholder="Enter Middle Name">
      </div>
      <div class="form-group">
        <label for="" class="allFormLebeal">Last Name</label>
        <input bind:value={lastName} class="form-control form-control-lg" type="text" placeholder="Enter Last Name">
      </div>
    <div class="form-group">
      <label for="" class="allFormLebeal">Email address</label>
      <input bind:value={email} type="email" class="form-control form-control-lg" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
      <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
    </div>
    <div class="form-group">
      <label for="" class="allFormLebeal">Password</label>
      <input bind:value={password} type="password" class="form-control form-control-lg" id="exampleInputPassword1" placeholder="Password">
    </div>
    <div class="form-group">
        <label for="" class="allFormLebeal">Select Gender</label>
        <select bind:value={gender} class="form-control form-control-lg" id="inputGroupSelect02">
          <option selected>Choose...</option>
          <option value="Male">Male</option>
          <option value="Female">Female</option>
          <option value="Other">Other</option>
        </select>
    </div>
    
    <div class="form-group">
        <label for="" class="allFormLebeal">Date</label>
        <input bind:value={dateOfBirth} type="date" class="form-control form-control-lg" name="" id="">
    </div>
    <div class="form-group">
        <label for="" class="allFormLebeal">Address</label>
        <input bind:value={address} class="form-control form-control-lg" type="text" placeholder="Enter full address">
      </div>
    <br>
    <button type="submit" class="btn btn-primary btn-lg" on:click={doPost}>Submit</button>
    
</div>



  <style>

  </style>