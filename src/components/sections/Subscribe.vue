<template>
    <div class="backsub">
        <div class="container text-center">
            <h2>Subscribe & Receive A Free eBook</h2>
            <p>Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.</p>
            <input type="email" placeholder="Insert your email ...*">
            <button>SUBSCRIBE</button>
            <span>Cras porttitor pellentesque sem eu pretium.</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Subscribe',
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';

.backsub {
    background-image: url('../../assets/img/subscribe-sec-bg.png');
    background-size: cover;
    background-position: center;
    background-color: #fff;
    height: 550px;

    .container {
        max-width: 760px;
        position: relative;
        top: 50%;
        transform: translateY(-50%);
        h2 {
            font-size: 40px;
            margin-bottom: 30px;
        }
        p{
            color: #afafaf;
            margin-bottom: 50px;
        }
        input {
            width: 450px;
            line-height: 50px;
            border: solid 1px #afafaf;
            border-radius: 5px;
            padding: 0 20px;
            margin-right: 20px;
        }
        button {
            color: #fff;
            border: none;
            border-radius: 2px;
            background-color: $mainColor;
            line-height: 50px;
            font-weight: bold;
            padding: 0 60px;
            margin-bottom: 50px;
        }
        input[type=email]:hover {
            border: 1px solid $mainColor;
        }
        input[type=email]:focus {
            border: solid 1px $mainColor;
        }
        button:hover {
            filter: brightness(0.9);
        }
        span {
            display: inline-block;
        }
    }
}
</style>