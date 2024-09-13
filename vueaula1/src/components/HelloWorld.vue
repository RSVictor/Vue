
------------------------ Exercicio aula 1-------------------

<template>
<div>
    <div>
        <h1>{{msg}}</h1>
    </div>
    <hr>
    
      <h3>{{Exercicio1}}</h3>
        <p>{{mensagem}}</p>
    
    </div>
    <hr>

    <div>
      <h3>{{Exercicio2}}</h3>
        <p>Contador:{{ contador }}</p>
         <button @click="incrementar">Clique para incrementar</button>
    
    </div>
    <hr>

    <div>
      <h3>{{Exercicio3}}</h3>
        <button @click="alternarMostrar">
            {{ mostrar ? 'Ocultar Texto' : 'Mostrar Texto' }}
         </button>
        <p v-if="mostrar">Este é o texto que pode ser mostrado ou ocultado.</p>
    </div>
    <hr>

     <div>
      <h3>{{Exercicio4}}</h3>
     <ul>
            <li v-for="(item, index) in itens" :key="index">
       
        {{ item }}
      </li>
        </ul>
      
    </div>
    <hr>

     <div>
      <h3>{{Exercicio5}}</h3>
        <input type="text" v-model="nome" placeholder="Digite seu nome" />

         <p>Nome digitado: {{ nome }}</p>
    </div>
     <hr>
     
      <div>
      <h3>{{Exercicio6}}</h3>
      

         <p class="teste">Texto para teste</p>
    </div>
</template>
 

<script>
export default {
    data(){
        return{
            msg: "Atividades aula 1",
            Exercicio1:"Exercício 1",
             mensagem: "Bem-vindo ao Vue.js",

            Exercicio2: "Exercício 2",
            contador: 0,

            Exercicio3: "Exercício 3",
            mostrar: false,

            Exercicio4: "Exercício 4",
             itens: ['Item 1', 'Item 2', 'Item 3', 'Item 4'],
                
            Exercicio5: "Exercício 5",
              nome: ''
        };
    },
    methods: {
    incrementar() {
            this.contador++;
        },
    alternarMostrar(){
        this.mostrar = !this.mostrar;
    }
    }
};
</script>

<style>
p {
    color:red;
}
 h1{
    color:black;
}

.teste{
    color: green;
}
</style>


