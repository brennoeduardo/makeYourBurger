<template>
    <div id="main-banner">
        <h1>Make Your Burger</h1>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>

#main-banner{
    background-image: url('burger.jpg');
    background-position: 0 -330px;
    background-size: cover;
    background-attachment: fixed;
    height: 600px;
    display: flex;
    align-items: center;
    justify-content: flex-start;
}

#main-banner h1{
    color: #fff;
    text-align: center;
    font-size: 60px;
    margin-left: 40px;
}

</style>