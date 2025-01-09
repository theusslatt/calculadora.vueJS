<script setup>
const props = defineProps(["valorNumero1", "valorNumero2", "trocarFiltro"]);
</script>

<template>
    <form>
        <div class="row d-flex align-items-center">
            <div class="col gap-2 d-flex">
                <input @keyup="props.valorNumero1" class="form-control" type="number" />
                <input @keyup="props.valorNumero2" class="form-control" type="number" />
            </div>
            <div class="col">
                <select @change="props.trocarFiltro" class="form-control text-center">
                    <option value="multiplicacao">Multiplicação</option>
                    <option value="adicao">Adição</option>
                    <option value="subtracao">Subtração</option>
                    <option value="divisao">Divisão</option>
                </select>
            </div>
        </div>
    </form>
</template>