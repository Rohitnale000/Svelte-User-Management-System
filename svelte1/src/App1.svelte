<script>
   
  
    let  name ='Rohit'
      $:orignalName = name
      $:upperCase = name.toUpperCase();
      $:lowerCase = name.toLowerCase();
      $:lengthOfString =  name.length;
      function demo(){
      if(name==='Rohit'){
        name="Mohi"
      }else if(name==="Mohi") {
        name="Rohit"
      }
    }
  </script>
  
  
  <h1>name is in upperCase  {upperCase}</h1>
  <h1>name is in lowerCase  {lowerCase}</h1>
  <h1>name length is  {lengthOfString}</h1>
  <h1>orignal Name is  {orignalName}</h1>
  <button class="btn" on:click={demo}>Click Me</button>
  
  <style>
    .btn {
      cursor: pointer;
      color: white;
      background-color: black;
      box-sizing: border-box;
    }
    .btn:hover {
      color: black;
      background-color: white;
    }
  </style>
  