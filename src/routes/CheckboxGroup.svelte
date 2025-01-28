<div class="component">
    <div class="checkbox-container">
        {#each checkboxes as checkbox}
            <label>
                <input
                        type="checkbox"
                        name={checkbox.name}
                        bind:checked={checkbox.checked}
                />
                <span>{checkbox.label}</span>
            </label>
        {/each}
    </div>
</div>

<script>
    let checkboxes = [
        { name: "Test1", label: "Checkbox 1", checked: false },
        { name: "Test2", label: "Checkbox 2", checked: false },
        { name: "Test3", label: "Checkbox 3", checked: false }
    ];
</script>

<style>
    .checkbox-container {
        padding: 1em;
        border-radius: 8px;
        background-color: var(--first-color-dark);
        display: flex;
        flex-direction: column;
        gap: 0.6em;
    }

    label {
        display: flex;
        align-items: center;
        cursor: pointer;
        font-size: 18px;
    }

    input[type="checkbox"] {
        appearance: none;
        -webkit-appearance: none;
        width: 24px;
        height: 24px;
        border: 2px solid var(--font-color-dark);
        background-color: transparent;
        cursor: pointer;
        margin-right: 10px;
        position: relative;
    }

    input[type="checkbox"]:checked {
        background-color: var(--third-color-dark);
        background-image: url("/icons/CheckMark.svg");
        background-repeat: no-repeat;
        background-position: center;
        background-size: 14px 14px;
    }

    span {
        color: var(--font-color-dark);
    }
</style>