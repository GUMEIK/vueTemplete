<template>
<div>
    {{visabledata}}
</div>
</template>

<script>
export default {
    props: ["visabledata"],
    mounted() {
        // setTimeout(function(){
        console.log(this.visabledata)
        // },1000)
    },
    watch: {
        visabledata(newValue, oldValue) {
            console.log(newValue, oldValue)
            // console.log("visable数据发生变化了")
            this.visabledata = newValue;
// 重新渲染
        }
    }
}
</script>
