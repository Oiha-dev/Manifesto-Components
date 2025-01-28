<div class="component">
    <div class="toggle-container">
        <label class="toggle-label">
            <input
                    type="checkbox"
                    bind:checked={isChecked}
                    class="toggle-input"
            />
            <span class="toggle-slider"></span>
            <span class="toggle-text">{isChecked ? 'On' : 'Off'}</span>
        </label>
    </div>
</div>

<script>
    let isChecked = false;
</script>

<style>
    .toggle-container {
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .toggle-label {
        display: flex;
        align-items: center;
        cursor: pointer;
    }

    .toggle-input {
        display: none;
    }

    .toggle-slider {
        position: relative;
        width: 60px;
        height: 30px;
        background-color: var(--third-color-dark);
        border: var(--font-color-dark) 2px solid;
        border-radius: 30px;
        transition: background-color 0.3s;
    }

    .toggle-slider::before {
        content: '';
        position: absolute;
        top: 1px;
        left: 3px;
        width: 24px;
        height: 24px;
        background-color: var();
        border: var(--font-color-dark) 2px solid;
        border-radius: 50%;
        transition: transform 0.3s;
    }

    .toggle-input:checked + .toggle-slider {
        background-color: var(--third-color-dark);
    }

    .toggle-input:checked + .toggle-slider::before {
        transform: translateX(30px);
    }

    .toggle-text {
        color: var(--font-color-dark);
        font-size: 18px;
        margin-left: 10px;
    }
</style>