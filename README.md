@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@500&display=swap');
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
body{
    overflow: hidden;
}
.wrapper{
    position: relative;
    width: 100%;
    height: 100vh;
    overflow: hidden;
}
.formInput{
    position: absolute;
    top: -100%;
    width: 40%;
    left: 50%;
    transform: translateX(-50%);
    background-color: #EA4C89;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 70;
    border-radius: 20px;
    transition: 1s;
    overflow: hidden;
    padding-bottom: 10px;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
    animation: formInput 1s 3s forwards;
}
@keyframes formInput {
    0%{
        top: -100%;
    }
    100%{
        top: 20px;
    }
}
.formInput::before{
    position: absolute;
    content: '';
    width: 8px;
    height: 40px;
    background: #EA4C89;
    top: -30px;
    left: 20%;
    z-index: -10;
}
.formInput::after{
    position: absolute;
    content: '';
    width: 8px;
    height: 40px;
    background: #EA4C89;
    top: -30px;
    right: 20%;
    z-index: -1;
}
.boxHands{
    position: absolute;
    display: flex;
    justify-content: center;
    top: -40%;
    animation: handsCat 1s 4s forwards ease-in;
}
@keyframes handsCat{
    0%{
        top: -40%;
    }
    100%{
        top: 0px;
    }
}
.formInput .handsCat{
    position: absolute;
    transform: rotate(180deg);
    width: 80px;
    top: -60px;
    animation: hands 1s 5s forwards ease-in-out;
}
@keyframes hands{
    0%{
        top: -60px;
    }
    50%,100%{
        top: -150px;
    }
}
.handsCat img{
    width: 100%;
}
.boxHands h1{
    transform: rotate(20deg);
    transform-origin: top left;
    padding-top: 5px;
    color: #fff;
    font-size: 50px;
    font-family: 'Dancing Script', cursive;
    animation: textHand 1.5s 6s forwards ease-in;
}
@keyframes textHand{
    0%{
        transform: rotate(20deg);
        transform-origin: top left;
    }
    20%,100%{
        transform: rotate(0deg);
        transform-origin: top left;
    }
}
.boxSlider{
    position: relative;
    margin-top: 70px;
    width: 100%;
    display: flex;
    justify-content: center;
    opacity: 0;
    transition: 1s;
    animation: boxSlider 1s 8s forwards ease-out;
}
@keyframes boxSlider {
    0%{
        opacity: 0;
    }
    100%{
        opacity: 1;
    }
}
.boxSlider .left, .boxSlider .right{
    position: absolute;
    top: 50%;
    color: #fff;
    transform: translateY(-50%);
    font-size: 30px;
    cursor: pointer;
    z-index: 50;
}
.left{
    left: 100px;
}
.right{
    right: 100px;
}

.listSlider{
    position: relative;
    width: 200px;
    height: 100px;
    display: flex;
    overflow: hidden;
    border-radius: 10px;
}

.listSlider .slider{
    width: 100%;
    position: relative;
    transition: 0.5s;
}
.listSlider img{
    width: 200px;
    height: 100%;
    object-fit: cover;
}
.boxHandsInput{
    display: flex;
    position: relative;
    top: 15px;
    right: -200%;
    width: 50%;
    animation: boxInputHands 1s 9s forwards ease-in;
}
@keyframes boxInputHands{
    0%{
    right: -200%;
    }
    60%,100%{
        right: 0%;
    }
}
.boxHandsInput input{
    width: 100%;
    height: 30px;
    border: none;
    outline: none;
    border-radius: 5px;
    padding: 0px 10px;
    font-family: 'Dancing Script', cursive;
    font-size: 20px;
    z-index: 11;
    opacity: 0;
    animation: boxSlider 1s 9s forwards ease-out;
}

.boxHandsInput .handsCatImgInput{
    position: absolute;
    width: 80px;
    transform: rotate(270deg);
    top: -140%;
    right: -30px;
    z-index: 100;
    animation: imgHandInput 1s 10s forwards ease-in-out;
}
@keyframes imgHandInput {
    0%{
    right: -30px;
    }
    70%,100%{
        right: -100%;
    }
}
.boxHandsInput .handsCatImgInput img{
    width: 100%;
}
.buttonLove{
    display: flex;
    position: relative;
    margin-top: 25px;
    align-items: center;
    transform: translateY(-100%);
    z-index: 10;
    width: 35px;
    transition: 0.5s;
}
.buttonLove .cricleBtn{
    width: 40px;
    height: 40px;
    background: #ffb7e4;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 10;
    transform: scale(0);
    transition: 0.5s;
    box-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px,
                inset rgb(255, 255, 255,0.8) 1.95px 1.95px 2.6px,
                inset rgba(0, 0, 0, 0.2) -1.95px -1.95px 2.6px;
}
.buttonLove .button{
    position: absolute;
    outline: none;
    width: 0px;
    height: 0px;
    cursor: pointer;
    border-radius: 5px;
    transition: 0.5s;
    z-index: 9;
    background: #FD89C3;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 12px;
    font-family: 'Roboto', sans-serif;
    user-select: none;
    color: #fff;
    box-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px,
                inset rgb(255, 255, 255,0.8) 1.95px 1.95px 2.6px,
                inset rgba(0, 0, 0, 0.2) -1.55px -1.55px 2.6px;
}
.buttonLove .button:hover{
    background: #ff9fda;
}
.boxCar{
    position: absolute;
    bottom: 15%;
    transform: translateX(-400px);
    z-index: 2;
    animation: car 4s 1s forwards, car1 2s 5s forwards;
}
.boxCar img{
    width: 350px;
}
@keyframes car{
    0%{
        transform: translateX(-400px);
    }
    50%,100%{
        transform: translateX(150px);
    }
}
.boxHeart{
    position: relative;
    width: 100%;
    height: 100vh;
    animation:  heartX 4s 1s forwards;
}
/* @keyframes car1 {
    0%{
        transform: translateX(150px);
    }
    100%{
        transform: translateX(1000px);
    }
} */
.heart1,.heart2,.heart3, .heart4, .heart5, .heart6{
    position: absolute;
    width: 15px;
    height: 15px;
    background-color: rgb(255, 62, 65);
    transform: scale(0.2) rotate(45deg);
    bottom: 20%;
    left: 450px;
    z-index: 1;
}
.heart1{
    animation:love1 4s infinite ease-in 1s;
}
.heart2{
    animation: love2 3s infinite ease-in 2s;
}
.heart3{
    animation: love2 5s infinite ease-in 1.5s;
}
.heart4{
    animation: love1 2s infinite ease-in 2s;
}
.heart5{
    animation: love1 2.3s infinite ease-in 0.5s;
}
.heart5{
    animation: love2 2.5s infinite ease-in 1.5s;
}
.heart1::before, .heart2::before,
.heart3::before,.heart4::before, .heart5::before, .heart6::before{
    position: absolute;
    content: '';
    width: 100%;
    height: 100%;
    background-color: rgb(255, 62, 65);
    left: -50%;
    border-radius: 50%;
}
.heart1::after, .heart2::after,
.heart3::after, .heart4::after, .heart5::after, .heart6::after{
    position: absolute;
    content: '';
    width: 100%;
    height: 100%;
    background-color: rgb(255, 62, 65);
    top: -50%;
    border-radius: 50%;
}
@keyframes love1{
    0%{
        opacity: 0;
        transform: scale(0.3) rotate(0deg) translate3d(40px, 0, 0);
    }
    50%{
        opacity: 1;
    }
    100%{
        opacity: 0;
        transform: scale(0.9) rotate(-15deg) translate3d(-20px, -300px, 0);
    }
}
@keyframes love2{
    0%{
        opacity: 0;
        transform: scale(0.2) rotate(10deg) translate3d(50px, 0, 0);
    }
    50%{
        opacity: 1;
    }
    100%{
        opacity: 0;
        transform: scale(0.7) rotate(5deg) translate3d(-20px, -250px, 0);
    }
}
@keyframes heartX {
    0%{
        left: -500px;
    }
    50%,100%{
        left: 0px;
    }
}
.boxLine{
    position: relative;
    width: 1000px;
    height: 100vh;
    margin: auto;
    overflow: hidden;
    z-index: 50;
}
.ground-line {
    width: 100%;
    position: absolute;
    bottom: 15%;
    left: 0;
    overflow: hidden;
    height: 6px;
}
.ground-line div {
    width: 2000px;
    font-size: 0;
    animation: roadLine 3s infinite linear;
}
.ground-line .line1 {
    width: 80px;
}
.ground-line .line2 {
    width: 300px;
}
.ground-line .line3 {
    width: 40px;
}
.ground-line .line4 {
    width: 200px;
}
.ground-line .line5 {
    width: 280px;
}
.ground-line span {
    height: 6px;
    display: inline-block;
    background-color: #4b1a61;
    -webkit-border-radius: 6px;
    -moz-border-radius: 6px;
    border-radius: 6px;
    vertical-align: bottom;
    margin-right: 20px;
}
@keyframes roadLine{
    0% {
        -webkit-transform: translate(0, 0);
        -moz-transform: translate(0, 0);
        transform: translate(0, 0);
    }
    
    100% {
        -webkit-transform: translate(-1000px, 0);
        -moz-transform: translate(-1000px, 0);
        transform: translate(-1000px, 0);
    }
}
/* .ground-line::before{
    position: absolute;
    content: '';
    width: 100%;
    height: 100%;
    background: repeating-linear-gradient(90deg, transparent 0, transparent 30%, #333 30%, #333 100%);
    background-size: 70px;
} */
.loadingLove{
    position: absolute;
    width: 100%;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    top: 0;
    left: 0;
    z-index: 100;
    background-color: #fff;
}
.rhombus {
    border-radius: 10px;
    height: 75px;
    width: 75px;
}

.rhombus:before {
    content: "";
    position: absolute;
    background: #EA4C89;
    height: 40px;
    width: 40px;
    z-index: 0;
    margin-top: 15px;
    margin-left: 15px;
    transform: rotate(45deg);
}

.rhombus .circle1 {
    content: "";
    position: absolute;
    background: #EA4C89;
    height: 40px;
    width: 40px;
    z-index: 1;
    border-radius: 50%;
    animation-duration: 2s;
    animation-name: change1;
    animation-iteration-count: infinite;
    /*animation-direction: alternate;*/
}

.rhombus .circle2 {
    content: "";
    position: absolute;
    background: #EA4C89;
    height: 40px;
    width: 40px;
    z-index: 1;
    margin-left: 30px;
    border-radius: 50%;
    animation-duration: 2s;
    animation-name: change2;
    animation-iteration-count: infinite;
    /*animation-direction: alternate;*/
}
@keyframes change1 {
    0%,
    25% {
        margin-top: 0px;
        margin-left: 0px;
    }
    50%,
    75% {
        margin-top: 30px;
        margin-left: 30px;
    }
}

@keyframes change2 {
    25%,
    50% {
        margin-top: 30px;
        margin-left: 0px;
    }
    75%,
    100% {
        margin-top: 0px;
        margin-left: 30px;
    }
}
.element, .heartRain{
    position: absolute;
    pointer-events: none;
    transition: 1s;
}
.letters{
    position: absolute;
    width: 65px;
    transition: 10s ease-in-out;
    cursor: pointer;
    z-index: 1000;
}
.letters img{
    width: 100%;
}
.wrapperLetterForm{
    position: absolute;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    z-index: 1000;
    background: rgba(0, 0, 0, 0.7);
    display: none;
}
.boxLetter{
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}
.boxLetter .formLetter{
    position: relative;
    width: 600px;
    height: 350px;
    background-color: #FFEBEB;
    border-radius: 20px;
    z-index: 100;
    padding: 20px 15px;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
}
.formLetter .wrapperLetter{
    position: relative;
    width: 100%;
    height: 100%;
    border: 2px dashed #FF6666;
    border-radius: inherit;
    display: flex;
}
.boxLetter .before{
    position: absolute;
    width: 600px;
    height: 350px;
    background: #fff;
    transform: rotate(-15deg);
    border-radius: 20px;
    z-index: 10;
}
.formLetter .heartLetter{
    position: absolute;
    width: 30px;
    height: 30px;
    border-radius: 50%;
    background: #FFEBEB;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 10;
}
.heartLetter .heartLetterItem{
    position: relative;
    width: 10px;
    height: 10px;
    transform: rotate(45deg);
    background: #FF6666;
}
.heartLetter:first-child{
    right: 5px;
    top: 10px;
}
.heartLetter:nth-child(2){
    left: 5px;
    bottom: 10px;
}
.heartLetterItem::before, .heartLetterItem::after{
    position: absolute;
    content: '';
    width: 100%;
    height: 100%;
    border-radius: 50%;
    background: inherit;
}
.heartLetterItem::before{
    top: -50%;
}
.heartLetterItem::after{
    left: -50%;
}
.giftbox{
    position: relative;
    width: 40%;
    height: 100%;
}
.giftbox .img{
    position: absolute;
    width: 180px;
    bottom: -10px;
    left: 50px;
    z-index: 100;
}
.giftbox img{
    width: 100%;
}
.textLetter{
    position: relative;
    width: 60%;
    flex-direction: column;
    display: flex;
    align-items: center;
    user-select: none;
}
.textLetter h2{
    margin-top: 20px;
    font-size: 30px;
    font-family: 'Dancing Script', cursive;
}
.textLetter .contentLetter{
    font-size: 19px;
    text-align: center;
    padding: 0px 10px;
    margin-top: 10px;
    font-family: 'Dancing Script', cursive;

}
.fa-xmark{
    position: absolute;
    right: 20px;
    top: 20px;
    color: #fff;
    cursor: pointer;
    font-size: 25px;
}
.show{
    display: block;
}
.heartAnimation{
    position: absolute;
    width: 200px;
    bottom: 0;
}
.heartAnimation img{
    width: 100%;
}
.mewmew1, .mewmew2{
    position: absolute;
    width: 90px;
}
.mewmew1{
    bottom: 0;
    left: 0;
}
.mewmew2{
    bottom: 0;
    right: 0;
}
.mewmew1 img, .mewmew2 img{
    width: 100%;
}




