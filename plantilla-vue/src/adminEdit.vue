<template>

    <div>

        <md-tabs md-sync-route class="md-transparent" md-alignment="fixed">
            <md-tab id="tab-home" md-label="Editar encuestas" to="/components/tabs/home">
                <div>


                <md-card>
                    <md-card-header class="md-title">A continuación modifique el nombre de la empresa sobre la que desea encuestar:</md-card-header>
                    <md-card-media style="margin: inherit">
                        <md-field>
                            <label>Ingrese el nombre aquí:</label>
                            <md-textarea v-model="empresa" md-autogrow></md-textarea>
                        </md-field>
                        <md-button v-on:click="modificarEmpresa">Guardar</md-button>
                    </md-card-media>
                </md-card>

                    <div v-if="submitted">
                        <div class="isa_success">
                            <i class="fa fa-check"></i>
                            La empresa ha sido añadida exitosamente
                        </div>
                    </div>

                    <div v-if="errorsub">
                        <div class="isa_error">
                            <i class="fa fa-times"></i>
                            No se pudo añadir la empresa, pruebe recargando la página.
                        </div>
                    </div>

                </div>
            </md-tab>


        <md-tab id="tab-posts" md-label="Estadísticas por Empresa" to="/components/tabs/posts">
            <div>
                <md-card>

                    <md-card-header>
                        <div class="md-title"> Usuarios del sistema: </div>
                    </md-card-header>

                    <md-card-media>
                        <md-table style="width: 100%; height: 50%">

                            <md-table-row>
                                <md-table-head>N°</md-table-head>
                                <md-table-head md-numeric >Nombre</md-table-head>
                                <md-table-head md-numeric >Correo</md-table-head>
                                <md-table-head md-numeric>Activo</md-table-head>
                                <md-table-head md-numeric>Rol</md-table-head>
                            </md-table-row>
                            <md-table-row v-for="(usuario, z) in this.dataUsuarios">
                                <md-table-cell >{{z}}</md-table-cell>
                                <md-table-cell>{{usuario.nombre}}</md-table-cell>
                                <md-table-cell>{{usuario.correo}}</md-table-cell>
                                <md-table-cell>{{usuario.activo}}</md-table-cell>
                                <md-table-cell>{{usuario.rol}}</md-table-cell>

                            </md-table-row>

                        </md-table>
                    </md-card-media>

                </md-card>

                <md-card style="height: 100%; width: 50%; float: right;">
                    <md-card-header>
                        <div class="md-title"> Busca un usuario específico: </div>
                    </md-card-header>
                    <md-card-media style="margin: inherit">
                        <label>Buscar por el nombre:</label>
                        <br>
                        <md-field>
                            <label>Escriba el nombre del usuario</label>
                            <md-textarea v-model="buscarNom"></md-textarea>
                        </md-field>
                        <md-button v-on:click="buscarPorNom" class="md-raised">Buscar</md-button>
                        <div v-if="mostrarNom == null">
                        </div>
                        <div class="center" v-else>
                            <md-card  v-for="user in mostrarNom">
                                <label>Nombre: {{user.nombre}}</label><br>
                                <label>Correo: {{user.correo}}</label><br>
                                <label>Rol: {{user.rol}}</label>
                            </md-card>
                        </div>
                        <hr>
                        <label>Buscar por el correo:</label>
                        <md-field>
                            <label>Escriba el correo del usuario</label>
                            <md-textarea v-model="buscarCorr"></md-textarea>
                        </md-field>
                        <md-button v-on:click="buscarPorCorr" class="md-raised">Buscar</md-button>
                        <div v-if="mostrarCorr == null">
                        </div>
                        <div class="center" v-else>
                            <md-card  v-for="correo in mostrarCorr">
                                <label>Nombre: {{correo.nombre}}</label><br>
                                <label>Correo: {{correo.correo}}</label><br>
                                <label>Rol: {{correo.rol}}</label>
                            </md-card>
                        </div>


                    </md-card-media>
                </md-card>

            </div>
        </md-tab>

        <md-tab id="tab-favorites" md-label="Añadir Categoria" to="/components/tabs/favorites">
            <div>
                <md-card style="width: 100%; height: 100%; float: none">
                    <md-card-header>
                        <div class="md-title"> Añadir categoría: </div>
                    </md-card-header>
                    <br>
                    <hr>
                    <md-card-media  style="margin: inherit">
                        <label>Nombre:</label>
                        <md-field>
                            <label>Ingrese el nombre de la categoría</label>
                            <md-textarea v-model="nombreCategoria" md-autogrow></md-textarea>
                        </md-field>
                        <br>

                        <hr>
                        <label>Descripción:</label>
                        <md-field>
                            <label>Escriba una pequeña descripcion para la categoría</label>
                            <md-textarea v-model="description"></md-textarea>
                        </md-field>
                        <br>
                        <hr>
                        <md-checkbox v-model="opcionCategoria" value="1">Crear preguntas por escala</md-checkbox>
                        <md-checkbox v-model="opcionCategoria" value="2">Crear preguntas con opciones</md-checkbox>
                        <!-- escalas -->
                        <div v-if="opcionCategoria == 1">
                            <label>Cantidad de preguntas:</label>
                            <md-field>
                                <md-select name="cantPreguntas" id="cantPreguntas" v-model="cantPreguntasEscala">
                                    <md-option value="1">1</md-option>
                                    <md-option value="12">2</md-option>
                                    <md-option value="123">3</md-option>
                                    <md-option value="1234">4</md-option>
                                    <md-option value="12345">5</md-option>
                                </md-select>
                            </md-field>
                            <hr>
                            <div v-for="i in this.cantPreguntasEscala" >
                                <br>
                                <label>Pregunta {{i}}:</label>
                                <md-field>
                                    <label>Ingrese la pregunta que desea realizar</label>
                                    <md-textarea :id=i v-model="preguntasEscala[i]" md-autogrow></md-textarea>
                                </md-field>
                                {{preguntasEscala}}
                                <br>
                                <label>Escala:</label>
                                <md-field>
                                    <md-radio v-model="escalas" value="1"><label>1</label></md-radio>
                                    <md-radio v-model="escalas" value="2"><label>2</label></md-radio>
                                    <md-radio v-model="escalas" value="3"><label>3</label></md-radio>
                                    <md-radio v-model="escalas" value="4"><label>4</label></md-radio>
                                    <md-radio v-model="escalas" value="5"><label>5</label></md-radio>
                                    <md-radio v-model="escalas" value="6"><label>6</label></md-radio>
                                    <md-radio v-model="escalas" value="7"><label>7</label></md-radio>
                                </md-field>
                            </div>
                        </div>

                        <!-- opciones -->
                        <div v-if="opcionCategoria == 2">
                            <label>Cantidad de preguntas:</label>
                            <md-field>
                                <md-select name="cantPreguntas" id="cantPreguntas" v-model="cantPreguntas">
                                    <md-option value="1">1</md-option>
                                    <md-option value="12">2</md-option>
                                    <md-option value="123">3</md-option>
                                    <md-option value="1234">4</md-option>
                                    <md-option value="12345">5</md-option>
                                </md-select>
                            </md-field>
                            <hr>
                            {{this.cantPreguntas}} cantidadad preguntas
                            <div v-for="i in this.cantPreguntas" >
                                <br>
                                <label>Pregunta {{i}}:</label>
                                <md-field>
                                    <label>Ingrese la pregunta que desea realizar</label>
                                    <md-textarea :id=i v-model="preguntaCate[i]" md-autogrow></md-textarea>
                                </md-field>
                                {{preguntaCate}}
                                <br>
                                <label>Escala:</label>
                                <md-field>
                                    <label>Ingrese la escala con que desea evaluar la pregunta</label>
                                    <md-textarea :id=i v-model="opciones[i]" md-autogrow></md-textarea>
                                </md-field>
                                <hr>
                            </div>
                        </div>

                        <md-button v-on:click="crearJSON" class="md-raised">Aceptar</md-button>
                    </md-card-media>
                </md-card>
            </div>
        </md-tab>

        <md-tab id="tab-preguntas" md-label="Eliminar Preguntas" to="/components/tabs/preguntas">

            <md-card style="width:30%; float: left">
                <md-card-header>
                    <div class="md-title"> Categorías: </div>
                </md-card-header>
                <md-card-media style="margin: inherit;">
                <div v-for="categoria in dataPreguntas">
                    <label>-Numeración de la categoría: {{categoria.ID}}<br>
                        -Nombre de la categoría: {{categoria.nombre}}<br>
                        <md-button :value=categoria.ID class="md-raised md-accent">Eliminar</md-button> </label>
                    <hr>
                </div>
                </md-card-media>
            </md-card>
            <md-card style="width: 68%; float: right">
                <md-card-header>
                    <div class="md-title"> Edición de categorías: </div>
                </md-card-header>
                <md-card-media style="margin: inherit">
                <br>
                <label>Seleccione la categoría que desea editar:</label>
                <select>
                    <option  v-for="(elemento, i) in dataPreguntas">
                        {{elemento.nombre}}</option>
                </select>
                <br>
                <br>
                <hr>
                <div>
                    <label>Modifique el nombre de la categoria:</label>
                    <md-field>
                        <label>Nuevo nombre de la categoría</label>
                        <md-textarea v-model="nuevoNombre" md-autogrow></md-textarea>
                    </md-field>
                    <hr>
                    <label>Modifique la descripcion de la categoria:</label>
                    <md-field>
                        <label>Nueva descripción de la categoría</label>
                        <md-textarea v-model="nuevaDescripcion" md-autogrow></md-textarea>
                    </md-field>
                </div>
                </md-card-media>
            </md-card>

        </md-tab>
        </md-tabs>

    </div>



</template>

<script>
    export default {
        props: ['datos'],
        name: "adminEdit",

        data: () => ({

            /*Data del bind*/
            dataUsuarios: null,
            dataPreguntas: null,


            empresa: null,
            submitted: false,
            errorsub: null,

                         buscarCorr: null,
                         buscarNom: null,
                         mostrarCorr: [],
                         mostrarNom: [],


            /* variables para armar json */
            nombreCategoria: null,
            description: null,

            cantPreguntasEscala: null, //cantidad de preguntas de escala
            escalas: null, //numero maximo de escala
            preguntasEscala: [], //arreglo con todas las preguntas la primera es nula
            listaEscala:[], //lista con los elemementos de la escala

            opciones: [],
            cantPreguntas2: null,
            preguntaCate: [],
            opcionCategoria: null
                     }),

        created() {

            this.dataUsuarios = this.datos[0];
            this.dataPreguntas = this.datos[1];
            this.buscarPorNom();
            this.buscarPorCorr();


        },
        methods : {

            modificarEmpresa(){

                let roleAdmin ={
                    headers: {'Authorization':'Bearer ' + 'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250cmFzZW5hIjoiYXNkZiIsInJvbCI6MSwiY29ycmVvIjoiYWRtaW5AbWFpbC5jbCIsImFjdGl2byI6dHJ1ZX0.TrVdJeaJ5km92RKv2hI0yot8gWwtON3azO1qPvfdjZ0'}
                };

                this.$http.put('http://134.209.49.245:8080/mongodb-v1/categories/updateEmpresa/' + this.empresa, this.empresa ,roleAdmin).then((response) => {
                    console.log("Hice el put de empresa")
                    this.submitted = true;
                }, (response) => {
                    this.error = false;
                    console.log("Fallo servicio, put de empresa")
                });
            },

            crearJSON() {

                if (this.opcionCategoria == 1){
                for (let i=1; i<=this.escalas; i++){
                    this.listaEscala.push(i)
                }//lista de escala completa

                let jsonCategoria ={
                    ID: this.dataPreguntas[this.dataPreguntas.length - 1].ID + 1,
                    nombre: this.nombreCategoria,
                    descripcion: this.description,
                    preguntas: []
                };

                for (let j=1; j<=this.cantPreguntasEscala.length; j++) {
                    if (this.preguntasEscala[j] == null) {
                        console.log("es nulo")
                    }
                    else {
                        let variable = {
                            idpregunta: j,
                            pregunta: this.preguntasEscala[j],
                            escala: this.listaEscala
                        };
                        console.log("el json que pondre es", variable)
                        jsonCategoria.preguntas.push(variable)
                    }
                }

                    let roleAdmin ={
                        headers: {'Authorization':'Bearer ' + 'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250cmFzZW5hIjoiYXNkZiIsInJvbCI6MSwiY29ycmVvIjoiYWRtaW5AbWFpbC5jbCIsImFjdGl2byI6dHJ1ZX0.TrVdJeaJ5km92RKv2hI0yot8gWwtON3azO1qPvfdjZ0'}
                    };
                    this.$http.post('http://134.209.49.245:8080/mongodb-v1/categories/', JSON.stringify(jsonCategoria) , roleAdmin).then((response) => {
                        console.log("Hice el post de", jsonCategoria)
                    }, (response) => {
                        console.log("Fallo servicio")
                    });
                }
                else if (this.opcionCategoria == 2){

                }

            },



            buscarPorNom(){

                for (let i=0; i<this.dataUsuarios.length; i++){
                    if(this.dataUsuarios[i].nombre.includes(this.buscarNom)){
                        this.mostrarNom.push(this.dataUsuarios[i])
                    }
                }

            },

            buscarPorCorr(){

                for (let i=0; i<this.dataUsuarios.length; i++){
                    if(this.dataUsuarios[i].correo.includes(this.buscarCorr)){
                        this.mostrarCorr.push(this.dataUsuarios[i])
                    }
                }

            }
        }
    }
</script>

    <style lang="scss" scoped>
                       .demo-badge {
    > div {
        margin-bottom: 16px;
    }
    }

    .md-card {
    //width: 600px;
    //margin: 5px;
        margin-right: 5px;
        margin-left: 5px;
        margin-top: 5px;
        display: inline-block;
        vertical-align: top;
}

.md-content {
    width: 100px;
    height: 200px;
    display: inline-flex;
    justify-content: center;
    align-items: center;
}
/* Color del cuadrado primary */
.md-content.md-theme-default.md-primary {
    background-color: #ffbe33;
    color: #5d5d5d;
    font-size: 17px;
@import url('https://fonts.googleapis.com/css?family=Francois+One');
    font-family: 'Francois One', sans-serif;
}
/* Color del cuadrado accent*/
.md-content.md-theme-default.md-accent {
    background-color: #ff8b09;
    color: #474747;
    font-size: 17px;
@import url('https://fonts.googleapis.com/css?family=Francois+One');
    font-family: 'Francois One', sans-serif;
}
.imagePos{
    display: inline-flex;
    justify-content: right;
    /*    align-items: right; */
    float: right;
}

.font1{
    color: black;
    font-size: medium;
    font-weight: normal;
    font-style: oblique;
}

.font2{
    color: grey;
    font-size: large;
}

</style>