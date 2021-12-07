<script>
    import FaSearch from "svelte-icons/fa/FaSearch.svelte";
    import FaAngleDown from "svelte-icons/fa/FaAngleDown.svelte";
    import FaBell from "svelte-icons/fa/FaBell.svelte";

    let search;

    let newNotification = true;
</script>

<main>
    <div class="search">
        <div class="icon">
            <FaSearch />
        </div>
        <input type="text" bind:value={search} placeholder="Search" />
    </div>
    <div class="notification" class:newNotification>
        <FaBell />
    </div>
    <div class="profilePic" />
    <div class="seperator" />
    <button
        >English / USD
        <div class="downArrow">
            <FaAngleDown />
        </div>
    </button>
    <button>Download</button>
</main>

<!-- markup (zero or more items) goes here -->
<style>
    .notification {
        width: 20px;
        color: #acacbb;
        margin-right: 36px;
        min-width: 20px;
        margin-left: 36px;
        position: relative;
    }

    .newNotification::before {
        width: 10px;
        height: 10px;
        background: #e3645f;
        position: absolute;
        content: "";
        border-radius: 100px;
        top: -2px;
        right: -4px;
    }

    .profilePic {
        background: url("../images/profile-pic.jpg");
        width: 48px;
        min-width: 48px;
        height: 48px;
        border-radius: 100px;
        background-size: cover;
        background-position: center;
        border: 3px solid white;
        margin-right: 36px;
    }
    .seperator {
        height: 30px;
        width: 1.5px;
        background: #d9d9e4;
    }

    button {
        margin: 0;
        padding: 0;
        height: 100%;
        width: 148px;
        font-size: 14px;
        color: #9495b6;
        outline: none;
        border: none;
        background: none;
        font-weight: 500;
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
    }

    .downArrow {
        width: 12px;
        width: 6px;
        margin-left: 8px;
    }
    main {
        width: 100%;
        height: 112px;
        background: #ebebf0;
        display: flex;
        align-items: center;
    }

    .search {
        display: flex;
        align-items: center;
        position: relative;
        margin-left: 38px;
        margin-right: 12px;
        max-width: 420px;
        width: 100%;
        margin-right: auto;
    }

    .search > .icon {
        width: 20px;
        height: 20px;
        position: absolute;
        padding-left: 28px;
        color: #ebebf0;
    }

    .search > input {
        margin: 0;
        padding: 0;
        height: 58px;
        width: 100%;
        font-size: 18px;
        padding-left: 78px;
        border: none;
        border-radius: 5px;
    }

    .search > input:focus {
        outline: none;
    }

    .search > input::placeholder {
        color: #ebebf0;
    }
</style>
