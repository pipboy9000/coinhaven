<script>
    import CurrencyDropdown from "./CurrencyDropdown.svelte";
    import Summary from "./Summary.svelte";

    let selected = "sell";
</script>

<main>
    <div class="headers">
        <div class="header" class:selected={selected == "buy"}>Buy</div>
        <div class="header" class:selected={selected == "sell"}>Sell</div>
        <div class="header" class:selected={selected == "convet"}>Convert</div>
    </div>
    <div class="content">
        {#if selected == "sell"}
            <div class="left">
                <div class="row">
                    <div>
                        <h2>Sell</h2>
                        <input type="number" />
                    </div>
                    <div>
                        <h2>Currency</h2>
                        <CurrencyDropdown />
                    </div>
                </div>
                <div class="row">
                    <div>
                        <h2>Get</h2>
                        <input type="number" />
                    </div>
                    <div>
                        <h2>Currency</h2>
                        <CurrencyDropdown />
                    </div>
                </div>
            </div>
        {/if}
        <div class="summary">
            <h2>Summary</h2>
            <Summary />
            <button class="sellBtn"> Sell </button>
        </div>
    </div>
</main>

<style>
    .sellBtn {
        display: flex;
        align-items: center;
        justify-content: center;
        margin-top: 38px;
        width: 270px;
        height: 65px;
        background: #4c56f6;
        font-size: 14px;
        font-weight: 700;
        color: #fff;
        border-radius: 5px;
        border: none;
        box-shadow: 0 10px 20px -15px #4c56f6;
        cursor: pointer;
    }
    .summary {
        padding-left: 16px;
    }
    .content {
        display: flex;
        padding-bottom: 36px;
    }
    .row {
        display: flex;
        gap: 30px;
    }

    main {
        background: #fff;
        box-shadow: 0 10px 25px -22px;
    }
    .headers {
        width: 100%;
        display: flex;
        align-items: center;
        background: #fbfcff;
        /* justify-content: space-evenly; */
    }

    .content {
        padding-top: 46px;
        padding-left: 38px;
    }

    h2 {
        font-weight: 500;
        font-size: 12px;
        color: #9999b5;
        margin: 0;
        margin-bottom: 7px;
    }

    input {
        height: 44px;
        background: #f4f5f6;
        border-radius: 4px;
        border: none;
        width: 200px;
    }

    input:focus {
        border: none;
    }

    .header {
        width: 245px;
        height: 80px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: #a1a2b2;
        font-weight: 600;
        border-bottom: solid 3px #eff1f9;
        cursor: pointer;
    }

    .header.selected {
        border-bottom: solid 4px #a3aee6;
        color: #191b3f;
        background: #fff;
    }
</style>
