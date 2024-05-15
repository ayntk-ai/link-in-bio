<template>
    <div class="subscription-form">
        <form>
            <input type="email" placeholder="Your email" />
            <button type="submit">Subscribe</button>
        </form>
    </div>
</template>

<style scoped>
.subscription-form {
    padding: 20px;
    max-width: 500px;
    margin: auto;
}

.subscription-form form {
    display: flex;
    justify-content: space-between;
}

.subscription-form input[type="email"] {
    flex-grow: 1;
    margin-right: 10px;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-size: 16px;
}

.subscription-form button {
    padding: 10px 20px;
    border: none;
    background-color: #333;
    color: #fff;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
    font-weight: bold;
}

.subscription-form button:hover {
    background-color: #555;
}
</style>