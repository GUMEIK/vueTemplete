<template>
<B :visabledata="visableData" />
</template>

<script>
import B from './B'
export default {
    components: {
        B
    },
    data() {
        return {
            visableData:[{name:"gumeik"},{name:"gumeik"},{name:"gumeik"}]
        }
    },
mounted(){
setTimeout(()=>{
    this.visableData = 'pppfdfpdfjp'
},1000)
}
}
</script>
