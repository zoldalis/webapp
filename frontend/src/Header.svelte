<script>
</script>

<header class="header">
    <div class="header-text">
        Dudko Mikhail
    </div>
    <div class="header-buttons">
        <button class="header-button">Home</button>
        <button class="header-button">About</button>
        <button class="header-button">Services</button>
        <button class="header-button">Portfolio</button>
        <button class="header-button">Contact</button>
    </div>
</header>

<style>
    .header-text {
        font-size: 2em;
        font-weight: bold;
        order: 0;
    }

    .header {
        background-color: #333; 
        color: white;
        padding: 1em 2em;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-direction: row;
        position: fixed; 
        top: 0; 
        left: 0; 
        width: 100%; 
        z-index: 10; 
        box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }

    .header-buttons {
            margin-right: 3em;
        }

    .header-button {
        background: none;
        border: 2px solid white;
        color: white;
        padding: 0.5em 1em;
        margin-left: 10px; 
        font-size: 1em;
        cursor: pointer;
        transition: background-color 0.3s, color 0.3s;
    }

    .header-button:hover {
        background-color: white;
        color: #333;
    }

    @media (max-width: 810px) {

        .header-buttons {
            margin-bottom: 0.5em;
        }

        .header-button {
            padding: 0.3em 0.6em;
            margin-left: 7px; 
            font-size: 0.9em;
        }

        .header-text {
            font-size: 1.5em;
        }
    }

    @media (max-width: 640px) {
        .header {
            flex-direction: column;
        }

        .header-text {
            order: 1;
        }
    }
</style>
