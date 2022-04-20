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
.mailing
    h1.heading Статьи каждую неделю
    p.text Больше 90% учеников прошли полный курс и смогли<br>собрать свой первый компьютер
    .input
        input(placeholder="E-mail")
        button(@mousedown = 'clickButton()') Подписаться
</template>

<style lang="scss">
.mailing{
    padding: 0 10% 40px 10%;
    .heading{
        font-size: 48px;
        font-weight: 700;
        text-align: center;
        margin-bottom: 30px;
    }
    .text{
        font-size: 16px;
        font-weight: 100;
        text-align: center;
        margin-bottom: 60px;
    }
    .input{
        background: rgba(255, 255, 255, 0.199);
        border-radius: 50px;
        width: 60%;
        margin: 0 auto;
        display: flex;
        input{
            width: 90%;
            padding: 15px 40px;
            padding-right: 0;
            background: none;
            border: none;
            color: #fff;
            font-size: 16px;
            font-family: Roboto;
            &:focus{
                outline: none;
            }
        }
        button{
            padding: 15px 40px;
            font-size: 16px;
            background: linear-gradient(94.78deg, #DF5950 11.19%, #451046 93.72%);
            border: none;
            border-radius: 50px;
            color: #fff;
            font-family: Roboto;
            font-weight: 700;
            margin-left: auto;
            margin-right: 0em;
            min-width: 200px;
            cursor:pointer;
        }
    }
}

@media (max-width: 800px){
    .mailing{
        padding: 0 5% 40px 5%;
        .heading{
            font-size: 36px;
        }
        .input{
            width: 100%;
            input{
                width: 90%;
                padding: 15px 20px;
                font-size: 14px;
            }
            button{
                padding: 0 15px;
                font-size: 14px;
                min-width: auto;
            }
        }
    }
}
</style>