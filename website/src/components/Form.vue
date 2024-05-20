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
    margin: 0;
    max-width: var(--lb-space-3xl);
    text-align: left;

}

.subscription-form form {
    display: flex;
    justify-content: space-between;
    border-top: none;

}

.subscription-form input[type="email"] {
    flex-grow: 1;
    margin-right: var(--lb-space-2xs);
    padding: var(--lb-space-xs);
    border: 1px solid var(--lb-bg-body-d-1);
    border-radius: var(--lb-radius-s);
    font-size: var(--lb-text-m);
    outline-color: var(--lb-accent);
    box-sizing: border-box;
}

.subscription-form button {
    padding: var(--lb-space-xs) var(--lb-space-s);
    border: none;
    background-color: var(--lb-bg-body-d-1);
    color: var(--lb-text);
    border-radius: var(--lb-radius-s);
    cursor: pointer;
    font-size: var(--lb-text-m);
    font-weight: var(--lb-font-700);
    box-sizing: border-box;
}

.subscription-form button:hover {
    background-color: var(--lb-bg-body-d-3);
}
</style>