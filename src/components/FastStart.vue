<script>
import StepVisualRect from './other-components/step-visual-rect.vue';

export default {
    components: {
        StepVisualRect
    }
}
</script>

<template lang="pug">
.fast-start
    .heading
        img.circle(src='../assets/images/elipse.svg')
        h1 Быстрый старт
    p.text Больше 90% учеников прошли полный курс и смогли<br>собрать свой первый компьютер
    .steps
        .step
            h1 100%
            StepVisualRect(style='--height: 100%; --c1: #C89AFC 9.51%; --c2: #7C6AFA 90.23%;')
            p Lorem ipsum dolor sit amet, consectetur adipiscing elit. Netus eget velit quisque accumsan 
                |amet tortor. Velit, volutpat egestas fringilla mi porttitor tempus. Placerat dui.
        .step
            h1 75%
            StepVisualRect(style='--height: 75%;  --c1: #7C6AFA 9.51%; --c2: #C89AFC 90.23%;')
            p Lorem ipsum dolor sit amet, consectetur adipiscing elit. Netus eget velit quisque accumsan 
                |amet tortor. Velit, volutpat egestas fringilla mi porttitor tempus. Placerat dui.
        .step
            h1 50%
            StepVisualRect(style='--height: 50%;  --c1: #C89AFC 9.51%; --c2: #7C6AFA 90.23%;')
            p Lorem ipsum dolor sit amet, consectetur adipiscing elit. Netus eget velit quisque accumsan 
                |amet tortor. Velit, volutpat egestas fringilla mi porttitor tempus. Placerat dui.
        .step
            h1 Итог
            StepVisualRect(style='--height: 20%;  --c1: #7C6AFA 9.51%; --c2: #C89AFC 90.23%;')
            p Lorem ipsum dolor sit amet, consectetur adipiscing elit. Netus eget velit quisque accumsan 
                |amet tortor. Velit, volutpat egestas fringilla mi porttitor tempus. Placerat dui.
</template>

<style lang="scss">
.fast-start{
    padding: 0 10% 200px 10%;
    .heading{
        display: flex;
        h1{
            font-size: 48px;
            padding-left: 40px;
            margin: auto 0;
        }
    }
    .text{
        font-size: 16px;
        font-weight: 100;
        padding-top: 50px;
    }
    .steps{
        display: flex;
        margin-top: 80px;
        .step{
            width: 100%;
            h1{
                font-weight: 700;
                font-size: 36px;
                padding-bottom: 25px;
            }
            p{
                font-weight: 100;
                font-size: 14px;
                line-height: 160%;
                padding-top: 25px;
            }
        }
    }
}

@media (max-width: 800px){
    .fast-start{
        padding: 50px 10% 100px 10%;
        .heading{
            h1{
                font-size: 36px;
            }
        }
        .text{
            padding-top: 30px;
        }
        .steps{
            display: flex;
            flex-direction: column;
            margin-top: 80px;
            .step{
                width: 100%;
                margin-bottom: 40px;
                p{
                    padding-top: 25px;
                }
            }
        }
    }
}
</style>