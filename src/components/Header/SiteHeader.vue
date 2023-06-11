<template>
        <header>
            <div class="left-side">
                <img src="@/assets/img/logo.svg" alt="">
                <ul class="header_list">
                    <a href=""><li>Доставка питания</li></a>
                    <a href=""><li>Обратная связь</li></a>
                </ul>
            </div>
            <support-button></support-button>
        </header>
</template>

<script>  
    import SupportButton from "./SupportButton.vue"

    export default {
        components: {
            SupportButton
        }
    }
</script>

<style lang="scss">
    a {
        text-decoration: none;
    }
    
    header {
        width: 1720px;
        margin: 0 auto;
        margin-top: 40px;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .left-side {
            display: flex;
            width: 576px;
            justify-content: space-between;
            align-items: center;

            ul {
                width: 330px;
                display: flex;
                justify-content: space-between;


                li {
                    font-family: 'Roboto';
                    font-style: normal;
                    font-weight: 700;
                    font-size: 18px;
                    line-height: 21px;
                    color: #303030;
                    list-style: none;
                }
            }
        }
    }
</style>