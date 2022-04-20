<script>
export default {
    methods: {
        clickButton(){
            alert('Это тестовая версия сайта');
        }
    }
}
</script>

<template lang="pug">
.contacts
    .buttons
        .button(@mousedown = 'clickButton()')
            i(class='fab fa-vk fa-lg')
        .button(@mousedown = 'clickButton()')
            i(class='fab fa-youtube fa-lg')
        .button(@mousedown = 'clickButton()')
            i(class='fab fa-facebook fa-lg')
        .button(@mousedown = 'clickButton()')
            i(class='fab fa-instagram fa-lg')
.copyright
    p Templates #18. More on Figma.info
</template>

<style lang="scss">
.contacts{
    margin-bottom: 50px;
    .buttons{
        display: flex;
        width: 30%;
        margin: 0 auto;
        .button{
            margin: 0 auto;
            background: linear-gradient(94.26deg, #C89AFC 9.51%, #7C6AFA 90.23%);
            border-radius: 50%;
            width: 50px;
            height: 50px;
            position: relative;
            cursor:pointer;
            i{
                color: #fff;
                font-size: 18px;
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
            }
        }
    }
}
.copyright{
    display: flex;
    padding-bottom: 30px;
    p{
        margin: 0 auto;
        font-size: 16px;
        font-weight: 400;
    }
}

@media (max-width: 800px){
    .contacts{
        .buttons{
            width: 80%;
        }
    }
}
</style>