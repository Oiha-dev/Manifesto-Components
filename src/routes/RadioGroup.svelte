<div class="component">
    <div class="radio-container">
        {#each options as option}
            <label>
                <input
                        type="radio"
                        name="Option"
                        value={option.value}
                        bind:group={selected}
                />
                <span>{option.label}</span>
            </label>
        {/each}
    </div>
</div>

<script>
    let selected = "";
    const options = [
        { value: "1", label: "Radio 1" },
        { value: "2", label: "Radio 2" },
        { value: "3", label: "Radio 3" },
    ];
</script>

<style>

    label {
        display: flex;
        align-items: center;
        gap: 0.5em;
    }

    .radio-container {
        padding: 1em;
        border-radius: 8px;
        background-color: var(--first-color-dark);
        display: flex;
        flex-direction: column;
        gap: 0.6em;
    }

    input[type="radio"] {
        appearance: none;
        -webkit-appearance: none;
        width: 24px;
        height: 24px;
        border: 2px solid var(--font-color-dark);
        background-color: var(--bg-color-dark);
        border-radius: 50%;
        cursor: pointer;
        margin-right: 10px;
        position: relative;
    }

    input[type="radio"]:checked::before {
        content: "";
        position: absolute;
        top: 4px;
        left: 4px;
        width: 12px;
        height: 12px;
        background-color: white;
        border-radius: 50%;
    }
</style>