<script>
export default {

}
</script>
<template lang="">
    <div>
        <div class="jumbotron">
            <div class="container">
                <div class="label">
                    <h3>CURRENT SERIES</h3>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    .jumbotron{
        height: 350px;
        background-image: url(../assets/img/jumbotron.jpg);
        background-size: cover;
        background-position: top;
        .container{
            position: relative;
            .label{
                color: white;
                background-color: $color-primary;
                width: fit-content;
                padding: 5px 10px;
                position: absolute;
                top: 100%;
                transform: translate(0, -50%);
            }
        }
    }
</style>