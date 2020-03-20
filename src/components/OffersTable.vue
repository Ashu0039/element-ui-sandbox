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
    <el-table-column>
      <i class="el-icon-success"></i>
      <i class="el-icon-view"></i>
      <i class="el-icon-edit"></i>
      <i class="el-icon-s-data"></i>
      <el-dropdown trigger="click">
        <span class="el-dropdown-link">
          <i class="el-icon-more"></i>
        </span>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item icon="el-icon-plus">Action 1</el-dropdown-item>
          <el-dropdown-item icon="el-icon-circle-plus">Action 2</el-dropdown-item>
          <el-dropdown-item icon="el-icon-circle-plus-outline">Action 3</el-dropdown-item>
          <el-dropdown-item icon="el-icon-check">Action 4</el-dropdown-item>
          <el-dropdown-item icon="el-icon-circle-check">Action 5</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
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