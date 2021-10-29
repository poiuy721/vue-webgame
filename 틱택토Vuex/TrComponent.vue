<template>
<tr>
    <td-component v-for="(cellData,index) in rowData" :key="index" :cell-index="index" :row-index="rowIndex"></td-component>
</tr>
</template>
<script>
import TdComponent from './TdComponent.vue'
export default {
    computed:{
        rowData(){
            return this.$store.state.tableData[this.rowIndex];
        }
    },
    props:{
        rowIndex:Number
    },
    components:{
        TdComponent
    }
}
</script>