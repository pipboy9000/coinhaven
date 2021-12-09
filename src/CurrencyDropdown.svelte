<script>
    import { Btc, Usd } from "svelte-cryptoicon";
    import FaAngleDown from "svelte-icons/fa/FaAngleDown.svelte";

    let isOpen = false;

    let currrencies = [
        {
            name: "BTC",
            icon: Btc,
        },
        {
            name: "USD",
            icon: Usd,
        },
    ];

    let selected = currrencies[0];
</script>

<div
    class="selected"
    on:click={() => {
        isOpen = !isOpen;
    }}
    on:focusout={() => {
        isOpen = false;
    }}
>
    <div class="icon">
        <svelte:component this={selected.icon} size="24" />
    </div>
    <p>{selected.name}</p>
    <div class="downArrow">
        <FaAngleDown />
    </div>
</div>

{#if isOpen}
    <div class="currencies">
        {#each currrencies as currency}
            <div
                class="currency"
                on:click={() => {
                    isOpen = false;
                    selected = currency;
                }}
            >
                <div class="icon">
                    <svelte:component this={currency.icon} size="24" />
                </div>
                <p>{currency.name}</p>
            </div>
        {/each}
    </div>
{/if}

<style>
    .selected {
        height: 44px;
        background: #f4f5f6;
        border-radius: 4px;
        border: none;
        width: 200px;
        padding-left: 24px;
        display: flex;
        align-items: center;
        position: relative;
    }

    .currencies {
        margin-top: 20px;
        box-shadow: 0 5px 25px -22px;
        position: absolute;
        z-index: 9;
    }

    .currency {
        height: 44px;
        background: #fff;
        border-radius: 4px;
        border: none;
        width: 200px;
        padding-left: 24px;
        display: flex;
        align-items: center;
        position: relative;
        cursor: pointer;
    }

    .currency:hover {
        background: #f4f5f6;
    }

    .icon {
        margin-right: 16px;
        display: flex;
    }

    .downArrow {
        width: 10px;
        position: absolute;
        color: #abacc1;
        right: 0;
        margin-right: 14px;
    }
</style>
