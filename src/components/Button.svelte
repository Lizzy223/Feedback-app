<script>
    export let style = 'primary'
    export let type = 'button'
    export let disabled = false
</script>

        <button {type} {disabled} class={style} >
            <slot></slot>
        </button>
   
<style>
    button{
        color: #fff;
        border: 0;
        border-radius: 8px;
        width: 5rem;
        height: 2.2rem;
        cursor: pointer;
    }

    .primary{
        background: #202142;
    }

    .secondary{
        background-color: #ff6a95;
    }

    button:hover{
        transform: scale(0.98);
        opacity: 0.9;
    }

    button:disabled{
        background-color: #ccc;

    }

</style>