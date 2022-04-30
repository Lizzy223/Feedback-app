<script>
    let selected = 10

    const onChange = () =>{
        console.log('')
    }
</script>

<ul class='rating'>
    <li>
        <input type="radio" name="rating" value="1" id="num1" on:change={onChange} checked={selected ==1} />
        <label for="num1" >1</label>
    </li>
    <li>
        <input type="radio" name="rating" value="2" id="num2" on:change={onChange} checked={selected ==2} />
        <label for="num2" >2</label>
    </li>
    <li>
        <input type="radio" name="rating" value="3" id="num3" on:change={onChange} checked={selected ==3} />
        <label for="num3" >3</label>
    </li>
    <li>
        <input type="radio" name="rating" value="4" id="num4" on:change={onChange} checked={selected ==4} />
        <label for="num4" >4</label>
    </li>
    <li>
        <input type="radio" name="rating" value="5" id="num5" on:change={onChange} checked={selected ==5} />
        <label for="num5" >5</label>
    </li>
    <li>
        <input type="radio" name="rating" value="6" id="num6" on:change={onChange} checked={selected ==6} />
        <label for="num6" >6</label>
    </li>
    <li>
        <input type="radio" name="rating" value="7" id="num7" on:change={onChange} checked={selected ==7} />
        <label for="num7" >7</label>
    </li>
    <li>
        <input type="radio" name="rating" value="8" id="num8" on:change={onChange} checked={selected ==8} />
        <label for="num8" >8</label>
    </li>
    <li>
        <input type="radio" name="rating" value="9" id="num9" on:change={onChange} checked={selected ==9} />
        <label for="num9" >9</label>
    </li>
    <li>
        <input type="radio" name="rating" value="10" id="num10" on:change={onChange} checked={selected ==10} />
        <label for="num10" >10</label>
    </li>
</ul>

<style>
    .rating{
        display: flex;
        align-items: center;
        justify-content: space-around;
        margin: 1.75rem 0;
    }

    .rating li {
        position: relative;
        background-color: #f4f4f4;
        width: 3rem;
        height: 3rem;
        padding: .7rem;
        text-align: center;
        border-radius: 50%;
        font-size: 1.1em;
        border: 1px solid #eee;
        transition: 0.3s;
}

.rating li label{
    position: absolute;
    top: 50%;
    left: 50%;
    width: 3rem;
    height: 3rem;
    padding: .7rem;
    border-radius: 50%;
    transform: translate(50%, -50%);
    cursor: pointer;
}

.rating li:hover{
    background-color: #ff6a95;
    color: #fff;
}

[type='radio']{
    opacity: 0;
}

[type='radio']:checked ~ label {
    background-color: #ff6a95;
    color: #fff;
}
</style>