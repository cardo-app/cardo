<template>
<div>
    <h1>DWOPDOUWN</h1>
    <div  v-for="game in games">
        <h1>{{game}}</h1>
    </div>
</div>
</template>

<script>
export default {
    name: "DropDown",
    props: ["games"]

}
</script>

<style>

</style>