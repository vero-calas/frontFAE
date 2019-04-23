<template>
    <div>

        <md-tabs md-sync-route class="md-transparent" md-alignment="fixed">
            <md-tab id="tab-home" md-label="Home" to="/components/tabs/home">
                <div>
                    <!-- Carousel -->
                    <div style="float: left; width: 70%">
                        <div id="carouselExampleIndicators" class="carousel slide container" data-ride="carousel">
                            <ol class="carousel-indicators">
                                <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
                                <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
                                <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
                            </ol>
                            <div class="carousel-inner">
                                <div class="carousel-item active" >
                                    <img class="d-block w-100" src="https://www.wendywutours.co.uk/resource/upload/230/countrychile.jpg" alt="grafico" style="width: 200px; height:700px; margin: 0 auto">
                                    <div class="carousel-caption">
                                        <h2>Norte</h2>
                                        <h3>Visita el norte de Chile</h3>
                                    </div>
                                </div>
                                <div class="carousel-item">
                                    <img class="d-block w-100" src="http://www.educacionadventista.com/wp-content/uploads/2017/08/Chile-1920x600.jpg" alt="mapas" style="width: 200px; height:700px; margin: 0 auto">
                                    <div class="carousel-caption">
                                        <h2>Centro</h2>
                                        <h3>
                                            Visita el centro de Chile
                                        </h3>
                                    </div>
                                </div>
                                <div class="carousel-item">
                                    <img class="d-block w-100" src="https://www.wendywutours.com.au/resource/upload/1638/chile-top-toe-banner.jpg" alt="grafo" style="width: 200px; height:700px; margin: 0 auto">
                                    <div class="carousel-caption">
                                        <h2>Sur</h2>
                                        <h3>Visita el sur de Chile
                                        </h3>
                                    </div>
                                </div>
                            </div>
                            <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev" style="border-bottom-color: black">
                                <span class="glyphicon glyphicon-chevron-left fa-4x" aria-hidden="true"></span>
                                <span class="sr-only">Anterior</span>
                            </a>
                            <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
                                <span class="glyphicon glyphicon-chevron-right fa-4x" aria-hidden="true"></span>
                                <span class="sr-only">Siguiente</span>
                            </a>
                        </div>

                    </div>

                    <div style="float: right; width: 30%">
                        <md-card>
                            <md-card-header>
                                <div class="md-title">Turismo en Chile: </div>
                            </md-card-header>

                            <md-card-content>
                                La World Travel Awards por cuarto año consecutivo ha elegido a Chile como el mejor destino de turismo aventura de Sudamérica 2018. Sin duda, este reiterado reconocimiento internacional es una gran oportunidad como país, para ofrecer y cristalizar una atención sobresaliente a los turistas que nos visitan y construir una imagen como destino turístico de nivel internacional.  Si bien, las características geográficas de Chile (desiertos, montañas y lagos, playas y mar) son un gran estímulo para los visitantes, esto por sí solo no basta para construir una experiencia única y diferente para el turista. Es necesario gestionar un proceso sinérgico a partir del complemento del sector público y el sector privado, única manera de ofrecer servicios turísticos integrales a los visitantes. En este contexto, por un lado, hoteles, restaurantes, comercios y medios de transporte y telecomunicaciones y por otro, oficinas de servicios de turismo, municipalidades, guarda parqués, incluso los propios habitantes, juegan un rol gravitante en la construcción de esta imagen como destino turístico internacional.
                                <hr>
                                <img  class="img-responsive" src="https://images.sipse.com/XcKdUIMJr5cgvgtxW2HW6TXjm4g=/800x497/smart/2018/04/25/1524624771669.jpg">

                            </md-card-content>

                        </md-card>
                    </div>
                    <div><br><br><md-card>
                    </md-card><br><br></div>


                    <div style="width: 10%">
                        <md-card>
                        </md-card>
                    </div>

                    <div>
                        <div style="float: right; width: 40%">
                            <md-card>
                                <md-card-header>
                                    <div class="md-title"> Información general </div>
                                </md-card-header>
                                <md-card-content>

                                    e-ematur surge como resultado de la tesis doctoral denominada: “Confianza hacia los Destinos Turísticos. El rol de la Imagen, sus habitantes e Instituciones”. Este estudio fue presentado en el marco del Programa de Doctorado en Ciencias Empresariales impartido por la Facultad de Ciencias Económicas y Empresariales de la Universidad Autónoma de Madrid, España. Cabe destacar que este trabajo de investigación fue calificado como “Sobresaliente Cum Laude”, siendo esta la máxima calificación que se puede obtener en España. Dos son los aportes epistemológicos con los que se contribuye a las ciencias del marketing: 1) un modelo para medir la percepción del consumidor o turista; 2) un modelo multidimensional para medir la confianza del consumidor o turista. Ambos modelos de medición han sido ampliamente probados y aplicados en varias compañías y lugares turístico, obteniéndose excelentes resultados a la hora de mejorar las estrategias de marketing corporativo.

                                </md-card-content>
                            </md-card>
                        </div>
                        <div>
                            <md-card>
                                <md-card-header>
                                    <div class="md-title"> ¿Quiénes somos? </div>
                                </md-card-header>
                                <md-card-content>

                                    e-ematur (electrónica-escala de marketing y turismo) es un servicio de medición online de la percepción que posee un consumidor o turista acerca de un producto, servicio o destino turístico, pionero en el área del marketing. Es un servicio innovador que permite la detección temprana, prevención, diagnóstico y tratamiento de un débil posicionamiento logrado por un producto, servicio, idea, empresa, marca o destino turístico. Es sabido que de la percepción de su producto, servicio o destino turístico dependerá, en gran medida, la satisfacción de su cliente o visitante.

                                </md-card-content>
                            </md-card>
                        </div>

                    </div>
                </div>
            </md-tab>

            <md-tab id="tab-pages" md-label="¿Quiénes Somos?" to="/components/tabs/pages">
                <div>
                    <md-card-content style="float: left; width: 50%">
                        <img  class="img-responsive" src="https://d1ljaggyrdca1l.cloudfront.net/wp-content/uploads/2017/04/Guanaco-in-Torres-del-Paine-National-Park-Chile-1600x900.jpg">
                    </md-card-content>

                    <div>
                        <md-card class="card">
                            <md-card-header>
                                <div class="md-title">Sobre la iniciativa: </div>
                            </md-card-header>
                            <md-card-content>

                                    La percepción o imagen desde el punto de vista de marketing es una combinación de aspectos distintos de las características físicas del producto o servicio, pero, no obstante, se identifican con el producto o servicio, como, por ejemplo, el nombre de la marca, los símbolos utilizados en la publicidad, la buena aprobación de una figura conocida o el país de origen de un producto o servicio. La percepción o imagen percibida es la expresión de todo el conocimiento, impresiones, prejuicios y pensamientos emocionales que un individuo o grupo tienen sobre un objeto o un lugar en particular. La percepción de un producto, servicio o destino turístico se forma como resultado de la evaluación de atributos individuales que pueden tener un contenido cognitivo y emocional. En otras palabras, la percepción o imagen es un factor formado por cinco dimensiones: a) la evaluación cognitiva; b) la evaluación afectiva; c) el beneficio funcional; d) el beneficio hedónico y e) el beneficio simbólico percibido por el consumidor o turista. Dimensiones que permiten al consumidor o turista conectarse en forma racional, emocional, enfocado (a) en la solución, placentera o enfocado (a) en la pertenencia social con el producto, servicio o lugar. Siendo estas cinco dimensiones desde el punto de vista de marketing, el soporte básico del triangulo virtuoso entre la calidad-satisfacción y lealtad del consumidor o turista.

                            </md-card-content>
                        </md-card>
                    </div>
                </div>


            </md-tab>

            <md-tab id="tab-posts" md-label="Contacto" to="/components/tabs/posts">

                <div>
                    <md-card-content style="float: left; width: 50%">
                        <img  class="img-responsive" src="https://www.rockandpop.cl/wp-content/uploads/2016/10/isla-de-pascua_shutterstok-MZ33.jpg">
                    </md-card-content>

                    <div>
                        <md-card class="card">
                            <md-card-header>
                                <div class="md-title">Información de contacto:</div>
                            </md-card-header>
                            <md-card-content>
                                A su disposición medios de contacto directo:
                                <hr>
                                <label><i class="material-icons">call</i> +56-9-98875670 </label>

                                <hr>
                                <label><i class="material-icons">mail_outline</i> enrique.marinao@usach.cl </label>
                                <hr>
                                <label><i class="material-icons">mail_outline</i> enrique.marinao@e-ematur.cl </label>
                                <!--<label><i class="material-icons">public</i> https: facebook </label>-->
                            </md-card-content>
                        </md-card>
                    </div>
                </div>


            </md-tab>

            <md-tab id="tab-favorites" md-label="Responder encuesta" to="/components/tabs/favorites">
                <md-progress-spinner v-if="mostrarSpinner" :md-value="progressSpinner" md-mode="indeterminate"></md-progress-spinner>
                <div v-if="mostrarOpciones" style="width: 100%; height: 100%">
                    <md-card style="float: left">
                        <img src="../src/img/logo.png"/>
                    </md-card>
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <md-card style="width: 700px; margin: 3px">
                        &nbsp;&nbsp;&nbsp;&nbsp;<label class="md-title">Seleccione los criterios para su encuesta:</label>
                    <hr><hr>
                        &nbsp;&nbsp;  <label>¿Qué temática de la encuesta desea responder?</label>
                        <br>
                        &nbsp;&nbsp;  <md-radio v-model="opcion1" value="1">Turismo</md-radio>
                        &nbsp;&nbsp;  <md-radio v-model="opcion1" value="2">Marketing</md-radio>
                    <hr>
                        &nbsp;&nbsp;  <label>¿Qué tipo de encuesta desea responder?</label>
                        <br>
                        &nbsp;&nbsp;  <md-radio v-model="opcion2" value="1">General</md-radio>
                        &nbsp;&nbsp;  <md-radio v-model="opcion2" value="2">Resumida</md-radio>
                    {{opcion1}} {{opcion2}}
                        <hr>
                        <md-button class="md-raised" v-on:click="mostrarPrimero">Aceptar</md-button>
                        </md-card>
                </div>

                <div v-if="mostrar1">
                    <div>
                        <!-- opciones  md-vertical, md-horizontal, md-alternative-->

                        <md-steppers md-horizontal>


                            <!--                          ENCUESTA DE Turismo                                        -->
                            <!--                          **************************                                       -->
                            <md-step id="0">
                                <div>
                                    <img width="150" height="80" src="../src/img/logo.png">
                                    &nbsp;&nbsp;&nbsp;&nbsp;
                                    <label>Bienvenido a la encuesta sobre el Marketing en Chile</label> </div>

                            <md-button class="md-raised" v-on:click="backButton">Atrás</md-button>
                            </md-step>


                            <md-step id="1">
                                <div>
                                <h1>Datos personales</h1>
                                <label>Por favor señale su nivel de estudios:</label>
                                <hr>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="Básica incompleta">
                                    <label>Básica incompleta</label>
                                </md-radio>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="Básica completa">
                                    <label>Básica completa</label>
                                </md-radio>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="Media incompleta">
                                    <label>Media incompleta</label>
                                </md-radio>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="Media completa">
                                    <label>Media completa</label>
                                </md-radio>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="Técnico (o instituto profesional) incompleto">
                                    <label>Técnico (o instituto profesional) incompleto</label>
                                </md-radio>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="Técnico (o instituto profesional) completo">
                                    <label>Técnico (o instituto profesional) completo</label>
                                </md-radio>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="Universitario incompleto">
                                    <label>Universitario incompleto</label>
                                </md-radio>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="Universitario completo">
                                    <label>Universitario completo</label>
                                </md-radio>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="Estudios de postgrado incompleto">
                                    <label>Estudios de postgrado incompleto</label>
                                </md-radio>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="Estudios de postgrado completo">
                                    <label>Estudios de postgrado completo</label>
                                </md-radio>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="Otro">
                                    <label>Otro</label>
                                </md-radio>
                                <md-radio v-model="jsonFinal.nivelDeEstudio" value="No sabe-No Responde">
                                    <label>No sabe-No Responde</label>
                                </md-radio>
                                {{jsonFinal.nivelDeEstudio}}
                                </div>
                                <div>

                                </div>


                            </md-step>

                            <md-step v-model="array" v-if="i>0" :key="i" :value="i" v-for="(categoria,i) in datos" :id="datos[i].id">
                                <h1>{{datos[i].nombre}}</h1><br>
                                <label>{{datos[i].descripcion}}</label>
                                <br><label> Por favor, responda según su opinión</label>
                                <hr>
                                <div v-model="array2" v-if="j!==20" :key="j" :value="j" v-for="(preguntas,j) in categoria.preguntas">
                                    <hr>
                                    <label> {{ preguntas.pregunta }} </label>
                                    <div>
                                        <md-radio v-model="form2[i].respuesta[j]" v-if="k!==14" :key="k" :value="k" v-for="(escala,k) in preguntas.escala">
                                            <label v-if="preguntas.escala !== null">
                                                {{preguntas.escala[k]}}
                                            </label>
                                        </md-radio>
                                        <md-radio v-model="form2[i].respuesta[j]" v-if="k!==14" :key="k" :value="k" v-for="(escala,k) in preguntas.opciones">
                                            <label v-if="preguntas.opciones !== null">
                                                {{preguntas.opciones[k]}}
                                            </label>
                                        </md-radio>
                                    </div>
                                </div>
                                <md-button v-on:click="guardarRespuestas" class="md-raised md-primary; center">Enviar Respuestas</md-button>
                            </md-step>
                        </md-steppers>
                    </div>
                </div>

                <div v-if="mostrar2">
                    <div>
                        <!-- opciones  md-vertical, md-horizontal, md-alternative-->

                        <md-steppers md-horizontal>


                            <!--                          ENCUESTA DE Turismo RESUMIDA                                       -->
                            <!--                          **************************                                       -->
                            <md-step id="0">
                                <div>
                                    <img width="150" height="80" src="../src/img/logo.png">
                                    &nbsp;&nbsp;&nbsp;&nbsp;
                                    <label>Bienvenido a la encuesta sobre el Turismo en Chile</label> </div>
                                <md-button v-on:click="backButton">Atrás</md-button>
                            </md-step>
                            <md-step id="1">
                                <div>
                                    <h1>Datos personales</h1>
                                    <label>Por favor señale su nivel de estudios:</label>
                                    <hr>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="Básica incompleta">
                                        <label>Básica incompleta</label>
                                    </md-radio>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="Básica completa">
                                        <label>Básica completa</label>
                                    </md-radio>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="Media incompleta">
                                        <label>Media incompleta</label>
                                    </md-radio>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="Media completa">
                                        <label>Media completa</label>
                                    </md-radio>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="Técnico (o instituto profesional) incompleto">
                                        <label>Técnico (o instituto profesional) incompleto</label>
                                    </md-radio>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="Técnico (o instituto profesional) completo">
                                        <label>Técnico (o instituto profesional) completo</label>
                                    </md-radio>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="Universitario incompleto">
                                        <label>Universitario incompleto</label>
                                    </md-radio>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="Universitario completo">
                                        <label>Universitario completo</label>
                                    </md-radio>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="Estudios de postgrado incompleto">
                                        <label>Estudios de postgrado incompleto</label>
                                    </md-radio>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="Estudios de postgrado completo">
                                        <label>Estudios de postgrado completo</label>
                                    </md-radio>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="Otro">
                                        <label>Otro</label>
                                    </md-radio>
                                    <md-radio v-model="jsonFinalSentimiento.nivelDeEstudio" value="No sabe-No Responde">
                                        <label>No sabe-No Responde</label>
                                    </md-radio>
                                    {{jsonFinalSentimiento.nivelDeEstudio}}
                                </div> <!--  Nivel de estudios   -->

                                <div>

                                </div>


                            </md-step>

                            <md-step v-model="array" v-if="i>0" :key="i" :value="i" v-for="(categoria,i) in datos" :id="datos[i].id">
                                <h1>{{datos[i].nombre}}</h1><br>
                                <label>{{datos[i].descripcion}}</label>
                                <br><label> Por favor, responda según su opinión</label>
                                <hr>
                                <div>
                                    <hr>
                                    <label>{{listaDescripciones[i]}}</label>
                                    <div>
                                        <br>
                                        <hr>
                                        <div>
                                            <md-icon class="md-size-2x" style="color: #08e166">
                                                sentiment_very_satisfied
                                            </md-icon>
                                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                                            <md-icon class="md-size-2x" style="color: #fbe246">
                                                sentiment_satisfied
                                            </md-icon>
                                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                                            <md-icon class="md-size-2x" style="color: #fb2514">
                                                sentiment_very_dissatisfied
                                            </md-icon><br>

                                            <md-radio v-model=form3[i].respuesta v-for="n in 7" :value="n">
                                                <label>
                                                    {{n}}
                                                </label>
                                            </md-radio>
                                          form3:  {{form3}}
                                          form3[i]:  {{form3[i]}}

                                        </div>
                                    </div>
                                </div>
                                <md-button v-on:click="guardarRespuestaSentimiento" class="md-raised md-primary; center">Enviar Respuestas</md-button>

                            </md-step>


                        </md-steppers>
                    </div>
                </div>

                <div v-if="mostrar3">
                    <div>
                        <!-- opciones  md-vertical, md-horizontal, md-alternative-->

                        <md-steppers md-horizontal>


                            <!--                          SEGUNDA ETAPA DE ENCUESTA                                        -->
                            <!--                          **************************                                       -->
                            <md-step id="0">
                                <div>
                                    <img width="150" height="80" src="../src/img/logo.png">
                                    &nbsp;&nbsp;&nbsp;&nbsp;
                                    <label>Bienvenido a la encuesta sobre el Marketing en Chile</label>
                                    <br>
                                    <md-button v-on:click="backButton">Atrás</md-button>
                                </div>
                            </md-step>
                            <md-step v-model="array" v-if="i!==20" :key="i" :value="i" v-for="(categoria,i) in datos" :id="datos[i].id">
                                <h1>{{datos[i].nombre}}</h1><br>
                                <label>{{datos[i].descripcion}}</label>
                                <br><label> Por favor, responda según su opinión</label>
                                <hr>
                                <div v-model="array2" v-if="j!==20" :key="j" :value="j" v-for="(preguntas,j) in categoria.preguntas">
                                    <hr>
                                    <label> {{ cambiarPregunta(preguntas.pregunta) }} </label>
                                    <div>
                                        <md-radio v-model="form2[i].respuesta[j]" v-if="k!==14" :key="k" :value="k" v-for="(escala,k) in preguntas.escala">
                                            <label v-if="preguntas.escala !== null">
                                                {{preguntas.escala[k]}}
                                            </label>
                                        </md-radio>
                                        <md-radio v-model="form2[i].respuesta[j]" v-if="k!==14" :key="k" :value="k" v-for="(escala,k) in preguntas.opciones">
                                            <label v-if="preguntas.opciones !== null">
                                                {{preguntas.opciones[k]}}
                                            </label>
                                        </md-radio>
                                    </div>
                                </div>

                            </md-step>
                            <md-button v-on:click="guardarRespuestas" class="md-raised md-primary; center">Enviar Respuestas</md-button>
                        </md-steppers>
                    </div>
                </div>


            </md-tab>

        </md-tabs>




    </div>
</template>

<script>
    export default {
        name: "home",
        props: ['datos'],
        data: () => ({
            form2:[],
            jsonFinal: {
                correo : null,
                nivelDeEstudio: null,
                situacionLaboral: null,
                nivelDeIngreso: null,
                sexo: null,
                estadoCivil: null,
                rangoDeEdad: null,
                fecha: null,
                idregion: null,
                telefono: null,
                tipoEncuesta: null,
                resultados: null
            },
            form3: [],
            jsonFinalSentimiento: {
                correo : null,
                nivelDeEstudio: null,
                situacionLaboral: null,
                nivelDeIngreso: null,
                sexo: null,
                estadoCivil: null,
                rangoDeEdad: null,
                fecha: null,
                idregion: null,
                telefono: null,
                tipoEncuesta: null,
                resultados: null
            },
            array:[],
            array2:null,
            empresa: null,
            opcion1: null,
            opcion2: null,
            mostrarOpciones: true,
            mostrar1: false,
            mostrar2: false,
            mostrar3: false,
            progressSpinner: 0,
            mostrarSpinner: true,
            listaDescripciones: ["Podría ser definida como aquellas estructuras y procesos mentales relacionados con el pensamiento, comprensión, e interpretación de estímulos y eventos. Esto incluye los acontecimientos, significados y creencias que se han desarrollado en los turistas y/o visitantes a partir de sus experiencias y que se almacenan en la memoria.",
                                  "Es reactiva, es incontrolable en forma directa, se manifiesta a través de expresiones físicas, es fácil de estimular y puede ser aprendida. La respuesta afectiva es reactiva dado que no es una condición planificada ni intencional, por el contrario, el turista responde a factores ambientales que para él son relevantes, por ejemplo, un atardecer a la orilla de un lago.",
                                "Es una experiencia en múltiples modalidades sensoriales como los gustos, los sonidos, los olores, las impresiones táctiles y las imágenes visuales. Los individuos no sólo responden a las impresiones multisensoriales de los estímulos externos (por ejemplo, una estadía en el desierto bajo una noche estrellada) mediante la codificación de estos insumos sensoriales, sino que también reaccionan mediante la generación de imágenes multisensoriales dentro de sí mismos.",
                "Puede ser definido como el “yo” real e ideal que tiene el turista. Este “yo” es la suma total de todo lo que una persona pueda llamar propio, su cuerpo, rasgos y habilidades, sus posesiones materiales, su familia, amigos y enemigos, sus vocaciones y ocupaciones y mucho más. Incluye las evaluaciones y definiciones de sí mismo que pueden ser reflejadas a través de sus acciones, incluyendo la evaluación y adquisición de lugares y/o destinos turísticos.",
                "El beneficio funcional está ligado a las necesidades, al valor, a los fundamentos, a la necesidad esencial y a la resolución de problemas. En concreto, el turista y/o visitante buscará satisfacer sus necesidades funcionales definidas como las que motivan la búsqueda de productos turísticos que resuelvan sus problemas relacionados con el descanso, por ejemplo, resolver un problema de estrés que lo aqueje. "
            ],
            cantidadCategoria: null
        }),
        created() {
        },
        mounted(){
            this.progressSpinner += 15;
            this.cantidad();

            console.log("llegue aca1", this.progressSpinner)
            this.progressSpinner +=25;
            this.cantidadSentimiento();
            this.progressSpinner +=75;
            this.mostrarSpinner = false;
            console.log("llegue aca2", this.progressSpinner)
            this.cambiarPregunta();


        },
        methods:{

            cambiarPregunta(entrada){
                this.$http.get('http://localhost:8092/categories/all').then(response => {
                    this.empresa = response.data;
                    console.log('data de regiones obtenido es:', this.empresa);
                }, (response) => {
                    this.error = true;
                    console.log('no obtiene regiones');
                });

              for (let i=0; i < 20 ; i++){
                  var cosa = this.empresa[0].empresa;
                  if (entrada[i] === "Chile") {
                      var split = entrada.split("Chile");
                      var preguntaFinal = split[0] + cosa + split[1]
                  }
                  else {
                      console.log("no hice nada jaja")
                  }

              }
              return preguntaFinal
            },

// opcion1, 1-turismo 2-marketing
// opcion2, 1-general 2-resumida
            mostrarPrimero(){
              if (this.opcion1==='1' && this.opcion2==='1' ){
                  this.mostrar1 = true;
                  this.mostrar2 = false;
                  this.mostrar3 = false;
                  this.mostrarOpciones = false
                }
                else if (this.opcion1==='1' && this.opcion2==='2'){
                  this.mostrar2 = true;
                  this.mostrar1 = false;
                  this.mostrar3 = false;
                  this.mostrarOpciones = false
              }
              else if (this.opcion1==='2' && this.opcion2==='1'){
                  this.mostrar3 = true;
                  this.mostrar1 = false;
                  this.mostrar2 = false;
                  this.mostrarOpciones = false
              }
              else if (this.opcion1==='2' && this.opcion2==='2'){
                  this.mostrar2 = true;
                  this.mostrar1 = false;
                  this.mostrar3 = false;
                  this.mostrarOpciones = false
              }
            },

            backButton(){
              this.mostrarOpciones = true;
              this.mostrar1 = false;
              this.mostrar2 = false;
              this.mostrar3 = false;
            },

            cantidad(){
                this.cantidadCategoria = (this.datos).length;
                for (let i=0; i<this.cantidadCategoria ; i++){
                    let json ={
                        respuesta: [],
                        idcategoria: i+1
                    };
                    this.form2.push(json)
                }
            },

            cantidadSentimiento(){
                console.log("la data que llega es", this.datos);
                this.cantidadCategoria = (this._props.datos).length;
                for (let i=0; i<this.cantidadCategoria; i++){
                    let json ={
                        respuesta: [],
                        idcategoria: i+1
                    };
                    this.form3.push(json)
                }
            },

            multiplicarRespuestas(){
                console.log("this.form3", this.form3);

                for(let i=0; i<this.form3.length; i++){
                    let numero = this.form3[i].respuesta;
                    this.form3[i].respuesta = [];
                    console.log("lo hareeeeee:", this.datos[i].preguntas.length);
                    for (let j=0; j<this.datos[i].preguntas.length; j++) {
                        this.form3[i].respuesta.push(numero)
                    }
                }
                this.form3.shift();
                console.log("lo que obtengo es;", this.form3)
            },

            guardarRespuestas(){
                this.form2.shift();
                this.jsonFinal.resultados = this.form2;
                console.log("el json final es:", this.jsonFinal)
                this.$http.post('http://localhost:8092/encuestados',JSON.stringify(this.jsonFinal)).then((response) => {
                    console.log("Se hizo el post",response);
                }, (response) =>{
                    console.log("No se logro el post",response)
                });

            },

            guardarRespuestaSentimiento(){
                this.multiplicarRespuestas();
                this.jsonFinalSentimiento.resultados = this.form3
                console.log("el json final es:", this.jsonFinalSentimiento)
                this.$http.post('http://localhost:8092/encuestados',JSON.stringify(this.jsonFinalSentimiento)).then((response) => {
                    console.log("Se hizo el post",response);
                }, (response) =>{
                    console.log("No se logro el post",response)
                });

            }
        }
    }
</script>


<style lang="scss" scoped>
    .carousel-item{
        height: 480px;
    }
    .card-expansion {
        height: 480px;
    }
    .md-card {
        width: 320px;
        margin: 4px;
        display: inline-block;
        vertical-align: top;
    }
    .center {
        display: block;
        margin-left: auto;
        margin-right: auto;
        width: 20%;
    }
    .ImageCarousel{
        max-width: 100%;
        height: 300px;
        position: relative;
        display: block;
        margin: auto;
    }
    .card {
        width: 40%;
        margin: 4px;
        display: inline-block;
        vertical-align: top;
    }
</style>