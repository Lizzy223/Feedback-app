<script>
    import Button from "./Button.svelte"
    import RatingSelect from "./RatingSelect.svelte"

    let text = ''
    let rating = 10
    let btnDisabled =true
    let min =10
    let message 

    const handleInput = () =>{
        if(text.trim().length <= min){
            message = `Text must be at least ${min} characters`
            btnDisabled = true
        } else{
            message = null
            btnDisabled = false
        }
    }
</script>
<header>
    <h2>How would you rate your service with us?</h2>
</header>
<form>
    <RatingSelect/>
    <div class="input-group">
        <input type="text" on:input={handleInput} placeholder="Give us your comeback comment" >
        <Button disabled={btnDisabled} type="submit"> Send </Button>
    </div>
    {#if message}
    <div class="message">
        {message}
    </div>
    {/if}
</form>

<style>
      input{
        border: 1px solid #fff;
        background-color: transparent;
        color: #fff;
        padding: 1rem ;
        width: 50%;
        border-radius: 8px;
    }

    .input-group{
        display: flex;
        justify-content: space-between;
    }

    .message{
        color:red;
        font-style: italic;
    }
</style>