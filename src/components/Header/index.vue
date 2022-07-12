<template>
  <header class="header">
    <div class="content">
      <div>
        <ph-wallet :size="24" color="#f0f0f0" weight="fill" />
        <h2>My wallet</h2>
      </div>
      <button type="button">Nova Transação</button>
    </div>
  </header>
</template>
<script>
import { PhWallet } from "phosphor-vue";
export default {
  name: "App",
  components: {
    PhWallet,
  },
};
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

.content button {
  font-size: 1rem;
  color: #fff;
  background: var(--green);
  border: 0;
  padding: 0 2rem;
  border-radius: 0.25rem;
  height: 3rem;

  transition: filter 0.2s;
}
.content button:hover {
  filter: brightness(0.95);
}
</style>
