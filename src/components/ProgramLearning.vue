<template lang="pug">
.program-learning
    .heading
        img(src='../assets/images/elipse.svg')
        h1.name-page Программа обучения
        p Больше 90% учеников прошли полный курс и смогли<br>собрать свой первый компьютер
    .active-by-week
        .sides
            .left
                .week
                    p.heading Неделя №1
                    .text
                        .liner
                        p Красивая часть курса,<br>которая помогает в успехе
                .week
                    p.heading Неделя №3
                    .text
                        .liner
                        p Красивая часть курса,<br>которая помогает в успехе
                .week
                    p.heading Неделя №5
                    .text
                        .liner
                        p Красивая часть курса,<br>которая помогает в успехе 
                .week
                    p.heading Неделя №7
                    .text
                        .liner
                        p Красивая часть курса,<br>которая помогает в успехе
            .border
            .right
                .week
                    p.heading Неделя №2
                    .text
                        .liner
                        p Красивая часть курса,<br>которая помогает в успехе
                .week
                    p.heading Неделя №4
                    .text
                        .liner
                        p Красивая часть курса,<br>которая помогает в успехе
                .week
                    p.heading Неделя №6
                    .text
                        .liner
                        p Красивая часть курса,<br>которая помогает в успехе
</template>

<style lang="scss">
.program-learning{
    padding: 0 10% 200px 10%;
    .heading{
        display: flex;
        flex-direction: column;
        img{
            margin: 0 auto;
            transform: rotate(135deg);
            margin-bottom: 80px;
        }
        .name-page{
            font-weight: 700;
            font-size: 48px;
            text-align: center;
            margin-bottom: 30px;
        }
        p{
            font-size: 16px;
            font-weight: 100;
            text-align: center;
        }
        margin-bottom: 80px;
    }
    .active-by-week{
        .sides{
            display: flex;
            .week{
                margin-bottom: 100px;
                position: relative;
                .heading{
                    font-weight: 100;
                    font-size: 14px;
                    margin-bottom: 5px;
                }
                .text{
                    p{
                        font-weight: 400;
                        font-size: 18px;
                        line-height: 160%;
                    }
                    .liner{
                        height:1px;
                        width: 40px;
                        background: #fff;
                        position: absolute;
                    }
                }
            }
            .left{
                width: 50%;
                display: flex;
                flex-direction: column;
                justify-content: right;
                .week{
                    margin-right: 60px;                    
                    .heading{
                        text-align: right;
                    }
                    .text{
                        p{
                            text-align: right;
                        }
                        .liner{
                            left: auto;
                            right: -60px;
                            transform: translate(0, 8px);
                        }
                    }
                    &:last-child{
                        margin-bottom: 5px;
                    }
                }
            }
            .right{
                width: 50%;
                display: flex;
                flex-direction: column;
                justify-content: left;
                .week{
                    margin-left: 60px;
                    transform: translate(0, 85%);
                    .liner{
                        transform: translate(-60px, 8px);
                    }
                }
            }
            .border{
                border-right:6px solid;
                border-image-source: linear-gradient(94.26deg, #C89AFC 9.51%, #7C6AFA 90.23%);
                border-image-slice: 1;
            }
        }
    }
}

@media (max-width: 800px){
    .program-learning{
        padding: 0 10% 100px 10%;
        .heading{
            display: flex;
            flex-direction: column;
            img{
                margin-bottom: 50px;
            }
        }
        .active-by-week{
            width: 100%;
            .sides{
                .week{
                    .heading{
                    }
                    .text{
                        p{
                            font-size: 14px;
                        }
                    }
                }
                .left{
                    .week{
                        margin-right: 60px;                    
                        .heading{
                            font-size: 14px;
                        }
                    }
                }
                .right{
                    .week{
                        transform: translate(0, 75%);
                    }
                }
            }
        }
    }
}
</style>