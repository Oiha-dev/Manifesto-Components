<div class="component">
    <div class="switch-container">
        <label>
            <input
                    type="checkbox"
                    bind:checked
            />
            <span>{checked ? 'ON' : 'OFF'}</span>
        </label>
    </div>
</div>

<script>
    export let checked = false;
</script>

<style>
    .switch-container {
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
        width: 42px;
        height: 24px;
        border: 2px solid var(--font-color-dark);
        background-color: transparent;
        cursor: pointer;
        margin-right: 10px;
        position: relative;
        border-radius: 12px;
    }

    input[type="checkbox"]:checked {
        background-color: var(--third-color-dark);
    }

    input[type="checkbox"]::before {
        content: "";
        position: absolute;
        width: 20px;
        height: 20px;
        background-color: var(--first-color-dark);
        border: 2px solid var(--font-color-dark);
        border-radius: 50%;
        top: -2px;
        left: -2px;
        transition: transform 0.1s;
    }

    input[type="checkbox"]:checked::before {
        transform: translateX(18px);

    }

    span {
        color: var(--font-color-dark);
        min-width: 32px;
    }
</style>