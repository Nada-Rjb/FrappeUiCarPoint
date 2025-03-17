<template>
  <div class="home"></div>
  <app-search></app-search>
  <customer-info></customer-info>
  <DebtSummary></DebtSummary>
  <InvoiceActions></InvoiceActions>
  <TransactionButtons></TransactionButtons>
</template>

<script>
import AppSearch from "../components/HomePage/AppSearch.vue";
import CustomerInfo from "../components/HomePage/CustomerInfo.vue";
import DebtSummary from "../components/HomePage/DebtSummary.vue";
import InvoiceActions from "../components/HomePage/InvioceActions.vue";
import TransactionButtons from "../components/HomePage/TransactionButtons.vue";
export default {
  name: "HomeView",
  components: {
    AppSearch,
    CustomerInfo,
    DebtSummary,
    InvoiceActions,
    TransactionButtons,
  },
};
</script>