<div class="input-container" style="--value-percent: {percent}%">
    <div class="range-wrapper">
        <span class="range-value">{value}</span>
        <input
                type="range"
                class="input-range"
                min="0"
                max="100"
                bind:value
        />
    </div>
</div>

<script>
    let value = 33;
    let percent = 33;

    $: {
        percent = (value / 100) * 100;
    }
</script>

<style>
    .input-container {
        width: 200px;
        padding: 1em;
        border-radius: 8px;
        background-color: var(--first-color-dark);
        display: flex;
        flex-direction: column;
        gap: 0.6em;
    }

    .range-wrapper {
        position: relative;
        width: 100%;
        margin: 30px 0 10px;
    }

    .input-range {
        -webkit-appearance: none;
        appearance: none;
        width: 100%;
        height: 12px;
        background: transparent;
        border-radius: 6px;
        outline: none;
        padding: 0;
        margin: 0;
        position: relative;
    }

    /* Track styling */
    .input-range::before,
    .input-range::after {
        content: '';
        position: absolute;
        top: 50%;
        height: 18px;
        transform: translateY(-50%);
        z-index: 1;
        box-sizing: border-box;
    }

    .input-range::before {
        left: 0;
        width: calc(var(--value-percent, 25%));
        background-color: var(--third-color-dark);
        border-radius: 19px 0 0 19px;
        /* Remove separate border to fix edge cases */
        border: none;
    }

    .input-range::after {
        left: calc(var(--value-percent, 25%));
        right: 0;
        background-color: white;
        border-radius: 0 19px 19px 0;
        /* Use box-shadow instead of border to prevent sizing issues */
        box-shadow: inset 0 0 0 3px var(--third-color-dark);
    }

    .range-value {
        position: absolute;
        top: -30px; /* Moved further up */
        left: calc(var(--value-percent, 25%));
        transform: translateX(-50%);
        color: var(--font-color-dark);
        font-size: 18px;
        pointer-events: none;
        /* Add background to ensure text is always visible */
        background-color: var(--first-color-dark);
        padding: 2px 6px;
        border-radius: 4px;
    }

    /* Thumb styling */
    .input-range::-webkit-slider-thumb {
        -webkit-appearance: none;
        appearance: none;
        width: 28px;
        height: 28px;
        background-color: var(--font-color-dark);
        border: 4px solid var(--third-color-dark);
        border-radius: 50%;
        cursor: pointer;
        position: relative;
        z-index: 2;
    }

    .input-range::-moz-range-thumb {
        width: 28px;
        height: 28px;
        background-color: var(--font-color-dark);
        border: 4px solid var(--third-color-dark);
        border-radius: 50%;
        cursor: pointer;
        position: relative;
        z-index: 2;
    }
</style>