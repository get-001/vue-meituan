<template>
    <div class="CenterWrap">
        <div class="CenterBox">
            <slot />
        </div>
    </div>
</template>

<style lang="less">
    .CenterWrap{
        .CenterBox{
            position: relative;
            margin: 0 auto;
            max-width: 1190px;
        }
    }
</style>