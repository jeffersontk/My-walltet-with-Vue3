<script setup>
import Summary from "../Summary/index.vue";
import TransactionsTable from "../TransactionsTable/index.vue";
</script>

<template>
  <main class="container">
    <Summary />
    <TransactionsTable />
  </main>
</template>

<style>
.container {
  max-width: 1120px;
  margin: 0 auto;
  padding: 2.5rem 1rem;
}
</style>
