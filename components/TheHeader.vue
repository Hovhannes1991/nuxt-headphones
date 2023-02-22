<template>
    <header class="header">
        <TheHeaderNav />


        <div class="header_content">
            <div class="main_image">
                <img src="images/headphone-red.svg" alt="headphone image">
            </div>
            <div class="header_texts">
                <div class="subtitle">
                    <span>Hear it. Feel it</span>
                </div>
                <div class="title text-uppercase">
                    <h1>Move with the music</h1>
                </div>
                <div class="price">
                    <div class="current_price">
                        <span>$435</span>
                    </div>
                    <div class="line"></div>
                    <div class="main_price">
                        <span>$465</span>
                    </div>
                </div>

                <div class="buy_btn">
                    <button class="text-uppercase">Buy Now</button>
                </div>
            </div>
        </div>
    </header>
</template>

<script setup lang="ts"></script>


<style lang="scss" scoped>
header {
    width: 100%;
    height: 850px;
    background: var(--main-gradient);
    padding: 20px 0;

    .header_content {
        margin-top: 50px;
        display: flex;
        justify-content: space-between;
        padding: 0 100px;

        .header_texts {
            color: #fff;

            .title {
                h1 {
                    font-size: 6rem;
                    width: 90%;
                    overflow-wrap: break-word;
                }
            }

            .price {
                display: flex;
                align-items: center;
                gap: 25px;

                .current_price {
                    font-weight: 700;
                    font-size: 2.5rem;
                }

                .main_price {
                    font-weight: 500;
                    font-size: 2rem;
                    opacity: 0.7;
                }

                .line {
                    width: 1px;
                    height: 50px;
                    background: #fff;
                    opacity: 0.5;
                }
            }

            .buy_btn {
                button {
                    width: 190px;
                    height: 50px;
                    margin-top: 50px;
                    background-color: #fff;
                    border: none;
                    font-size: 1.4rem;
                    border-radius: 50px;
                    color: #DE5150;
                    transition: all 0.2s linear;
                    cursor: pointer;

                    &:hover {
                        width: 210px;
                        height: 70px;
                        font-size: 1.5rem;
                    }
                }
            }
        }
    }
}
</style> 
