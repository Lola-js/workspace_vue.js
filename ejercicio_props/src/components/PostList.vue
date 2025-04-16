<template>
    <div class="post_container">
        <PostDetail v-for="elm in info" 
        :key="elm.title" 
        :title="elm.title" 
        :autor="elm.autor" 
        :description="elm.description" 
        :imagen="elm.imagen"
        />
    </div>
</template>

<script>
    import PostDetail from './PostDetail.vue'
    import imagenLibro1 from '../assets/img_libro1.png'
    import imagenLibro2 from '../assets/img_libro2.png'
    import imagenLibro3 from '../assets/img_libro3.png'
    import imagenLibro4 from '../assets/img_libro4.png'
    import imagenLibro5 from '../assets/img_libro5.png'

    export default{
        name: 'PostList',
        components: {
            PostDetail
        },
    data(){
        return {
            info:  [
    {title: "La sombra del viento", autor: "Carlos Ruiz Safón",
    description: "Ambientada en la Barcelona de la primera mitad del siglo XX, La sombra del viento es el inicio de una saga llena de misterio, que tiene como principal protagonista a Daniel Sempere, un personaje que comienza como un niño en la primera novela y evoluciona a lo largo de los cuatro libros que componen la saga.'Cada libro, cada volumen que ves, tiene un alma. El alma de la persona que lo escribió y el alma de quienes lo leen y lo viven. Y, cuando lo abres por primera vez, el libro le habla al alma.'",
    imagen: imagenLibro1},
    {title:"El día que Selma soñó con un Okapi", autor:"Mariana Leky", 
    description: "Todo el mundo en Westerwald sabe que Selma tiene un don especial: cuando sueña con un okapi alguien fallece en veinticuatro horas. El día que se hace realidad la premonición que todos temen, las verdades acalladas y las cartas iniciadas con nunca y siempre comienzan a circular, y su sueño cambia irreversiblemente las vidas de Luise, su nieta; de Martin, el niño levantador de pesas; del óptico enamorado; de la triste Marlies e, incluso, la de un peculiar monje budista.",
    imagen: imagenLibro2},
    {title:"La chica salvaje", autor: "Delia Owens", description: "La Chica Salvaje han perturbado la vida de la pequeña localidad de Barkley Cove, un tranquilo pueblo de pescadores en Carolina del Norte. Abandonada a los seis años, Kya es una joven sensible, inteligente y de una belleza insólita que ha sobrevivido en soledad en las marismas, con la naturaleza como única amiga. Es una superviviente nata. Su solitaria vida se complica cuando un hombre aparece asesinado en el pantano y la acusan del crimen. Entonces, todos sus misterios saldrán a la luz.",
    imagen: imagenLibro3},
    {title:"La casa de los espíritus", autor: "Isabel Allende", 
    description:"El despótico patriarca Esteban Trueba ha construido con mano de hierro un imperio privado que empieza a tambalearse con el paso del tiempo y un entorno social explosivo. Finalmente, la decadencia personal del patriarca arrastrará a los Trueba a una dolorosa desintegración. Atrapados en unas dramáticas relaciones familiares, los personajes de esta poderosa novela encarnan las tensiones sociales y espirituales de una epoca que abarca gran parte del siglo XX.",
    imagen: imagenLibro4},
    {title:"La verdad sobre Harry Quebert", autor: "Joel Dicker",
    description:"En 2008, Marcus Goldman, un joven escritor, visita a su mentor -Harry Quebert, autor de una aclamada novela- y descubre que éste tuvo una relación secreta con Nola Kellergan. Poco después, Harry es arrestado y acusado de asesinato al encontrarse el cadáver de Nola enterrado en su jardín. 'El secreto de una buena novela no es lo que se cuenta, sino cómo se cuenta.'",
    imagen: imagenLibro5},
    ]
        }
    }
}
</script>



<style scoped>
.post_container {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    justify-content: center;
    gap: 10px;
    padding: 10px;
    background-color: #f9f9f9;
    border-radius: 5px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}



</style>