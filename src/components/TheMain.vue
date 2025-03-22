<template>
    <div class="main">
        <div class="main__text-container">
            <div class="main__top fade-in fade-in--delay-1">
                <span class="main__top-line"></span>
                <span class="main__top-text">
                    OVER 1M CREATORS
                </span>
            </div>
            <h1 class="main__heading fade-in fade-in--delay-2">
                Discover And Create NFTs
            </h1>
            <p class="main__text fade-in fade-in--delay-3">
                Discover, Create and Sell NFTs On Our NFT Marketplace With Over Thousands Of NFTs And Gey a 
                <span class="main__text-bold">
                    $20 bonus.
                </span>
            </p>
            <div class="main__buttons fade-in fade-in--delay-4">
                <button class="main__explore">
                    EXPLORE MORE
                </button>
                <button class="main__create">
                    CREATE NFT
                </button>
            </div>
            <div class="main__statistics fade-in fade-in--delay-4">
                <div class="main__statistic">
                    <h3 class="main__statistic-number">
                        430K+
                    </h3>
                    <span class="main__statistic-text">
                        Art Works
                    </span>
                </div>
                <div class="main__statistic">
                    <h3 class="main__statistic-number">
                        159K+
                    </h3>
                    <span class="main__statistic-text">
                        Creators
                    </span>
                </div>
                <div class="main__statistic">
                    <h3 class="main__statistic-number">
                        87K+
                    </h3>
                    <span class="main__statistic-text">
                        Collections
                    </span>
                </div>
            </div>
        </div>
        <div class="main__img-container">
            <img src="@/assets/Image.png" alt="" class="main__image slide-in slide-in--delay-1">
            <img src="@/assets/Blur.png" alt="" class="main__blur slide-in slide-in--delay-2">
            <img src="@/assets/Arrow.png" alt="" class="main__arrow fade-in-arrow">
            <img src="@/assets/background.png" alt="" class="main__background fade-in-arrow">
        </div>
    </div>
</template>

<style scoped lang="scss">
@import '@/assets/styles/variables.scss';

.main {
    display: flex;
    justify-content: center;
    margin-top: 3rem;
    margin-bottom: 8rem;

    @media (max-width: $breakpoint-mobile) {
        flex-direction: column;
    }

    &__text-container {
        display: flex;
        flex-direction: column;
        padding-left: 3rem;
        @media (max-width: $breakpoint-mobile) {
            align-items: center;
            padding-left: 0;
        }
    }

    &__top {
        display: flex;
        align-items: center;
        gap: .5rem;
        justify-content: start;
        margin-bottom: 1rem;

        @media (max-width: $breakpoint-mobile) {
            justify-content: center;
        }

        &-line {
            border: 1px solid #201f1f;
            width: 195px;
            height: 0px;
            opacity: 0.2;

            @media (max-width: $breakpoint-tablet) {
                width: 138px;
            }
            @media (max-width: $breakpoint-mobile) {
                width: 33px;
            }
        }

        &-text {
            font-weight: 600;
            font-size: 10px;
            line-height: 120%;
            letter-spacing: 0.1em;
            color: #201f1f;
            opacity: .6;
            display: none;

            @media (max-width: $breakpoint-mobile) {
                display: inline;
            }
        }
    }

    &__heading {
        max-width: 570px;
        font-weight: 600;
        font-size: 76px;
        line-height: 111%;
        letter-spacing: -0.04em;
        text-transform: capitalize;
        color: #141416;

        @media (max-width: $breakpoint-tablet) {
            max-width: 400px;
            font-size: 54px;
            line-height: 115%;
        }
        @media (max-width: $breakpoint-mobile) {
            max-width: 315px;
            font-size: 40px;
            line-height: 112%;
            text-align: center;
        }
    }

    &__text {
        max-width: 500px;
        font-weight: 400;
        font-size: 18px;
        line-height: 156%;
        color: #676767;
        margin-top: 2rem;
        margin-bottom: 2rem;

        @media (max-width: $breakpoint-tablet) {
            font-size: 13px;
            line-height: 138%;
        }
        @media (max-width: $breakpoint-mobile) {
            max-width: 315px;
            font-size: 11px;
            line-height: 161%;
            text-align: center;
        }

        &-bold {
            font-weight: 600;
            color: #141416;
        }
    }

    &__buttons {
        display: flex;
        gap: 1rem;
    }

    &__explore {
        border-radius: 12px;
        padding: 18px 29px;
        width: 180px;
        height: 60px;
        border: none;
        background: #000;
        font-weight: 500;
        font-size: 16px;
        letter-spacing: 0.01em;
        text-transform: uppercase;
        color: #fff;
        cursor: pointer;

        &:hover {
            background: #222;
            transform: scale(1.05);
            transition: all .3s ease;
        }

        @media (max-width: $breakpoint-tablet) {
            border-radius: 9px;
            width: 130px;
            height: 42px;
            font-size: 11px;
            padding: 10px 20px;
        }
        @media (max-width: $breakpoint-mobile) {
            border-radius: 10px;
            width: 128px;
            height: 47px;
            font-size: 11px;
        }
    }

    &__create {
        border: 2px solid #000;
        border-radius: 12px;
        padding: 18px 21px;
        width: 140px;
        height: 60px;
        background: transparent;
        font-weight: 500;
        font-size: 16px;
        letter-spacing: 0.01em;
        text-transform: uppercase;
        color: #000;
        cursor: pointer;

        &:hover {
            background: #d7d7d7;
            transform: scale(1.05);
            transition: all .3s ease;
        }

        @media (max-width: $breakpoint-tablet) {
            border: 1.07px solid #000;
            border-radius: 9px;
            width: 100px;
            height: 42px;
            font-size: 11px;
            padding: 10px 10px;
        }
        @media (max-width: $breakpoint-mobile) {
            border: 0.65px solid #000;
            border-radius: 10px;
            width: 99px;
            height: 47px;
            font-size: 11px;
        }
    }

    &__statistics {
        display: flex;
        gap: 3rem;
        margin-top: 3rem;

        @media (max-width: $breakpoint-mobile) {
            display: none;
        }
    }

    &__statistic {
        display: flex;
        flex-direction: column;
        align-items: start;

        &-number {
            font-weight: 600;
            font-size: 36px;
            line-height: 117%;
            text-align: center;
            color: #141416;

            @media (max-width: $breakpoint-tablet) {
                font-size: 26px;
                line-height: 115%;
            }
        }

        &-text {
            font-weight: 500;
            font-size: 12px;
            line-height: 133%;
            text-align: center;
            color: #848586;

            @media (max-width: $breakpoint-tablet) {
                font-size: 9px;
                line-height: 144%;
            }
        }
    }

    &__img-container {
        width: 780px;
        height: 543px;
        position: relative;

        @media (max-width: $breakpoint-tablet) {
            width: 555px;
            height: 390px;
        }
        @media (max-width: $breakpoint-mobile) {
            width: 400px;
            height: 290px;
            margin-top: 4rem;
            margin: 0 auto;
        }
    }

    &__image {
        position: absolute;
        right: 25%;
        bottom: 8%;
        opacity: 0;

        @media (max-width: $breakpoint-tablet) {
            width: 360px;
            height: 360px;
            right: 30%;
            bottom: 20%;
        }
        @media (max-width: $breakpoint-mobile) {
            width: 260px;
            height: 263px;
            left: 0%;
            top: 0%;
        }

        &.slide-in {
            animation: slideInFromRight 0.5s ease forwards;
            &--delay-1 {
                animation-delay: 0.2s;
            }
        }
    }

    &__blur {
        position: absolute;
        left: 60%;
        top: 25%;
        opacity: 0;
        @media (max-width: $breakpoint-tablet) {
            width: 321px;
            height: 320px;
            top: 30%;
            left: 54%;
        }
        @media (max-width: $breakpoint-mobile) {
            width: 210px;
            height: 220px;
            left: 53%;
        }

        &.slide-in {
            animation: slideInFromRight 0.5s ease forwards;
            &--delay-2 {
                animation-delay: 0.4s;
            }
        }
    }

    &__arrow {
        position: absolute;
        left: 67%;
        bottom: 70%;
        opacity: 0;

        @media (max-width: $breakpoint-tablet) {
            width: 90px;
            height: 90px;
            bottom: 60%;
            left: 60%;
        }
        @media (max-width: $breakpoint-mobile) {
            width: 60px;
            height: 60px;
            bottom: 63%;
            left: 58%;
        }

        &.fade-in-arrow {
            animation: fadeIn 0.5s ease forwards;
            animation-delay: 0.6s;
        }
    }

    &__background {
        position: absolute;
        left: 90%;
        bottom: 30%;
        z-index: -1;
        opacity: 0;

        @media (max-width: $breakpoint-tablet) {
            width: 124px;
            height: 300px;
            bottom: 30%;
            left: 85%;
        }
        @media (max-width: $breakpoint-mobile) {
            width: 100px;
            height: 200px;
            left: 80%;
        }

        &.fade-in-arrow {
            animation: fadeIn 0.5s ease forwards;
            animation-delay: 0.6s; // Задержка перед появлением
        }
    }

    @keyframes fadeIn {
        from {
            opacity: 0;
            transform: translateY(20px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
    @keyframes slideInFromRight {
        from {
            opacity: 0;
            transform: translateX(100px); // Начальное положение справа
        }
        to {
            opacity: 1;
            transform: translateX(0); // Конечное положение
        }
    }
        
    .fade-in {
        opacity: 0;
        animation: fadeIn 0.5s ease forwards;
        
        &--delay-1 {
            animation-delay: 0.2s;
        }
        
        &--delay-2 {
            animation-delay: 0.4s;
        }
        
        &--delay-3 {
            animation-delay: 0.6s;
        }
        
        &--delay-4 {
            animation-delay: 0.8s;
        }
    }

}
</style>