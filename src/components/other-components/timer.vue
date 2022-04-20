<script>
export default {
    props: {
        day: {
            Type: Number,
            default: 18
        },
        hours: {
            Type: Number,
            default: 18
        },
        minuts: {
            Type: Number,
            default: 18
        },
        seconds: {
            Type: Number,
            default: 18
        }
    },
    data(){
        return{
            _day : 0,
            _hours : 0,
            _minuts : 0,
            _seconds : 0,
        }
    },
    methods:{
        TimerActive(){
            return this._day==0 && this._hours==0 && this._minuts==0 && this._seconds==0;
        }
    },
    mounted(){
        this.$nextTick(function(){
            this._day = this.day;
            this._hours = this.hours;
            this._minuts = this.minuts;
            this._seconds = this.seconds;
            let time = setInterval(function(){
                if (!this.TimerActive()){
                    this._seconds--;
                }
                if (this._seconds <=0 && !this.TimerActive()){
                    if (this._minuts > 0){
                        this._seconds=60;
                        this._minuts--;
                    }
                }
                if (this._minuts <=0 && !this.TimerActive()){
                    if (this._hours > 0){
                        this._minuts=59;
                        this._hours--;
                    }
                }
                if (this._hours <=0 && !this.TimerActive()){
                    if (this._day>0 && this._minuts==0 && this._seconds==0){
                        this._hours=24;
                        this._seconds=60;
                        this._day--;
                    }
                }
            }.bind(this), 1000);
        });
    }
}
</script>

<template lang="pug">
.timer(id='timer')
    .number(id='timer-day')
        h1 {{_day}}
        p Дней
    .number(id='timer-hours')
        h1 {{_hours}}
        p Часов
    .number(id='timer-minuts')
        h1 {{_minuts}}
        p Минут
    .number(id='timer-seconds')
        h1 {{_seconds}}
        p Секунд
</template>

<style lang="scss">
.timer{
    display: flex;
    margin-top: 50px;
    margin-bottom: 140px;
    .number{
        background: #121212;
        padding: 20px 30px 20px 30px;
        margin-right: 30px;
        h1{
            font-size: 30px;
            margin: 0;
            text-align: center;
        }
        p{
            margin: 0;
            font-size: 16px;
            font-weight: 100;
            padding-top: 10px;
        }
    }
}

@media (max-width: 800px){
.timer{
    margin-bottom: 50px;
    .number{
        padding: 0;
        width: 50px;
        height: 50px;
        padding: 5px;
        margin-right: 0;
        margin: 0 auto;
        h1{
            margin-top: 8px;
            font-size: 15px;
        }
        p{
            font-size: 10px;
            padding-top: 5px;
            text-align: center;
        }
    }
}
}
</style>