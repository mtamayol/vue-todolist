<template>
    <div id="app">
        <h1>Crear una nueva tarea</h1>
        Tarea: <input type="text" id="inputTarea" />
        <button @click="agregarTarea">Crear</button>

        <ul>
            <li v-for="(tarea,index) in listaTareas">
                {{ index+1 }} : {{ tarea }}
            </li>
         </ul>
</div>
</template>
<script>
        export default {
        data() {
		    return {
                listaTareas: []
		    }
	    },
        
        methods: {
            agregarTarea() {
                    let tarea = $("#inputTarea").val();
                    this.listaTareas.push(tarea);
            }
        }
    };
</script>
<style>
    #app {
        font-size: 25px;
        font-family: 'Calibri', sans-serif;
        color: darkblue;
        background: lightblue;
    }
</style>