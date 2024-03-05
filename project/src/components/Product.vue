    <template>
        <div class="gamecard">
            <h2>{{ Game.name }}</h2>
            <h2>{{ Game.price }}</h2>
        <img :src = "Game.img" alt="" />
        <button @click = "price++, count++, addToCart()" class="btn">Add to Cart</button>
        </div>

        <div class="addToCart">
      <h2>Shopping Cart</h2>
      <h3>Items in Cart: {{ store.count }}</h3>
      <h3>Total Price: {{ store.price }}</h3>
    </div>
    </template>

    <script setup>
    const props = defineProps({
        Game: Object,
        cart: Array,    
    });
    

    </script>

    <style scoped>
    img {
    width: 50%;
    height: 10rem;
    margin-top: 1.5rem;
    }
    .gamecard {
    width: 25%;
    background-color: var(--secondary);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    border-radius: 1rem;
    margin: 25px 25px;
    box-shadow: 1rem 1rem 0.5rem var(--tertiary);
    padding-bottom: 40px;
    }

    .btn {
    background-color: var(--tertiary);
    padding: 0.5rem;
    font-size: 1.1rem;
    margin: 1rem auto;
    border: solid var(--primary);
    }
    </style>