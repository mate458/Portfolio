<template>
  <div id="app-body">
        <div class="side-section1"></div>
        <section>
            <img src="../../public/Img/FP_1.png" class="profilePhoto">
            <br>
            <h2>Mateo Alonso Pabón García</h2>
            <h4>Alias: Kathar6</h4>
            <hr>
            <p>{{ProfileDescription}}</p>
            <br>
            <info-block :title-info="titleInfoBlockLanguages" :images-info="imagesInfoLanguages"/>
            <info-block :title-info="titleInfoBlockProjects" :images-info="imagesInfoProjects"/>
        </section>
        <div class="side-section2"></div>
  </div>
</template>

<script>
import InfoBlock from './info-block';
export default {
    name:"app-body",
    components: {
        InfoBlock
    },
    data(){
        return{
            ProfileDescription:`I'm a technologist in analysis and development of information systems, I have experecience in programming since i was 16 years old, Throughout my studies I made many projects I've done several projects in various programming languages`,
            titleInfoBlockLanguages:"Programming Languages",
            imagesInfoLanguages:[
                {
                    id:1,
                    imgUrl:"/Img/js_logo.png",
                    url:"https://developer.mozilla.org/es/docs/Web/JavaScript"
                },
                {
                    id:2,
                    imgUrl:"/Img/php_logo.png",
                    url:"https://www.php.net"
                },
                {
                    id:3,
                    imgUrl:"/Img/Csharp_Logo.png",
                    url:"https://docs.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/"
                }
            ],
            titleInfoBlockProjects:"Projects",
            imagesInfoProjects:[
                {
                    id:1,
                    imgUrl:"/Img/udea_logo.png",
                },
                {
                    id:2,
                    imgUrl:"/Img/ARI_Logo.png",
                    url:"https://github.com/Kathar6/A.R.I"
                }
            ],
            colors: [
                'indigo',
                'warning',
                'pink darken-2',
                'red lighten-1',
                'deep-purple accent-4',
            ],
            slides: [
                'First',
                'Second',
                'Third',
                'Fourth',
                'Fifth',
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../scss/_variables.scss';
    /* # Section Styles */
    #app-body{
        display:grid;
        grid-template-columns: 1fr 3fr 1fr;
        margin-top:25vh;
    }
    // # Body Blocks
    .side-section1, section, .side-section2{
        background-color:$white2;
        height:150vh;
        -webkit-box-shadow: inset 0px 181px 13px -183px rgba(0,0,0,.75);
        -moz-box-shadow: inset 0px 181px 13px -183px rgba(0,0,0,.75);
        box-shadow: inset 0px 181px 13px -183px rgba(0,0,0,.75);
    }
    .side-section2, .side-section1{
        opacity:.85;
    }
    .side-section1{
        grid-column: 1/2;
    }
    section{
        grid-column: 2/3;
        padding:0 1vw;
        hr{
            margin:3vh 0;
        }
    // # Profile Photo
        .profilePhoto{
            display:flex;
            align-items: center;
            width:10vw;
            max-width:10vw;
            height:20vh;
            max-height:20vh;
            border: 1px solid rgba(124, 124, 124, 0.75);
            border-radius:100%;
            -webkit-box-shadow:0px 0px 15px -3px rgba(0,0,0,.75);
            -moz-box-shadow:0px 0px 15px -3px rgba(0,0,0,.75);
            box-shadow:0px 0px 15px -3px rgba(0,0,0,.75);
            margin:10vh auto 2vh auto;
        }
        &>h2, &>h4{
            text-align:center;
        }
    }
    .side-section2{
      grid-column: 3/4;
    }
    
</style>