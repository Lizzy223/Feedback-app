<script>
    import {createEventDispatcher} from "svelte"
    import Card from './Card.svelte'
    export let item

    const dispatch = createEventDispatcher()

    const handleDelete = (itemId) =>{
        dispatch('delete', itemId)
    }
</script>

<Card>
    <div class="num-display">
        {item.rating}
    </div>
    <button class="close"  on:click={() => handleDelete(item.id)} >X</button>
    <p class="text-display">
        {item.text}
    </p>
</Card>

<style>
    .num-display{
        position: relative;
        top:-.75rem;
        left: -.75rem;
        width: 3.5rem;
        height: 3.5rem;
        background-color: #ff6a95;
        color:#fff;
        border:1px #eee solid;
        border-radius: 50%;
        padding: .75rem;
        text-align: center;
        font-size: 1.2em;
    }

    .close{
        position: absolute;
        top: .75rem;
        right: 1.4rem;
        cursor: pointer;
        background: none;
        border: none;
    }
</style>