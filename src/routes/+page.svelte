<main>
    <div class="grid-container">
        <CheckboxGroup />
        <RadioGroup />
        <ButtonGroup />
        <InputGroup />
        <RangeInput />
        <Select />
        <ToggleSwitch />
    </div>
</main>

<script>
    import CheckboxGroup from './CheckboxGroup.svelte';
    import RadioGroup from './RadioGroup.svelte';
    import ButtonGroup from './ButtonGroup.svelte';
    import InputGroup from './InputGroup.svelte';
    import RangeInput from './RangeInput.svelte';
    import Select from './Select.svelte';
    import ToggleSwitch from './ToggleSwitch.svelte';
</script>

<style global>
    @import './global.css';

    .grid-container {
        background: var(--first-color-dark);
        border-radius: 16px;
        height: 80vh;
        width: 80vw;
        display: grid;
        place-items: center;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 1em;
    }

</style>