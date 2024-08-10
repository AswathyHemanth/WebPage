<h1> Select the Menuitemss</h1>
<script>
    let message='';
    // Array to track multiple checkboxes
    let selectedOptions = {
      option1: false,
      option2: false,
      option3: false
    };
  
    function handleChange(event) {
      selectedOptions[event.target.value] = event.target.checked;
    }
    
    function Smessage() {
        message = 'Your request has been recorded, Will contact you shortly';
    }
  </script>
  
  <label>
    <input
      type="checkbox"
      value="option1"
      bind:checked={selectedOptions.option1}
      on:change={handleChange}
    />
    Vegetarian
  </label>
  
  <label>
    <input
      type="checkbox"
      value="option2"
      bind:checked={selectedOptions.option2}
      on:change={handleChange}
    />
    Non Vegetarian
  </label>
  
  <label>
    <input
      type="checkbox"
      value="option3"
      bind:checked={selectedOptions.option3}
      on:change={handleChange}
    />
    Mixed 
  </label>
  
  <button on:click={Smessage}>Submit</button>
  {#if message} <p>{message}</p> {/if}
