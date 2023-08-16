<template>
    <div>
        <a>
            <span>Telegram</span>
            <img src="../assets/link.png"/>
        </a>
    </div>
</template>

<script>
export default {
    name: "PartnerLink",
};
</script>

<style scoped>
    a {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 5px;
        font-size: 16px;
        color: black;
        text-transform: uppercase;
    }

    img{
        height: 16px;
        width: auto;
    }
</style>