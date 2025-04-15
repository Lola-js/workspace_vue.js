<template>
    <section>
        <h3>Añadir nuevo profesor:</h3>
        <div>
            <label>Nombre:</label>
            <input type="text" v-model="teacher.teachersName" />
        </div>

        <div>
            <label>Apellidos:</label>
            <input type="text" v-model="teacher.teachersSurname" />
        </div>

        <div>
            <label>DNI/NIE:</label>
            <input type="text" v-model="teacher.teachersDni"/>
        </div>

        <div>
            <label>Materias que imparte:</label>
            <input type="text" v-model="subject"/> 
            <button @click="AddSubject()">Agregar</button>
        </div>

        <div>
            <ul>
                <li v-for="(asig, index) in teacher.subjects" :key="index"> {{ asig }}</li>
            </ul>
        </div>
        <input type="checkbox" v-model="teacher.doc"/> Documentación entregada
        <button @click="AddTeacher()">Agregar profesor</button>
    </section>

        <h3>Lista de profesorado</h3>
            <table>
            <tr>
                <th>Nombre</th>
                <th>Apellidos</th>
                <th>DNI</th>
                <th>Materias</th>
                <th>Documentación entregada</th>
            </tr>
            <tr v-for="asig in teachers" :key="asig.teachersDni">
                <th>{{ asig.teachersName }}</th>
                <th>{{ asig.teachersSurname }}</th>
                <th>{{ asig.teachersDni }}</th>
                <th>
                    <ul>
                        <li v-for="(asig, index) in asig.subjects" :key="index">{{ asig }}</li>
                    </ul>
                </th>
                <th v-if="asig.doc">Documentación entregada</th>
                <th v-else>Documentación no entregada</th>
            </tr>
            </table>
</template>

<script setup>
import { ref } from 'vue'

let teacher = ref({

    teachersName:'',
    teachersSurname:'',
    teachersDni:'',
    subjects: [], //Array para las asignaturas
    doc: false //checkbox con docu
})

    //Array para guardar profe + asignaturas
    let teachers=ref([])
    let subject =ref('')

    const AddSubject = () =>{
        teacher.value.subjects.push(subject.value)
        subject.value=''
    }
//nuevo objeto para 
    const AddTeacher = () => {
        teachers.value.push({
            teachersName: teacher.value.teachersName,
            teachersSurname: teacher.value.teachersSurname,
            teachersDni:teacher.value.teachersDni,
            subjects:teacher.value.subjects,
            doc:teacher.value.doc
        })
        teacher.value.teachersName= ""
        teacher.value.teachersSurname= ""
        teacher.value.teachersDni= ""
        teacher.value.subjects = []
        teacher.value.doc = false
    }

</script>

<style scoped>

</style>