<script>
    export let count
    export let average
</script>

<div class="feedback-stat">
    <h4>{count} Reviews </h4>
    <h4>Ratings Average: {average}</h4>
</div>

<style>
    .feedback-stat{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
</style>

