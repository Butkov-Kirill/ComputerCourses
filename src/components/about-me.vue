<script>
export default {
    
}
</script>

<template lang="pug">
.about-me
    .sides
        .left
            .picture
                img(src='../assets/images/pc.png')
        .right
            h1.heading Чем мы занимаемся?
            p.text Lorem ipsum dolor sit amet, consectetur adipiscing elit. Eget neque, dignissim 
                |et feugiat elit augue in suspendisse egestas. Dictum vestibulum mi et sed nunc, orci 
                |fermentum vestibulum, morbi. Et neque, adipiscing sapien sem senectus praesent aenean 
                |consequat. Aenean facilisi turpis aliquet fringilla. Nunc sem felis sed interdum feugiat 
                |mattis elit, sollicitudin. Quam pharetra rhoncus risus, cursus id elementum aliquet. 
                |Nullam turpis arcu malesuada arcu interdum placerat nisi, lobortis. 
</template>

<style lang="scss">
.about-me{
    padding: 200px 10% 200px 10%;
    .sides{
        display: flex;
        .left{
            width: 50%;
            .picture{
                position: relative;
                border: 30px solid;
                border-image-source: linear-gradient(94.26deg, #C89AFC 9.51%, #7C6AFA 90.23%);
                width: 450px;
                height: 450px;
                border-image-slice: 1;
                img{
                    position: absolute;
                    top: 18%;
                }
            }
        }
        .right{
            width: 50%;
            .heading{
                font-size: 48px;
                font-weight: 700;
                margin-bottom: 45px;
            }
            .text{
                font-size: 16px;
                font-weight: 400;
                line-height: 160%;
            }
        }
    }
}

@media (max-width: 800px){
    .about-me{
        padding: 100px 10% 50px 10%;
        .sides{
            flex-direction: column;
            .left{
                width: 100%;
                .picture{
                    width: auto;
                    height: 250px;
                    img{
                        width: 100%;
                    }
                }
            }
            .right{
                width: 100%;
                margin-top: 50px;
                .heading{
                    margin-bottom: 30px;
                }
            }
        }
    }
}
</style>