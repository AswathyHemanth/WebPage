<script>
  let register = [];

  
  let formData = {
    name: '',
    email: '',
    password: ''
  };

  
  function handleSubmit(event) {
    event.preventDefault();


  

    formData = {
      name: '',
      email: '',
      password: ''
    };
  }
</script>


<form on:submit={handleSubmit}>
  <label>
    Name:
    <input type="text" bind:value={formData.name} required />
  </label>
  <br />
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
  <button type="submit">Register</button>
</form>

<h2>Registered Users:</h2>
<ul>
  {#each register as register (register.email)}
    <li>{register.name} - {register.email}</li>
  {/each}
</ul>