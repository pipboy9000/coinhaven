<script>
    import FaWallet from "svelte-icons/fa/FaWallet.svelte";
    import FaHome from "svelte-icons/fa/FaHome.svelte";
    import FaExchangeAlt from "svelte-icons/fa/FaExchangeAlt.svelte";
    import FaMoneyCheckAlt from "svelte-icons/fa/FaMoneyCheckAlt.svelte";
    import FaMoneyBillWave from "svelte-icons/fa/FaMoneyBillWave.svelte";
    import FaUserCog from "svelte-icons/fa/FaUserCog.svelte";
    import FaDollarSign from "svelte-icons/fa/FaDollarSign.svelte";
    import MdSettings from "svelte-icons/md/MdSettings.svelte";

    let isOpen = false;

    let exchangeOpen = false;
</script>

<main
    class:isOpen
    on:click={() => {
        isOpen = !isOpen;
        if (!isOpen) exchangeOpen = false;
    }}
>
    <div class="brand" class:isOpen>
        <img src="images/logo.jpg" alt="brand logo" />
        <p class:hideTag={!isOpen}>Coinhaven</p>
    </div>
    <ul class="list">
        <li>
            <div class="icon">
                <FaHome />
            </div>
            <p class:hideTag={!isOpen}>Dashboard</p>
        </li>
        <li>
            <div class="icon">
                <FaWallet />
            </div>
            <p class:hideTag={!isOpen}>Wallet</p>
        </li>
        <li
            on:click|stopPropagation={() => {
                exchangeOpen = !exchangeOpen;
                if (exchangeOpen) isOpen = true;
            }}
        >
            <div class="icon">
                <FaExchangeAlt />
            </div>
            <p class:hideTag={!isOpen}>Exchange</p>
        </li>

        <li class="exchange" class:exchangeOpen>
            <ul>
                <li>Instant</li>
                <li>Spot</li>
                <li>Margin</li>
                <li>Peer 2 Peer</li>
            </ul>
        </li>

        <li>
            <div class="icon">
                <FaMoneyCheckAlt />
            </div>
            <p class:hideTag={!isOpen}>Finance</p>
        </li>
        <li>
            <div class="icon">
                <FaMoneyBillWave />
            </div>
            <p class:hideTag={!isOpen}>Transaction</p>
        </li>
        <li>
            <div class="icon">
                <FaUserCog />
            </div>
            <p class:hideTag={!isOpen}>Account Management</p>
        </li>
        <li>
            <div class="icon">
                <FaDollarSign />
            </div>
            <p class:hideTag={!isOpen}>Merchant Account</p>
        </li>
        <li>
            <div class="icon">
                <MdSettings />
            </div>
            <p class:hideTag={!isOpen}>API Management</p>
        </li>
    </ul>
</main>

<style>
    main {
        background: #191b3f;
        min-width: 64px;
        width: 64px;
        height: 100vh;
        position: relative;
        overflow-y: scroll;
        transition: all 0.3s ease-out;
    }

    main.isOpen {
        min-width: 290px;
        width: 290px;
    }

    p {
        opacity: 1;
        max-width: 180px;
        transition: all 0.3s ease-out;
    }

    .hideTag {
        max-width: 0;
        opacity: 0;
    }

    main::-webkit-scrollbar {
        display: none;
    }

    .brand {
        display: flex;
        align-items: center;
        justify-content: center;
        padding-left: 10px;
        transition: padding-left 0.3s ease-out;
    }

    .brand.isOpen {
        padding-left: 0;
    }

    .brand > p {
        font-family: serif;
        color: white;
        font-size: 37px;
        margin-left: 14px;
        font-weight: 700;
    }

    ul {
        padding: 0;
    }

    li {
        color: #8c8c9e;
        display: flex;
        align-items: center;
        padding-left: 20px;
        cursor: pointer;
    }

    li > p {
        white-space: nowrap;
    }

    .list {
        margin-top: 0;
    }

    .list > li:after {
        position: absolute;
        width: 5px;
        height: 5px;
        background: white;
    }

    .exchange {
        max-height: 0;
        overflow: hidden;
        transition: all 0.3s ease-out;
    }

    .exchangeOpen {
        max-height: 300px;
    }

    .exchange > ul {
        list-style: disc;
        padding-left: 24px;
        width: 100%;
    }

    .exchange > ul > li {
        display: list-item;
        padding-left: 10px;
        padding-top: 14px;
        padding-bottom: 14px;
        width: 100%;
    }

    li:hover {
        background: #383a64;
        color: white;
    }

    .icon {
        width: 20px;
        height: 20px;
        margin-right: 14px;
    }
</style>
