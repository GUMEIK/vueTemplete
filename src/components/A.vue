<template>
<div>
    <B :visabledata="visableData" />
    {{name}}
    <button @click="handleClick">change</button>
</div>
</template>

<script>
import B from './B'
import { mapState } from 'vuex' //辅助函数，帮助生成计算属性
export default {
    components: {
        B
    },
    data() {
        return {
            visableData: [{ name: "gumeik" }, { name: "gumeik" }, { name: "gumeik" }]
        }
    },
    methods: {
        handleClick() {
            this.$store.state.info.name = 'changeName'
        }
    },
    mounted() {
        console.log(this.$store.state.info)
        setTimeout(() => {
            this.visableData = 'pppfdfpdfjp'
        }, 1000)
    },
    // computed: {
    //     name() {
    //         return this.$store.state.info.name
    //     }
    // }
    computed: mapState({
        name(state) {
            return state.info.name
        }

    })
}
</script>
