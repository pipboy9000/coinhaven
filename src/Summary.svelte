<script>
    import FaClock from "svelte-icons/fa/FaClock.svelte";
</script>

<main>
    <div class="top">
        <span class="amount">1404.9</span>
        <span class="ratio">GBP per BTC</span>
        <div class="clockIcon">
            <FaClock />
        </div>
        <span class="time">08:00</span>
    </div>
    <div class="fee">
        <div>
            <span class="amount">0.0055468789</span>
            <span class="coin">BTC</span>
        </div>

        <div class="feeRight">
            <span class="amount">299.99</span>
            <span class="coin">GBP</span>
        </div>
        <div>
            <span>Fee</span>
        </div>
        <span class="amount feeRight">10.00</span>
    </div>
    <div class="total">
        <p>Total:</p>
        <span class="amount">309.99</span>
        <span class="coin">GBP</span>
    </div>
</main>

<style>
    main {
        font-size: 12px;
    }

    .amount {
        font-weight: 700;
        margin-right: 8px;
        color: #2f316c;
        font-weight: 500;
    }

    .total {
        background: #191b3f;
        height: 80px;
        display: flex;
        align-items: center;
        padding: 0 24px;
        border-radius: 0 0 5px 5px;
    }

    .total > p {
        color: #d1d1d8;
        font-size: 12px;
    }

    .total > .amount {
        color: #fff;
        font-size: 18px;
        font-weight: 700;
        margin-right: 10px;
        margin-left: auto;
    }

    .total > .coin {
        color: #fff;
        font-size: 13px;
        font-weight: 400;
    }

    .fee {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-column-gap: 0px;
        grid-row-gap: 18px;
        background: #eaebfd;
        padding: 24px;
        box-sizing: border-box;
        margin-top: 1px;
        border-radius: 0 0 5px 5px;
    }

    .top {
        display: flex;
        align-items: center;
        width: 300px;
        height: 50px;
        background: #f1f1fe;
        padding: 30px;
        box-sizing: border-box;
        font-weight: 500;
        color: #2f316c;
        border-radius: 5px 5px 0px 0px;
    }

    .feeRight {
        display: flex;
        justify-content: end;
        margin-right: 0;
    }
    .ratio {
        margin-right: auto;
    }

    .coin {
        font-weight: 500;
    }

    .clockIcon {
        width: 16px;
        height: 16px;
        display: flex;
        margin-right: 8px;
        color: #c1c1d9;
        background: #8283a9;
        border-radius: 100px;
    }

    .time {
        color: #324bc9;
    }
</style>
