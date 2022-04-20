<script>
import msi_image from '../assets/images/msi.png';

export default {
    data(){
        return{
            pairs: [
                msi_image,msi_image,msi_image,msi_image,msi_image,msi_image,msi_image,msi_image
            ],
            columns_parents: [],
            columns: []
        }
    },
    mounted(){
        this.$nextTick(function(){
            let pairs_parent = document.getElementById('pairs-icons');
            let columns = Math.ceil(this.pairs.length/2);
            console.log('columns: '+columns);
            let columns_parents = Math.ceil(columns/2);
            console.log('columns parents: '+columns_parents);
            let pairs_inject = 0;
            for (let i=0; i<columns; i++){
                let columns_parents_element = document.createElement('div');
                columns_parents_element.className = 'columns-parents';
                pairs_parent.appendChild(columns_parents_element);
                this.columns_parents[i] = columns_parents_element;
            }
            for (let i=0; i<this.columns_parents.length; i++){
                let column = document.createElement('div');
                column.className = 'column';
                this.columns_parents[i].appendChild(column);
                for (let j=0; j<2; j++){
                    if (pairs_inject!=this.pairs.length){
                        let icon = document.createElement('img');
                        icon.src=this.pairs[pairs_inject];
                        column.appendChild(icon);
                        pairs_inject++;
                    }
                }
            }
        });
    }
}
</script>

<template lang="pug">
.pairs
    .heading
        img(src='../assets/images/elipse.svg')
        h1 Партнеры - топовые бренды
    .pairs-icons(id='pairs-icons')
    
</template>

<style lang="scss">
.pairs{
    padding: 0 10% 200px 10%;
    display: flex;
    flex-direction: column;
    
    .heading{
        display: flex;
        img{
            transform: rotate(135+45deg);
        }
        h1{
            font-weight: 700;
            font-size: 48px;
            margin: auto 0;
            margin-left: 50px;
        }
        margin-bottom: 100px;
    }
    .pairs-icons{
        display: flex;
        margin: 0 auto;
        .columns-parents{
            display: flex;
            .column{
                display: flex;
                flex-direction: column;
                img{
                    padding: 30px 60px 30px 60px;
                    width: 160px;
                    border-right: 1px solid #fff;
                    border-bottom: 1px solid #fff;
                    &:last-child{
                        border-bottom: none;
                    }
                }
            }
            &:last-child{
                .column:last-child{
                    img{
                        border-right: none;
                    }
                }
            }
        }
        
    }
}

@media (max-width: 800px){
    .pairs{
        padding: 0 10% 100px 10%;
        .heading{
            h1{
                font-weight: 700;
                font-size: 35px;
                margin: auto 0;
                margin-left: 50px;
            }
            margin-bottom: 50px;
        }
        .pairs-icons{
            display: flex;
            flex-direction: column;
            margin: 0 auto;
            .columns-parents{
                display: flex;
                .column{
                    display: flex;
                    img{
                        padding: 30px 60px 30px 60px;
                        width: 100px;
                        border-right: none;
                        border-bottom: 1px solid #fff;
                        &:last-child{
                            border-bottom: 1px solid #fff;
                        }
                    }
                }
                &:last-child{
                    .column:last-child{
                        img:last-child{
                            border-bottom: none;
                        }
                    }
                }
            }

        }
    }
}
</style>