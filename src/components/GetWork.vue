<template lang="pug">
.get-work
    h1.heading Получите профессию прямо сейчас
    .points
        .paragraph
            img.icon(src='../assets/images/icons/pc.svg')
            h1.heading Только практические<br>навыки в работе
            p.text Lorem ipsum dolor sit amet, consectetur adipiscing elit. Netus eget velit quisque 
                |accumsan amet tortor. Velit, volutpat egestas fringilla mi porttitor tempus. Placerat dui.
        .paragraph
            img.icon(src='../assets/images/icons/usb-flash.svg')
            h1.heading Работа на самом<br>современном оборудовании
            p.text Lorem ipsum dolor sit amet, consectetur adipiscing elit. Netus eget velit quisque 
                |accumsan amet tortor. Velit, volutpat egestas fringilla mi porttitor tempus. Placerat dui.
        .paragraph
            img.icon(src='../assets/images/icons/usb.svg')
            h1.heading Сертификация<br>по окончании обучения
            p.text Lorem ipsum dolor sit amet, consectetur adipiscing elit. Netus eget velit quisque 
                |accumsan amet tortor. Velit, volutpat egestas fringilla mi porttitor tempus. Placerat dui.
</template>

<style lang="scss">
.get-work{
    padding: 0 10% 200px 10%;
    .heading{
        font-weight: 700;
        font-size: 48px;
        text-align: center;
        margin-bottom: 120px;
    }
    .points{
        display: flex;
        .paragraph{
            width: 100%;
            padding: 0 20px 0 20px;
            display: flex;
            flex-direction: column;
            .icon{
                margin: auto 0;
                margin-bottom: 50px;
                height: 100px;
            }
            .heading{
                font-weight: 500;
                font-size: 20px;
                line-height: 140%;
                margin-bottom: 30px;
            }
            p{
                font-size: 16px;
                line-height: 160%;
                font-weight: 100;
                text-align: center;
            }
        }
    }
}

@media (max-width: 800px){
    .get-work{
        padding: 0 10% 100px 10%;
        .heading{
            font-size: 36px;
            margin-bottom: 50px;
        }
        .points{
            flex-direction: column;
            .paragraph{
                width: 100%;
                padding: 0;
                flex-direction: column;
                margin-bottom: 50px;
                .icon{
                    margin-bottom: 25px;
                }
                .heading{
                    margin-bottom: 15px;
                }
            }
        }
    }
}
</style>