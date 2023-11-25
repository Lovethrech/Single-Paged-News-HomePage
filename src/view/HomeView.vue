<script setup>
import Header from "../component/Header.vue";
</script>
<template>
    <Header></Header>
    <div class="headline">
        <div class="first-section">
            <div class="image"></div>
            <div class="content">
                <div class="head">
                    <h1 style="font-weight:900;">The Bright Future of Web 3.0?</h1>
                </div>
                <div class="text">
                    <p>The dive into the evolution of the web that claims to put
                        the power of the platforms back into the hand of the people.
                        But is it really fulfilling its promise?
                    </p>
                    <button>READ MORE</button>
                </div>
            </div>
        </div>
        <div class="second-section">
            <h2 style="color:hsl(35, 77%, 62%); font-weight: 600; font-size:30px; margin:10px 0;">New</h2>
            <div>
                <h3>Hydrogen VS Electric Cars</h3>
                <p style="color: hsl(0, 0%, 73%);">Will hydrogen-fueled cars ever catch up to EVs?</p>
            </div><br><hr><br>
            <div>
                <h3>The Downside of AI Artistry</h3>
                <p style="color: hsl(0, 0%, 73%);">What are the possible adverse effects of on-demand AI image generation?</p>
            </div><br><hr><br>
            <div>
                <h3>Is VC Funding Drying Up?</h3>
                <p style="color: hsl(0, 0%, 73%);">Private funding by VC firms is down 50% YOY.
                    We take a look at what that means.
                </p>
            </div><br>
        </div>
    </div>
    <div class="lastLine">
        <div class="contain-content">
            <div class="image">
                <img src="/public/image-retro-pcs.jpg" alt="Retro">
            </div>
            <div class="text">
                <h3 style="color:hsl(233, 8%, 79%); font-size:30px;">01</h3>
                <h4 style="font-size:20px; font-weight:700;">Reviving Retro Pcs</h4>
                <p style="font-size:16px;">What happens when old PCs are given modern upgrades?</p>
            </div>
        </div>
        <div class="contain-content">
            <div class="image">
                <img src="/public/image-top-laptops.jpg" alt="Top Laptop">
            </div>
            <div class="text">
                <h3 style="color:hsl(233, 8%, 79%); font-size:30px;">02</h3>
                <h4 style="font-size:20px; font-weight:700;">Top 10 Laptops of 2022</h4>
                <p style="font-size:16px;">Our best pick for various needs and budge.</p>
            </div>
        </div>
        <div class="contain-content">
            <div class="image">
                <img src="/public/image-gaming-growth.jpg" alt="Gaming growth">
            </div>
            <div class="text">
                <h3 style="color:hsl(233, 8%, 79%); font-size:30px;">03</h3>
                <h4 class="title" style="font-size:20px; font-weight:700;">The Growth of Gaming</h4>
                <p style="font-size:16px;">How the pandemic has sparked fresh opportunities.</p>
            </div>
        </div>
    </div>
</template>
<style scoped>
.headline{
    margin: 20px 0 70px;
    display:flex;
    gap:20px;
}
.first-section{
    width:50vw;
    height:90px;
}
.first-section .image{
    background-image:url('/public/image-web-3-desktop.jpg');
    width: 100%;
    height:40vh;
}
.content{
    width:100%;
    display:flex;
    gap:30px;
    margin-top:20px;
}
.content .head{
    width:200px;
    font-weight:900;
}
.content .text{
    font-size: 16px;
    width: 40vw;
    text-align: justify;
}
.text button{
    background-color:hsl(5, 85%, 63%);
    color: hsl(0, 100%, 100%);
    margin: 20px 0;
    padding:15px 30px;
    letter-spacing:5px;
}

.second-section{
    background-color: hsl(0, 0%, 0%);
    color: hsl(0, 100%, 100%);
    width:30vw;
    padding: 10px 20px 0;
}

.lastLine{
    width:100%;
    margin:120px 0;
    display:flex;
    flex-direction: row;
    gap:25px;
}
.lastLine .contain-content{
    display:flex;
    flex-direction: row;
    gap:15px;
    height:29vh;
}
.lastLine .contain-content .image img{
    width:8vw;
    height:100%;
}

@media screen and (max-width:950px) and (min-width:651px){
    .lastLine .contain-content{
        display:block;
        width:30vw;
        height:20vh;
    }
    .lastLine .contain-content .image img{
        width:100%;
        height:30vh;
    }
}
@media screen and (max-width:650px){
    .headline{
        display:flex;
        flex-direction: column;
    }
    .first-section{
        width:100%;
        height:90px;
    }
    .first-section .image{
        background-image:url('/public/image-web-3-mobile.jpg');
        width: 100%;
        height:40vh;
    }
    .content{
        width:100%;
        display:block;
    }
    .content .head{
        width:100%;
        font-weight:900;
    }
    .content .text{
        font-size: 16px;
        width: 100%;
    }
    .second-section{
        background-color: hsl(0, 0%, 0%);
        color: hsl(0, 100%, 100%);
        width:100%;
        margin-top:70vh;
        padding: 10px 20px 0;
    }

    .lastLine{
        display: block;
    }
    .lastLine .contain-content{
        display:flex;
        width:100%;
        margin:40px 0;
    }
    .lastLine .contain-content .image img{
        width: 40vw;
        height:100%;
    }
    .contain-content .text{
        height:40vh;
    }
}
@media screen and (max-width:495px){
    .lastLine .contain-content .image img{
        width: 25vw;
        height:100%;
    }
    .contain-content .text p{
        font-size:14px;
    }
}
@media screen and (max-width:380px) {
    .second-section{
        margin-top:80vh;
    }
}
@media screen and (max-width:280px){
    .second-section{
        margin-top: 90vh;
    }
    .lastLine .contain-content{
        display:block;
        width:100%;
        height:100%;
        margin: 10px 0;
    }
    .lastLine .contain-content .image img{
        width:100%;
        height:100%;
    }
}
</style>
