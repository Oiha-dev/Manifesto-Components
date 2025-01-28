<div class="component">
    <div class="input-container">
        {#each inputs as input}
            <input
                    type={input.type}
                    placeholder={input.placeholder}
                    class={input.class}
            />
        {/each}
    </div>
</div>

<script>
    const inputs = [
        { type: "text", placeholder: "Enter your text here", class: "input-text" },
        { type: "search", placeholder: "Search...", class: "input-search" },
        { type: "email", placeholder: "Enter your email", class: "input-email" },
        { type: "password", placeholder: "Enter your password", class: "input-password" },
        { type: "tel", placeholder: "Enter your phone number", class: "input-tel" },
        { type: "number", placeholder: "Enter a number", class: "input-number" },
        { type: "url", placeholder: "Enter a URL", class: "input-url" }
    ];
</script>

<style>
    .input-container {
        padding: 1em;
        border-radius: 8px;
        background-color: var(--first-color-dark);
        display: flex;
        flex-direction: column;
        gap: 0.6em;
    }

    input {
        padding: 10px 20px;
        border-radius: 19px;
        font-size: 16px;
        border: none;
        background-color: var(--third-color-dark);
        border-bottom: 4px solid var(--bg-color-dark);
        color: white;
        width: 100%;
        box-sizing: border-box;
    }

    ::placeholder {
        color: white;
        font-style: italic;
    }

    .input-search {
        background-image: url("/icons/SearchIcon.svg");
        background-position: right 10px center;
        background-repeat: no-repeat;
        background-size: 20px 20px;
    }
</style>