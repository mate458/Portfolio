<template>
    <div>
        <h2>{{title}}</h2>
        <hr>
        <div class="block-icons" v-for="image in images" v-bind:key="image.id">
            <a :href="image.url" target="_blank">
                <span v-bind:title="image.altImg" class="block-border">
                    <img :src="image.imgUrl" class="block-image"/>
                </span>
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name:"info-block",
    props: {
        titleInfo: String,
        imagesInfo: Array
    },
    data(){
        return{
            title:this.titleInfo,
            images:this.imagesInfo
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../scss/_variables.scss';
    h3{
       text-align: center;
       margin-bottom:3vh; 
    }
    .block-icons{
        display: inline-block;
        padding:5vh 1vw 0 1vw;
        margin-bottom:5vh;
        & *{
            margin:0 1vw;
            text-align:center;
        }
        span{
            transition-property: background-color box-shadow;
            transition-duration:.7s;
            &:hover{
                background-color: rgba($color: #bdbdbd, $alpha: 0.7);
                -webkit-box-shadow:0px 0px 15px -3px rgba($color: #fff, $alpha: 1);
                -moz-box-shadow:0px 0px 15px -3px rgba($color: #fff, $alpha: 1);
                box-shadow:0px 0px 15px -3px rgba($color: #fff, $alpha: 1);
            }
        }
        .block-border{
            width:10vw;
            height:15vh;
            border: 1px solid rgba($color: #c8c8c8, $alpha: 0.75);
            border-radius:100%;
            -webkit-box-shadow:0px 0px 15px -3px rgba(0,0,0,.75);
            -moz-box-shadow:0px 0px 15px -3px rgba(0,0,0,.75);
            box-shadow:0px 0px 15px -3px rgba(0,0,0,.75);
        }
        .block-image{
            min-width:10vw;
            max-width: 15vw;
            min-height:15vh;
            max-height:20vh;
        }
    }
    
</style>