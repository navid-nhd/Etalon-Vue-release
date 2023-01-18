<template>
    <section class="special-offer container-fluid" id="special-offer">
            <div class="container">
                <div class="timer-holder">
                    <h4 class="timer-header">Sale ends soon</h4>
                    <ul class="timer list-unstyled">
                        <li class="timer-item">
                            <div class="timer-number">3</div>
                            <div class="timer-unit">Days</div>
                        </li>
                        <li class="timer-item">
                            <div class="timer-number">23</div>
                            <div class="timer-unit">Hours</div>
                        </li>
                        <li class="timer-item">
                            <div class="timer-number">15</div>
                            <div class="timer-unit">Minutes</div>
                        </li>
                        <li class="timer-item">
                            <div class="timer-number">33</div>
                            <div class="timer-unit">Seconds</div>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="shoe-holder hidden md:block">
                <div class="shoe-off">70% OFF</div>
                <div class="shoe-picture">
                    <img src="src/image/4.png" alt="shoe">
                </div>
                
            </div>
        </section>
</template>
<script>
</script>
<style scoped> 
 /* ------- SPECIAL OFFER ------*/
.special-offer {
    background-color: var(--etalon-primary);
    text-align: center;
    height: 226px;
    position: relative;
}
.timer-holder {
    padding: 32px 15px 48px;
}
.timer-header {
    font-weight: 700;
    font-size: 32px;
    line-height: 32px;
    color: var(--etalon-white);
}
.timer {
    margin:  0 -12px;
    display: flex;
    justify-content: center;
}
.timer-item {
    padding: 32px 12px 12px;
    flex-shrink: 1;  
}
.timer-number {
    width: 54px;
    height: 56px;
    background-color: rgba(0,0,0,0.25);
    border-radius: 8px;
    font-family: var(--etalon-font-secondry);
    font-weight: 700;
    font-size: 24px;
    line-height: 32px;
    color: var(--etalon-white);
    display: flex;
    justify-content: center;
    align-items: center;
}
.timer-unit {
    padding: 12px 0 0;
    font-family: var(--etalon-font-secondry);
    color: var(--etalon-white);
    font-weight: 300;
    font-size: 12px;
    line-height: 14px;
    text-align: center;
}
.shoe-holder {
    position: absolute;
    top: 20%;
    left: -22vw;
}
.shoe-picture {

}
.shoe-picture > img{
    transform: scaleX(1);
    width: 28vw;
    height: auto;
}
.shoe-off {
    position: relative;
    top: 0;
    font-family: var(--etalon-font-secondry);
    font-weight: 700;
    font-size: 64px;
    line-height: 48px;
    padding-bottom: 32px;
}
@media  screen and (min-width : 768px) {
    .special-offer {
        padding-left: 10%;
        text-align: left;
        border-left: 33.33vw solid var(--etalon-yellow);
        height: 450px;
    }
    .timer-header {
        font-size: 64px;
        line-height: 48px;
    }
    .timer {
        margin:  0 -24px;
        justify-content: flex-start;
    }
    .timer-holder {
        padding: 78px 15px 0px;
    }
    .timer-item {
        padding: 93px 24px 12px;  
    }
    .timer-number {
        width: 108px;
        height: 112px;
        font-size: 48px;
        line-height: 40px;
    }
    .timer-unit { 
        font-size: 18px;
        line-height: 36px;
    }
    
}
@media  screen and (min-width : 1200px) { 
    .timer-number {
        width: 153px;
        height: 112px;
        font-size: 64px;
        line-height: 48px;
    }
    .timer-unit { 
        font-size: 24px;
        line-height: 48px;
    }

}
</style>