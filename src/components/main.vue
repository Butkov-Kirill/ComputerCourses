<script>
import Timer from './other-components/timer.vue';
import Statistics from './other-components/course-statistics.vue';

export default {
    components: {
        Timer,
        Statistics
    },
    methods: {
        clickButton(){
            alert('Это тестовая версия сайта');
        }
    }
}
</script>

<template lang="pug">
.main
    .header
        img.icon(src='../assets/images/logo.svg')
        .buttons
            button Главная
            button Курсы
            button Расписание
            button Преподаватели
            button Рассылка
            button Контакты
        button.LogIn(@mousedown='clickButton()') Зайти в кабинет
    .content
        h1.name-site Первый курс<br>по компьютерной сборке
        Timer(day=18, hours=12, minuts=2, seconds=14)
        //Timer(day=0, hours=0, minuts=0, seconds=5)
    Statistics(all_members=200, graduates=190, earnings=400000)
</template>

<style lang="scss">
.main{
    background: url('../assets/images/background-first.png');
    background-size: cover;
    padding: 0;
    .header{
        display: flex;
        padding: 38px 5% 38px 5%;
        .buttons{
            margin-left: auto;
            margin-right: 100px;
            margin-top: auto; margin-bottom: auto;
            button{
                color: #fff;
                background: none;
                border: none;
                font-family: Roboto;
                font-weight: 400;
                margin-left: 56px;
                font-size: 14px;
                border-bottom: 1px solid transparent;
                cursor: pointer;
                &:hover{
                    transition: 0.3s;
                    border-bottom: 1px solid #fff;
                }
            }
        }
        .LogIn{
            color: #fff;
            border: none;
            background: linear-gradient(94.26deg, #C89AFC 9.51%, #7C6AFA 90.23%);
            border-radius: 50px;
            padding: 10px 30px 10px 30px;
            font-size: 14px;
            cursor: pointer;
        }
    }
    .content{
        padding: 130px 15% 0px 15%;
        .name-site{
            font-size: 40px;
        }
    }
}

@media (max-width: 800px){
.main{
    .header{
        padding: 15px 5% 15px 5%;
        .buttons{
            display: none;
        }
        .LogIn{
            margin-left: auto;
            margin-right: 0em;
        }
    }
    .content{
        padding: 50px 10% 0px 10%;
        .name-site{
            font-size: 30px;
        }
    }
}
}
</style>