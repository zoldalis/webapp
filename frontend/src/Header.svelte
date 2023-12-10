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
    }

    .header {
        background-color: #333; /* Dark background */
        color: white;
        padding: 1em 2em;
        display: flex;
        justify-content: space-between; /* Space between text and buttons */
        align-items: center;
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
</style>
