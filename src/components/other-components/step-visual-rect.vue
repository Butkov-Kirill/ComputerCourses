<template lang="pug">
.step-visual-rect
    .rect
</template>

<style lang="scss">
.step-visual-rect{
    width: 100%;
    height: 80px;
    display: flex;
    .rect{
        height: var(--height);
        margin: auto 0;
        width: 100%;
        background: linear-gradient(94.26deg, var(--c1), var(--c2));
    }
}

@media (max-width: 800px){
    .step-visual-rect{
        height: 60px;
    }
}
</style>