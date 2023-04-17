<script>
    let inputVal = '';
  
    function handleClick() {
      console.log('Button clicked');
    }
  
    function handleInput() {
      const button = document.getElementById('myButton');
      button.click();
    }
  </script>
  
  <label>
    Enter a value:
    <input type="text" bind:value={inputVal} on:input={handleInput} />
  </label>
  <br />
  
  <button id="myButton" on:click={handleClick}>Click me</button>
  