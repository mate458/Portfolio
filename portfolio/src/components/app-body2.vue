<template>
    <v-container fluid id="container-body">
        <v-row>
            <v-col cols="12" class="block-spacer">

            </v-col>
        </v-row>
        <v-row>
            <v-col cols="2" class="grey lighten-4 block-side">
            </v-col>
            <v-col cols="8" class="text-center black--text grey lighten-5">
                <h1 class="portfolio-title text-center">Portfolio</h1>
                <hr>
                <img src="../../public/Img/FP_1.png" class="profilePhoto">
                <br>
                <h2>Mateo Alonso Pabón García</h2>
                <h4>Alias: Kathar6</h4>
                <hr>
                <p>{{ProfileDescription}}</p>
                <br>
                <a id="languages"></a>
                <info-block :title-info="titleInfoBlockLanguages" :images-info="imagesInfoLanguages"/>
                <p>I've made many projects along my studies, like social networks, application systems, and the most important project that I've made with my university classmates is a smart recycling assistant</p>
                <a id="projects"></a>
                <info-block :title-info="titleInfoBlockProjects" :images-info="imagesInfoProjects"/>
                <br>
            </v-col>
            <v-col cols="2" class="grey lighten-4 block-side">
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import InfoBlock from './info-block';
export default {
    name:"app-body2",
    components: {
        InfoBlock
    },
    data(){
        return{
            opacityCol:0.5,
            ProfileDescription:`I'm a technologist in analysis and development of information systems, I have experecience in programming since i was 16 years old, Throughout my studies I made many projects in various programming languages like PHP, JS, Python and C#`,
            titleInfoBlockLanguages:"Programming Languages",
            imagesInfoLanguages:[
                {
                    id:1,
                    imgUrl:"/Img/js_logo.png",
                    url:"https://developer.mozilla.org/es/docs/Web/JavaScript",
                    altImg:"JavaScript"
                },
                {
                    id:2,
                    imgUrl:"/Img/php_logo.png",
                    url:"https://www.php.net",
                    altImg:"PHP"
                },
                {
                    id:3,
                    imgUrl:"/Img/Csharp_Logo.png",
                    url:"https://docs.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/",
                    altImg:"C#"
                },
                {
                    id:4,
                    imgUrl:"/Img/python_logo.png",
                    url:"https://www.python.org",
                    altImg:"Python"
                }
            ],
            titleInfoBlockProjects:"Projects",
            imagesInfoProjects:[
                {
                    id:1,
                    imgUrl:"/Img/udea_logo.png",
                    altImg:"Application System project (Private) \nLanguages: PHP, JS"
                },
                {
                    id:2,
                    imgUrl:"/Img/ARI_Logo.png",
                    url:"https://github.com/Kathar6/A.R.I",
                    altImg:"Smart recycling assistant \nLanguages: Python, PHP, HTML, CSS, JS"
                },
                {
                    id:3,
                    imgUrl:"/Img/VFO_logo.png",
                    url:"https://github.com/Kathar6/VFO",
                    altImg:"Social network for the Villa Flora School \nLanguages: PHP, HTML, CSS, JS"
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
    
    // # Body Blocks
    #container-body{
        padding:0;
    }
    .block-spacer{
        margin:15vh 0vw;
    }
    .block-side{
        opacity:.85;
    }
    .portfolio-title{
        margin:10vh 0vw;
    }
    // # Profile Photo
    .profilePhoto{
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
        transition:box-shadow .7s;
        &:hover{
            -webkit-box-shadow:0px 0px 15px -3px rgba(0,0,0,.75);
            -moz-box-shadow:0px 0px 15px -3px rgba(0,0,0,.75);
            box-shadow:0px 0px 15px -3px rgba(0,0,0,.75);
        }
    }
    h2, h4{
        text-align:center;
    }
    
</style>