<h1>Login Page</h1>
<script>
  let login = [];
   
  
  let formData = {
    email: '',
    password: ''
  };

  
  function handleSubmit(event) {
    event.preventDefault();

    formData = {
      email: '',
      password: ''
    };
  }
  function handleClick() {
    window.location.href = '/Menuitems';
  }
</script>


<form on:submit={handleSubmit}>
  <label>
    Email:
    <input type="email" bind:value={formData.email} required />
  </label>
  <br />
  <label>
    Password:
    <input type="password" bind:value={formData.password} required />
  </label>
  <br />
  <button on:click={handleClick}>Login</button>


</form>

