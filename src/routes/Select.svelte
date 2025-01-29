<div class="component">
    <div class="select-container">
        <select bind:value={selectedValue} class="select-input">
            {#each options as option}
                <option value={option.value}>{option.label}</option>
            {/each}
        </select>
        <div class="select-arrow">▼</div>
    </div>
</div>

<script>
    export let options = [
        { value: "1", label: "Option 1" },
        { value: "2", label: "Option 2" },
        { value: "3", label: "Option 3" }
    ];

    let selectedValue = options[0].value;
</script>

<style>
    .component {
        padding: 1em;
        border-radius: 8px;
        background-color: var(--first-color-dark);
    }

    .select-container {
        position: relative;
        width: 100%;
    }

    .select-input {
        appearance: none;
        -webkit-appearance: none;
        width: 100%;
        padding: 10px 30px 10px 15px;
        border-radius: 19px;
        font-size: 16px;
        border: none;
        background-color: var(--third-color-dark);
        border-bottom: 4px solid var(--bg-color-dark);
        color: white;
        cursor: pointer;
    }

    .select-input:focus {
        outline: none;
    }

    .select-arrow {
        position: absolute;
        top: 50%;
        right: 15px;
        transform: translateY(-70%);
        pointer-events: none;
        color: var(--font-color-dark);
        font-size: 14px;
    }

    .select-input::placeholder {
        color: white;
        font-style: italic;
    }

    .select-input option {
        background-color: var(--first-color-dark);
        color: var(--font-color-dark);
    }
</style>