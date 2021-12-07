<script>
    import FaWallet from "svelte-icons/fa/FaWallet.svelte";
    import FaHome from "svelte-icons/fa/FaHome.svelte";
    import FaExchangeAlt from "svelte-icons/fa/FaExchangeAlt.svelte";
    import FaMoneyCheckAlt from "svelte-icons/fa/FaMoneyCheckAlt.svelte";
    import FaMoneyBillWave from "svelte-icons/fa/FaMoneyBillWave.svelte";
    import FaUserCog from "svelte-icons/fa/FaUserCog.svelte";
    import FaDollarSign from "svelte-icons/fa/FaDollarSign.svelte";
    import MdSettings from "svelte-icons/md/MdSettings.svelte";

    let isOpen = true;

    let exchangeOpen = false;
</script>

<main>
    <div class="brand">
        <img src="images/logo.jpg" alt="brand logo" />
        <p>Coinhaven</p>
    </div>
    <ul class="list">
        <li>
            <div class="icon">
                <FaHome />
            </div>
            <p>Dashboard</p>
        </li>
        <li>
            <div class="icon">
                <FaWallet />
            </div>
            <p>Wallet</p>
        </li>
        <li>
            <div class="icon">
                <FaExchangeAlt />
            </div>
            <p>Exchange</p>
        </li>

        <li>
            <ul class="exchange">
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
            <p>Finance</p>
        </li>
        <li>
            <div class="icon">
                <FaMoneyBillWave />
            </div>
            <p>Transaction</p>
        </li>
        <li>
            <div class="icon">
                <FaUserCog />
            </div>
            <p>Account Management</p>
        </li>
        <li>
            <div class="icon">
                <FaDollarSign />
            </div>
            <p>Merchant Account</p>
        </li>
        <li>
            <div class="icon">
                <MdSettings />
            </div>
            <p>API Management</p>
        </li>
    </ul>
</main>

<style>
    main {
        background: #191b3f;
        min-width: 290px;
        height: 100vh;
        position: relative;
        overflow-y: scroll;
    }

    main::-webkit-scrollbar {
        display: none;
    }

    .brand {
        display: flex;
        align-items: center;
        justify-content: center;
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
        padding-left: 14px;
        cursor: pointer;
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

    ul.exchange {
        list-style: disc;
        padding-left: 24px;
        width: 100%;
    }

    .exchange > li {
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
