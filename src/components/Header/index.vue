<template>
  <header class="header">
    <div class="content">
      <div>
        <ph-wallet :size="24" color="#f0f0f0" weight="fill" />
        <h2>My wallet</h2>
      </div>
      <NewTransactionModal />
    </div>
  </header>
</template>
<script setup>
import { PhWallet } from "phosphor-vue";
import NewTransactionModal from "../NewTransactionModal/index.vue";
</script>
<style>
.header {
  background: var(--gray-dark);
}
.content {
  max-width: 1120px;
  margin: 0 auto;

  padding: 2rem 1rem 8rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.content div {
  display: flex;
  align-items: center;
  gap: 1rem;
}
.content div h2 {
  line-height: 1.5rem;
  color: var(--shape);
}
</style>
