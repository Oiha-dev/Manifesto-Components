<div class="component buttons">
    <div class="button-container">
        <button class="btn btn-primary">Primary Button</button>
        <button class="btn btn-secondary">Secondary Button</button>
    </div>
</div>

<style>
    .buttons {
        height: 146px;
    }

    .button-container {
        padding: 1em;
        border-radius: 8px;
        background-color: var(--first-color-dark);
        display: flex;
        flex-direction: column;
        gap: 0.6em;
    }

    .btn {
        padding: 20px 20px;
        border-radius: 19px;
        font-size: 20px;
        cursor: pointer;
        text-align: center;
        border: none;
    }

    .btn-primary {
        background-color: var(--third-color-dark);
        color: white;
    }

    .btn-primary:hover {
        background-color: var(--second-color-dark);
    }

    .btn-secondary {
        background-color: transparent;
        color: var(--font-color-dark);
        border: 2px solid var(--third-color-dark);
    }

    .btn-secondary:hover {
        background-color: var(--bg-color-dark);
        color: white;
    }
</style>