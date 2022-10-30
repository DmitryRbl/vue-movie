<template>
    <div class="fullDate">
        {{localDate}}
    </div>
</template>

<script>

// import { computed } from '@vue/reactivity';

export default {
    name: "nav111",
    data() {
        return {
            date: new Date().getSeconds(),
        };
    },
    computed: {
        localDate() {
            return this.date;
        },
    },
    created() {
        this.intervalId = setInterval(() => this.date = new Date().getSeconds(), 1000); // Обновляем значения не чаще раза в секунду. А то и реже.
    },

    // Если повесили таймер, то его нужно отключать
    beforeDestroy() {
        if (this.intervalId) clearInterval(this.intervalId)
    },
    
};


</script>

<!-- <style scoped>

</style> -->