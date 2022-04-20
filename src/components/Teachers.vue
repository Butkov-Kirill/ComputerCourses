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
.teachers
    .heading
        img(src='../assets/images/elipse.svg')
        h1 Ваши преподаватели
    .humans
        .human
            img.image-human(src='../assets/images/humans/human1.png')
            h1.name Дмитрий Иванов
            p.position Специалист по видеокартам
            button(@mousedown = 'clickButton()') Биография
        .human
            img.image-human(src='../assets/images/humans/human2.png')
            h1.name Дмитрий Иванов
            p.position Специалист по видеокартам
            button(@mousedown = 'clickButton()') Биография
        .human
            img.image-human(src='../assets/images/humans/human3.png')
            h1.name Дмитрий Иванов
            p.position Специалист по видеокартам
            button(@mousedown = 'clickButton()') Биография
</template>

<style lang="scss">
.teachers{
    padding: 0 10% 200px 10%;
    .heading{
        display: flex;
        img{
            transform: rotate(-45deg);
        }
        h1{
            font-weight: 700;
            font-size: 48px;
            margin: auto 0;
            margin-left: 40px;
        }
        margin-bottom: 113px;
    }
    .humans{
        display: flex;
        .human{
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            img{
                margin: 0 auto;
            }
            .name{
                margin: 0 auto;
                margin-top: 40px;
                margin-bottom: 15px;
            }
            .position{
                font-weight: 100;
                font-size: 14px;
                margin: 0 auto;
                margin-bottom: 40px;
            }
            button{
                width: 80%;
                background: none;
                border: 1px solid #fff;
                color: #fff;
                font-weight: 400;
                font-size: 16px;
                padding: 15px 0;
                border-radius: 50px;
                margin: 0 auto;
                cursor: pointer;
            }
        }
    }
}

@media (max-width: 800px){
    .teachers{
        padding: 0 10% 100px 10%;
        .heading{
            flex-direction: column;
            img{
                width: 30%;
                margin: 0 auto;
            }
            h1{
                font-size: 30px;
                margin: 0 auto;
            }
            margin-bottom: 70px;
        }
        .humans{
            flex-direction: column;
            .human{
                margin-bottom: 60px;
                &:last-child{
                    margin-bottom: 0;
                }
            }
        }
    }
}
</style>