<template>
  <el-table
    :data="tableData"
  >
    <el-table-column
      prop="title"
      label="Title"
    >
    </el-table-column>
    <el-table-column
      prop="products"
      label="Products"
    >
    </el-table-column>
    <el-table-column
      prop="price"
      label="Price"
    >
    </el-table-column>
    <el-table-column
      prop="revenue"
      label="Revenue"
    >
    </el-table-column>
  </el-table>
</template>
<script>
export default {
  props: {
    tableData: {
      type: Array,
      required: true
    }
  }
}
</script>