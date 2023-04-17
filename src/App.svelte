<script>

    let text;
    let email;
    let isDisplay=false;
    function handleInput(){
        isDisplay=false;
    }
    function display(){
    if(text&&email){
        console.log('Name:', text);
            console.log('Email:', email);
            isDisplay = true;
    }
    }
</script>
<style>
h1{
    text-align:center;
	font-family:'Rubik', sans-serif;
}
.Container {
    display: flex;
    justify-content: center;
    align-items: center;
    height:70vh;
  }
  form {
    background-color: white;
    width: 400px;
    border-radius: 8px;
    padding: 20px 40px;
    box-shadow: 0 10px 25px rgba(92, 99, 105, 0.2);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
label{
	font-size:18px;
	font-family:'Rubik', sans-serif;
	font-weight: bold;
}
input{
    color:#432000;
    background-color:#DCE1EB;
    text-align:center;
    border-radius:8px;
    padding:15px;
    border:0;
    font-size:20px;
    font-family:'Rubik', sans-serif;
    margin:10px 0;
}
button{
	color:#FDFDFD;
    background-color:#AC485A;
    text-align:center;
    border-radius:8px;
    padding:15px;
    border:0;
    font-size:20px;
    font-family:'Rubik', sans-serif
}
</style>
<h1>Login</h1>
<div class="Container">
<form>
    <label for="name">Enter your Name:</label><br/>
    <input type="text" bind:value={text} on:input={handleInput}/><br/>
    <label for="name">Enter your Email id:</label><br/>
    <input type="email" bind:value={email} on:input={handleInput}/><br/>
	<button type="button" on:click={display}>Login</button>
    {#if isDisplay}
    <h1>Hello {text}! and You logged in as {email}</h1>     
    {/if}
</form>
</div>

