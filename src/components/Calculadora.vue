<script setup>
    const props = defineProps(["getValor1", "getValor2", "getCalculo", "resultado"]);
</script>

<template>
    <div class="row p-4 mb-3 mt-3 rounded-3">
        <div class="col-md-11 ms-5">
            <h3>Insira o valor que deseja utilizar na operação aritmética.</h3>
            <input required type="number" placeholder="0" class="form-control mb-4" @keyup="props.getValor1"/>
        </div>
    </div>

    <div class="row p-4 mb-3 mt-3 rounded-3">
        <div class="col-md-11 ms-5">
            <h3>Escolha a Operação Aritmética</h3>
            <select class="form-control text-center" @change="props.getCalculo">
                <option class="subtrair text-center" value="subtrair">-</option>
                <option class="somar text-center" selected value="somar">+</option>
                <option class="dividir text-center" value="dividir">÷</option>
                <option class="multiplicar text-center" value="multiplicar">x</option>
            </select>
        </div>
    </div>

    <div class="row p-4 mb-3 mt-3 rounded-3">
        <div class="col-md-11 ms-5">
            <h3>Informe o segundo valor</h3>
            <input required type="number" placeholder="0" class="form-control mb-4" @keyup="props.getValor2"/>
            <div class="col text-center">
            <h3>Resultado:</h3>
            </div>
            <div class="col text-center">
            <h2 class="fs-1 fw-bold ps-2 mb-2">{{ props.resultado }}</h2>
            </div>
        </div>
    </div>
</template>

<style scoped>
.row {
    background-color: rgb(196, 168, 162);
    align-items: center;
}

h2, h3, p {
    font-family: "Roboto", sans-serif;
    font-weight: 400;
    font-style: normal;
}

    .black-text {
        color: black;
    }

    input[type=number]::-webkit-inner-spin-button,
    input[type=number]::-webkit-outer-spin-button {
        -webkit-appearance: none;
        margin: 0;
}

@media screen and (max-width: 768px) {
    .form-control {
        text-align: center;
    }

    select {
        padding-left: 48%;
        padding-right: 48%;
    }
}
</style>