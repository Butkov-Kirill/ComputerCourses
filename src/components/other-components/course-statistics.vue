<script>
export default {
    props: {
        all_members: {
            Type: Number,
            default: 0
        },
        graduates: {
            Type: Number,
            default: 0
        },
        earnings:{
            Type: Number,
            default: 1000
        }
    },
    data(){
        return{
            earnings_string : 0,
            procentages : 0
        }
    },
    mounted(){
        this.$nextTick(function(){
            this.earnings_string = this.earnings;
            let space_id=0;
            if (this.earnings_string.length==6){
                space_id = 2;
            } else if (this.earnings_string.length==5){
                space_id = 1;
            } else if (this.earnings_string.length==7){
                space_id = [0,3];
                console.log(space_id);
            }
            let newString = '';
            for(let i=0; i<this.earnings_string.length; i++){
                newString+=this.earnings_string[i];
                if (space_id!=[0,3]){
                    if (space_id==i){
                        newString+=' ';
                    }
                }
                if (JSON.stringify(space_id)==JSON.stringify([0,3])){
                    for(let j=0; j<2; j++){
                        if (space_id[j]==i){
                            newString+=' ';
                        }
                    }
                }
            }
            this.earnings_string = newString;

            this.procentages = (this.earnings*100)/1000000;
            document.getElementById('progress-bar').style.width = this.procentages+'%';
        });
    },
    methods: {
        clickButton(){
            alert('Это тестовая версия сайта');
        }
    }
}
</script>

<template lang="pug">
.course-statistics
    button(@mousedown='clickButton()') Заказать курс
    .members
        p Учеников всего: 
            span {{all_members}}
        p Успешно закончили курс: 
            span {{graduates}}
    .earnings
        p Заработано учениками: 
            span {{earnings_string}}₽
        .progress-bar
            .progress(id='progress-bar')
        .progress-numbers
            p 0
            p 1 000 000₽
</template>

<style lang="scss">
.course-statistics{
    background: #121212;
    padding: 20px 10% 20px 10%;
    display: flex;
    button{
        background: linear-gradient(94.78deg, #DF5950 11.19%, #451046 93.72%);
        border-radius: 50px;
        font-weight: 700;
        font-size: 16px;
        color: #fff;
        border: none;
        padding: 10px 30px 10px 30px;
        cursor: pointer;
        margin: auto 0;
        cursor: pointer;
    }
    .members{
        margin: 0 auto;
        width: 25%;
        margin-top: auto;
        margin-bottom: auto;
        p{
            font-size: 16px;
            font-weight: 100;
            display: flex;
            width: 100%;
            span{
                font-weight: 400;
                margin-left: auto;
                margin-right: 0em;
            }
        }
    }
    .earnings{
        display: flex;
        flex-direction: column;
        width: 40%;
        p{
            font-size: 16px;
            font-weight: 100;
            display: flex;
            width: auto;
            span{
                font-weight: 400;
                margin-left: 5%;
            }
        }
        .progress-bar{
            background: #fff;
            height: 5px;
            width: 100%;
            position: relative;
            .progress{
                width: 10%;
                height: 5px;
                background: linear-gradient(94.78deg, #DF5950 11.19%, #451046 93.72%);
                position: absolute;
            }
        }
        .progress-numbers{
            display: flex;
            width: 100%;
            p{
                width: auto;
                &:last-child{
                    margin-left: auto;
                    margin-right: 0em;
                }
            }
        }
    }
}

@media (max-width: 800px){
    .course-statistics{
        flex-direction: column;
        .members{
            width: 100%;
            margin: 0;
            margin-top: 15px;
        }
        .earnings{
            display: flex;
            flex-direction: column;
            width: 100%;
        }
    }
}
</style>