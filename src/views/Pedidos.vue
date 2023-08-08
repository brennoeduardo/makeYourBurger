<template>
    <h1>Pedidos</h1>
    <div class="pedidos-container">
        <div class="pedido-container" v-for="pedido in pedidos" :key="pedido.id">
            <div class="pedido-header">
                <h2>{{ pedido.nome }}</h2>
                <h3>{{ pedido.status }}</h3>
            </div>
            <div class="pedido-body">
                <p>Pão: {{ pedido.pao }}</p>
                <p>Carne: {{ pedido.carne }}</p>
                <p>Opcionais: {{ pedido.opcionais }}</p>
                <p>Observações: {{ pedido.obs }}</p>
            </div>
            <div class="pedido-footer">
                <button class="btn" @click="updateStatus(pedido.id, 'Pronto')">Pronto</button>
                <button class="btn" @click="updateStatus(pedido.id, 'Entregue')">Entregue</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Pedidos',

    data() {
        return {
            pedidos: null
        }
    },

    methods: {
        async getPedidos() {
            const res = await fetch('http://localhost:3000/burgers')
            const data = await res.json()
            this.pedidos = data
            console.log(this.pedidos)
        },
    },
    mounted() {
        this.getPedidos()
    }}
</script>

<style></style>