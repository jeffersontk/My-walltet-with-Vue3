<script>
import { PhCoins } from "phosphor-vue";
export default {
  name: "Summary",
  components: {
    PhCoins,
  },
};
</script>

<template>
  <div class="summary-container">
    <div class="card-content">
      <header>
        <p>Entradas</p>
        <ph-coins :size="24" color="#33cc95" weight="fill" />
      </header>
      <strong>
        {{
          new Intl.NumberFormat("pt-BR", {
            style: "currency",
            currency: "BRL",
          }).format(5000)
        }}
      </strong>
    </div>
    <div class="card-content">
      <header>
        <p>Saídas</p>
        <ph-coins :size="24" color="#e52e4d" weight="fill" />
      </header>
      <strong>
        {{
          new Intl.NumberFormat("pt-BR", {
            style: "currency",
            currency: "BRL",
          }).format(5000)
        }}
      </strong>
    </div>
    <div class="card-content highlight-background">
      <header>
        <p>Total</p>
        <span>$</span>
      </header>
      <strong>
        {{
          new Intl.NumberFormat("pt-BR", {
            style: "currency",
            currency: "BRL",
          }).format(5000)
        }}
      </strong>
    </div>
  </div>
</template>

<style>
.summary-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-top: -8rem;
}

.card-content {
  background: var(--shape);
  padding: 1.5rem 2rem;
  border-radius: 0.25rem;
  color: var(--text-title);
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
}

.card-content header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.card-content header span {
  font-size: 1.5rem;
}
.card-content strong {
  display: block;
  margin-top: 1rem;
  font-size: 2rem;
  font-weight: 500;
  line-height: 3rem;
}

.highlight-background {
  background: var(--green);
  color: #fff;
}
</style>
