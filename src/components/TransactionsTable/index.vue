<script>
export default {};
</script>
<template>
  <div class="table-container">
    <table>
      <thead>
        <tr>
          <th>Titulo</th>
          <th>Valor</th>
          <th>Categoria</th>
          <th>Data</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>salário</td>
          <td class="deposit">
            {{
              new Intl.NumberFormat("pt-BR", {
                style: "currency",
                currency: "BRL",
              }).format(5000)
            }}
          </td>
          <td>trabalho</td>
          <td>25/07/2022</td>
        </tr>
        <tr>
          <td>aluguel</td>
          <td class="withdraw">
            {{
              new Intl.NumberFormat("pt-BR", {
                style: "currency",
                currency: "BRL",
              }).format(1830)
            }}
          </td>
          <td>trabalho</td>
          <td>25/07/2022</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style>
.table-container {
  margin-top: 4rem;
}

table {
  width: 100%;
  border-spacing: 0 0.5rem;
}

th {
  color: var(--text-title);
  font-weight: 400;
  padding: 1rem 2rem;
  text-align: left;
  line-height: 1.5rem;
}

td {
  padding: 1rem 2rem;
  border: 0;
  background: var(--shape);
  color: var(--text-body);
  border-radius: 0.25rem;
}

td:first-child {
  color: var(--text-title);
}

.deposit {
  color: var(--green);
}

.withdraw {
  color: var(--red);
}
</style>
