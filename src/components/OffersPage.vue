<template>
  <div>
    <h1>Offers</h1>
    <el-row :gutter="12">
      <el-col :span="3">
        <i class="el-icon-s-ticket"></i>&nbsp;Coupons
      </el-col>
      <el-col :span="3">
        <i class="el-icon-bank-card"></i>&nbsp;Payments
      </el-col>
      <el-col :span="3">
        <i class="el-icon-s-platform"></i>&nbsp;Sales Pages
      </el-col>
    </el-row>
    <el-card class="offer-stats">
      <el-row :gutter="20">
        <el-col :span="8">
          <h3>0</h3>
          <h6>Purchases</h6>
          <p>Last 30 days</p>
        </el-col>
        <el-col :span="8">
          <h3>$0</h3>
          <h6>Net Revenue</h6>
          <p>Last 30 days</p>
        </el-col>
        <el-col :span="8">
          <h3>$0</h3>
          <h6>Net Revenue</h6>
          <p>All Time</p>
        </el-col>
      </el-row>
    </el-card>
    <el-card class="offers-list">
      <el-tabs v-model="activeTab" @tab-click="tabClicked">
        <el-tab-pane label="Published" name="published">
          <el-input placeholder="Search Offers" v-model="searchOffers"></el-input>
          <offers-table :tableData="publishedOffers" />
        </el-tab-pane>
        <el-tab-pane label="Drafts" name="drafts">
          <el-input placeholder="Search Offers" v-model="searchOffers"></el-input>
          <offers-table :tableData="draftOffers" />
        </el-tab-pane>
      </el-tabs>
    </el-card>
  </div>
</template>
<script>
import OffersTable from './OffersTable.vue'

export default {
  components: {
    OffersTable
  },
  data() {
    const publishedOffers = [
      {
        id: 1,
        title: 'Internal Title',
        products: 1,
        price: 'Free',
        revenue: '0.00'
      },
      {
        id: 2,
        title: 'Product 2',
        products: 1,
        price: 'Free',
        revenue: '0.00'
      },
      {
        id: 3,
        title: 'Product 3',
        products: 1,
        price: 'Free',
        revenue: '0.00'
      },
      {
        id: 4,
        title: 'Product 4',
        products: 0,
        price: 'Free',
        revenue: '3.00'
      },
      {
        id: 5,
        title: 'Product 5',
        products: 0,
        price: 'Free',
        revenue: '0.00'
      }
    ]

    const draftOffers = [
      {
        id: 1,
        title: 'Product 1',
        products: 1,
        price: 'Free',
        revenue: '0.00'
      },
      {
        id: 2,
        title: 'Product 2',
        products: 1,
        price: 'Free',
        revenue: '0.00'
      },
      {
        id: 3,
        title: 'Product 3',
        products: 1,
        price: 'Free',
        revenue: '0.00'
      }
    ]

    return {
      activeTab: 'published',
      searchOffers: '',
      publishedOffers,
      draftOffers
    }
  },
  methods: {
    tabClicked(tab, event) {
      console.log('tab clicked --> ', tab, event)
    }
  }
}
</script>
<style scoped>
.el-card {
  margin: 24px 0;
}
.el-col {
  text-align: center;
}
</style>