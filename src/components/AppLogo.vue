<script>

export default{
    name: "AppLogo",
}
</script>

<template>
    <div class="m-logo">
        <span class="first-half">NEX</span>
        <span class="second-half">GEN</span>
    </div>
</template>


<style lang="scss" scoped>
@use "../assets/style/partials/variables" as *;
.m-logo{
    letter-spacing: .3rem;
    font-size: 1.5rem;
    font-weight: bold;
    .first-half{
        color: $light-acqua;
        padding: .5rem 0 .5rem 2rem;
        border-radius:20px 0 0 20px ;
        background: rgba($color: #1BABAB, $alpha: .15)
    }
    .second-half{
        color: $primary-font-white;
        padding: .5rem 2rem .5rem 0rem;

    }
}

</style>