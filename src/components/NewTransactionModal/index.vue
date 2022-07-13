<script setup>
import { PhArrowUp } from "phosphor-vue";
import { PhArrowDown } from "phosphor-vue";
import { ref } from "vue";

const showModal = ref(false);
const type = ref("deposit");

function toggleModal() {
  showModal.value = !showModal.value;
}
function toggleColor(value) {
  type.value = value;
}
</script>

<template>
  <button class="btn-open" type="button" @click="toggleModal">Nova Transação</button>
  <div class="modal-overlay" v-show="showModal">
    <div class="modal">
      <button class="modal-close" @click="toggleModal">X</button>
      <form class="modal-form">
        <h2 class="modal-title">Cadastrar nova Transação</h2>
        <input placeholder="Titulo" />
        <input type="number" placeholder="Valor" />
        <div class="transaction-type">
          <button
            type="button"
            @click="toggleColor('deposit')"
            :class="type === 'deposit' ? 'deposit' : 'transparent'"
          >
            <ph-arrow-up :size="24" color="#33cc95" weight="fill" />
            <span>Entrada</span>
          </button>
          <button
            type="button"
            @click="toggleColor('withdraw')"
            :class="type === 'withdraw' ? 'withdraw' : 'transparent'"
          >
            <ph-arrow-down :size="24" color="#e52e4d" weight="fill" />
            <span>Saida</span>
          </button>
        </div>
        <input placeholder="Categoria" />

        <button type="submit">Cadastrar</button>
      </form>
    </div>
  </div>
</template>

<style>
.btn-open {
  font-size: 1rem;
  color: #fff;
  background: var(--green);
  border: 0;
  padding: 0 2rem;
  border-radius: 0.25rem;
  height: 3rem;

  transition: filter 0.2s;
}
.btn-open:hover {
  filter: brightness(0.95);
}
.modal-overlay {
  background: rgba(0, 0, 0, 0.5);

  position: fixed;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  z-index: 99;
  display: flex;
  align-items: center;
  justify-content: center;
}
.modal {
  width: 100%;
  max-width: 580px;
  background: var(--background);
  padding: 3rem;
  position: relative;
  border-radius: 0.5rem;
}

.modal-close {
  position: absolute;
  right: 1.5rem;
  top: 1.5rem;
  border: 0;
  background: transparent;

  transition: filter 0.2s;
}
.modal-close:hover {
  filter: brightness(0.7);
}
.modal-title {
  color: var(--text-title) !important;
  font-size: 1.5rem;
  margin-bottom: 2rem;
}
.modal-form input {
  width: 100%;
  padding: 0 1.5rem;
  height: 4rem;
  border: 0.25rem;

  border: 1px solid #d7d7d7;
  background: #e7e9ee;

  font-weight: 400;
  font-size: 1rem;
}
.modal-form input::placeholder {
  color: var(--text-body) !important;
}
.modal-form input + input {
  margin-top: 1rem;
}
.modal-form button[type="submit"] {
  width: 100%;
  padding: 0 1.5rem;
  height: 4rem;
  background: var(--green);
  color: #fff;
  border-radius: 0.25rem;
  border: 0;
  font-size: 1rem;
  margin-top: 1.5rem;
  font-weight: 600;

  transition: filter 0.2;

  &:hover {
    filter: brightness(0.95);
  }
}
.transaction-type {
  display: grid !important;
  grid-template-columns: 1fr 1fr;
  gap: 0.5rem !important;
  margin: 1rem 0;
}
.transaction-type button {
  height: 4rem;
  border: 1px solid #d7d7d7;
  border-radius: 0.25rem;
  display: flex;
  align-items: center;
  justify-content: center;

  transition: border-color 0.2s;
}
.transaction-type button:hover {
  border-color: rgba(215, 215, 215, 0.9);
}

.transaction-type button span {
  display: inline-block;
  margin-left: 0.25rem;
  font-size: 1rem;
  color: var(--text-title) !important;
}
.transparent {
  background: transparent;
}

.transaction-type .deposit {
  background: rgba(51, 204, 149, 0.2);
}
.transaction-type .withdraw {
  background: rgba(229, 46, 77, 0.2);
}
</style>
