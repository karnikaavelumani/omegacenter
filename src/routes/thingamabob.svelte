<script lang="ts">
    import App from '$lib/components/App.svelte';
  </script>
  
<section class="thingamabob-container">
    <div class="thingamabob-content">
        <div class="thingamabob-image">
            <App />
        </div>
        <div class="thingamabob-text">
            <div class="thingamabob-header">
                <h1>Thingamabob</h1>
            </div>
            <div class="thingamabob-rating">
                <p>⭐⭐⭐⭐✩ 4.5/5 stars</p>
            </div>
            <div class="thingamabob-description">
                <p> Check out our latest release reaching rave reviews from many buyers. This intricate device is a captivating blend of countless knobs, buttons, mesmerizing lights, and so much more. Grab one today before they are all sold out! </p>
            </div>
            <div class="thingamabob-features">
                <h2>Features</h2>
                <ul>
                    <li>Knobs</li>
                    <li>Buttons</li>
                    <li>Lights</li>
                    <li>More</li>
                </ul>
            </div>
            <div class="thingamabob-price">
                <h2>Price</h2>
                <p>$99.99</p>
            </div>
        </div>
    </div>
</section>
  
<style>
    .thingamabob-container {
        display: grid;
    }

    .thingamabob-content {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 20px;
    }

    /* .thingamabob-image {
        display: grid;
        justify-self: center;
        align-items: center;
    } */

    @media (max-width: 768px) {
        .thingamabob-content {
            grid-template-columns: 1fr;
        }
    }
    /* .thingamabob-container {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        padding: 20px;
    }

    .thingamabob-content {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        width: 100%;
    }

    .thingamabob-text {
        flex: 1;
        padding: 20px;
    }

    .thingamabob-header h1 {
        font-size: 24px;
        margin: 0;
    }

    .thingamabob-rating p {
        font-size: 16px;
        margin: 10px 0;
    }

    .thingamabob-description p {
        font-size: 16px;
        margin: 10px 0;
    }

    .thingamabob-features h2 {
        font-size: 20px;
        margin: 10px 0;
    }

    .thingamabob-features ul {
        list-style: none;
        padding: 0;
    }

    .thingamabob-features li {
        font-size: 16px;
    }

    .thingamabob-price h2 {
        font-size: 20px;
        margin: 10px 0;
    }

    .thingamabob-price p {
        font-size: 24px;
        margin: 10px 0;
    }

    .thingamabob-image {
        flex: 1;
    }

    @media (max-width: 768px) {
        .thingamabob-container {
            flex-direction: column;
        }
        .thingamabob-text {
            padding: 20px;
            text-align: center;
        }
        .thingamabob-image {
            margin-top: 20px;
            text-align: center;
        }
    } */
  </style>
  