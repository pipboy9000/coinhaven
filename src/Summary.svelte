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
</main>

<style>
    main {
    }
    .top {
        display: flex;
        align-items: center;
        width: 300px;
        height: 50px;
        background: #f1f1fe;
    }
    .ratio {
        margin-right: auto;
    }

    .clockIcon {
        width: 16px;
        height: 16px;
        display: flex;
    }
</style>
