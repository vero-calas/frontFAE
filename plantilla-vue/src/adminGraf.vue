<template>

    <div>
        <md-tabs md-sync-route class="md-transparent" md-alignment="fixed">
           <md-tab id="tab-general" md-label="General" to="/components/tabs/generalGraf">
               <md-card style="width: 40%; float: left">
                   <md-card-header>
                       <div class="md-title">Gráfico 1:</div>
                   </md-card-header>
                   <md-card-media>
                       <div>
                           <vue-chart  v-if="this.dataFija1 !== null" type="pie" :data="this.dataFija1"></vue-chart>
                           <div v-else>
                               <div class=" lds-css ng-scope">
                               </div>
                           </div>
                       </div>
                   </md-card-media>
               </md-card>
           <br>
               <md-card style="width: 40%; float: right">
                   <md-card-header>
                       <div class="md-title">Gráfico 2:</div>
                   </md-card-header>
                   <md-card-media>
                       <div>
                           <vue-chart  v-if="this.dataFija2 !== null" type="pie" :data="this.dataFija2"></vue-chart>
                           <div v-else>
                               <div class=" lds-css ng-scope">
                               </div>
                           </div>
                       </div>
                   </md-card-media>
               </md-card>
               <br>
               <md-card style="width: 40%; float: left">
                   <md-card-header>
                       <div class="md-title">Gráfico 3:</div>
                   </md-card-header>
                   <md-card-media>
                       <div>
                           <vue-chart  v-if="this.dataFija3 !== null" type="pie" :data="this.dataFija3"></vue-chart>
                           <div v-else>
                               <div class=" lds-css ng-scope">
                               </div>
                           </div>
                       </div>
                   </md-card-media>
               </md-card>
               <br>
               <md-card style="width: 40%; float: right">
                   <md-card-header>
                       <div class="md-title">Gráfico 4:</div>
                   </md-card-header>
                   <md-card-media>
                       <div>
                           <vue-chart  v-if="this.dataFija4 !== null" type="pie" :data="this.dataFija4"></vue-chart>
                           <div v-else>
                               <div class=" lds-css ng-scope">
                               </div>
                           </div>
                       </div>
                   </md-card-media>
               </md-card>
           </md-tab>

            <md-tab id="tab-filter" md-label="Filtrar Gráfico" to="/components/tabs/filterGraf">

                <div style="float: left; width: 50%">
                <md-card>
                    <div>

                    <div>

                        <div>
                            <div>
                                <label>Elija tipo de encuesta:</label>
                            </div>
                            <div>
                                <md-radio v-model="tipoDeEncuesta" value="1">Encuesta detallada</md-radio>
                                <md-radio v-model="tipoDeEncuesta" value="2">Encuesta resumida</md-radio>
                                </div>
                            </div>
                        </div>

                        <div>
                        <div>
                            <label>Elija criterios para graficar:</label>
                        </div>
                        <div>
                            <div class="md-layout md-gutter">
                                <div class="md-layout-item">
                            <md-field>
                                <md-select v-model="variableSD" name="variableSD" id="variableSD">
                                    <md-option value="nivel de estudios">Nivel de estudios</md-option>
                                    <md-option value="situacion laboral">Situacion Laboral</md-option>
                                    <md-option value="nivel de ingresos">Nivel de Ingresos</md-option>
                                    <md-option value="genero">Genero</md-option>
                                    <md-option value="estado civil">Estado Civil</md-option>
                                    <md-option value="edad">Edad</md-option>
                                </md-select>
                            </md-field>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div>
                        <div>
                            <label>Elija la región para graficar:</label>
                        </div>
                        <div>
                        <div class="md-layout md-gutter">
                            <div class="md-layout-item">
                                <md-field>
                                    <md-select v-model="region" name="region" id="region">
                                        <md-option value="1">XV - Arica y Parinacota</md-option>
                                        <md-option value="2">I - Tarapacá</md-option>
                                        <md-option value="3">II - Antofagasta</md-option>
                                        <md-option value="4">III - Atacama</md-option>
                                        <md-option value="5">IV - Coquimbo</md-option>
                                        <md-option value="6">V - Valparaíso</md-option>
                                        <md-option value="7">VI - Libertador Bernardo O'Higgins</md-option>
                                        <md-option value="8">VII - Maule</md-option>
                                        <md-option value="9">VIII - Bío-Bío</md-option>
                                        <md-option value="10">IX - La Araucanía</md-option>
                                        <md-option value="11">XIV - Los Ríos</md-option>
                                        <md-option value="12">X - Los Lagos</md-option>
                                        <md-option value="13">XI - Aysén</md-option>
                                        <md-option value="14">XII - Magallanes y la Antártica Chilena</md-option>
                                        <md-option value="15">RM - Metropolitana</md-option>
                                    </md-select>
                                </md-field>
                            </div>
                        </div>
                        </div>
                    </div>

                        <div>
                            <div>
                                <label>Elija la categoría para graficar:</label>
                            </div>
                            <div>
                                <div class="md-layout md-gutter">
                                    <div class="md-layout-item">
                                        <md-field>
                                            <md-select v-model="categoria" name="variableSD" id="variableSD">
                                                <md-option value="2">Percepcion Cognitiva</md-option>
                                                <md-option value="3">Evaluacion Afectiva</md-option>
                                                <md-option value="4">Beneficio Hedónico</md-option>
                                                <md-option value="5">Beneficio Simbólico</md-option>
                                                <md-option value="6">Beneficio Funcional</md-option>
                                                <md-option value="7">Familiaridad</md-option>
                                                <md-option value="8">Satisfacción</md-option>
                                                <md-option value="9">Reputación</md-option>
                                                <md-option value="10">Honestidad (Confianza en la gente)</md-option>
                                                <md-option value="11">Benevolencia (Confianza en la gente)</md-option>
                                                <md-option value="12">Competencia (Confianza en la gente)</md-option>
                                                <md-option value="13">Honestidad (Confianza en las instituciones publicas)</md-option>
                                                <md-option value="14">Benevolencia (Confianza en las instituciones publicas)</md-option>
                                                <md-option value="15">Competencia (Confianza en las instituciones publicas)</md-option>
                                                <md-option value="16">Honestidad (Confianza en las instituciones privadas)</md-option>
                                                <md-option value="17">Benevolencia (Confianza en las instituciones privadas)</md-option>
                                                <md-option value="18">Competencia (Confianza en las instituciones privadas))</md-option>
                                            </md-select>
                                        </md-field>
                                    </div>
                                </div>
                            </div>
                        </div>

                    <div>
                        <md-datepicker v-model="selectedInitial">
                            <label>Seleccione fecha inicial</label>
                        </md-datepicker>
                    </div>

                    <div>
                        <md-datepicker v-model="selectedFinal">
                            <label>Seleccione fecha final</label>
                        </md-datepicker>
                    </div>

                    </div>

                </md-card>

               <button v-on:click="crearGrafico">Click me</button>
                </div>

                <div style="float: right; width: 50%">
                <md-card style="width: 97%; float: left">
                    <md-card-header>
                        <div class="md-title">Gráfico:</div>
                    </md-card-header>
                    <md-card-media>
                        <div v-if="this.showd">
                            <vue-chart  v-if="this.pieData !== null" type="pie" :data="this.pieData"></vue-chart>
                            <div v-else>
                                <div class=" lds-css ng-scope">
                                </div>
                            </div>
                        </div>
                    </md-card-media>
                </md-card>
</div>
                
            </md-tab>

        </md-tabs>
    </div>
    
</template>

<script>
    import VueChart from "vue-chart-js";
    export default {
        props: ['datos'],
        name: "adminGraf",
        components: {
            VueChart
        },

        data: () => ({
            tipoDeEncuesta: null,
            variableSD: null,
            region: null,
            selectedInitial: null,
            selectedFinal: null,
            categoria: null,
            dataGr: null,
            dataGrSD: null,
            error: false,
            pieData: null,
            showd: null,
            mostrar: false,
            dataFija1: {
                labels: ["Aprobados", "Desaprobados", "Neutro"],
                datasets: [
                    {
                        //data: [this.DataGr.Aprobados, this.DataGr.Rechazados, this.DataGr.Neutro],
                        data: [100, 20, 30],
                        label: ["Puntuación alcanzada"],
                        backgroundColor: [
                            '#D4E157',
                            '#e15545',
                            '#fbe246'
                        ],
                    },

                ]
            },
            dataFija2: {
                labels: ["Aprobados", "Desaprobados", "Neutro"],
                datasets: [
                    {
                        //data: [this.DataGr.Aprobados, this.DataGr.Rechazados, this.DataGr.Neutro],
                        data: [40, 40, 40],
                        label: ["Puntuación alcanzada"],
                        backgroundColor: [
                            '#D4E157',
                            '#e15545',
                            '#fbe246'
                        ],
                    },

                ]
            },
            dataFija3: {
                labels: ["Aprobados", "Desaprobados", "Neutro"],
                datasets: [
                    {
                        //data: [this.DataGr.Aprobados, this.DataGr.Rechazados, this.DataGr.Neutro],
                        data: [20, 0, 30],
                        label: ["Puntuación alcanzada"],
                        backgroundColor: [
                            '#D4E157',
                            '#e15545',
                            '#fbe246'
                        ],
                    },

                ]
            },
            dataFija4: {
                labels: ["Aprobados", "Desaprobados", "Neutro"],
                datasets: [
                    {
                        //data: [this.DataGr.Aprobados, this.DataGr.Rechazados, this.DataGr.Neutro],
                        data: [30, 30, 90],
                        label: ["Puntuación alcanzada"],
                        backgroundColor: [
                            '#D4E157',
                            '#e15545',
                            '#fbe246'
                        ],
                    },

                ]
            }
        }),

        created() {
            this.graficoInicial();
            //this.crearGrafico();
        },

        methods: {

            graficoInicial(){
                const auth = {
                    headers: {'Authorization':'Bearer ' + 'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250cmFzZW5hIjoiJDJhJDEwJGtsblN6Tm9oNHF5M1RQOS9scXhCN3VpdmdQeG9XTVZNZ2F0eVIwb0taVC4vRnl2Qi42S0RLIiwicm9sIjoxLCJjb3JyZW8iOiJhZG1pbkBtYWlsLmNsIiwiYWN0aXZvIjp0cnVlfQ.g78PzR0At1xVkHqXYPIVJmHWmF8YHmtQu6nXG8AoEnU'}
                };
                let json = {
                    "categoria_id": 2,
                    "tipoEncuesta": 1,
                    "region_id": 1,
                    "fechaInicial": "2018-08-27T23:59:59.000+0000",
                    "fechaFinal": "2018-09-01T00:00:00.000+0000"
                };

                //servicio de envio del json
                //console.log("el json que quiero enviar es:", json);
                /*
                this.$http.post('http://localhost:8092/encuestados/graphics', JSON.stringify(json), auth).then(response => {
                   console.log("entre")
                    this.dataGr = response.data;
                    console.log('data de grafico obtenido es:', this.dataGr);
                }, (response) => {
                    console.log('no obtiene data grafico');
                    this.error = true;
                });
                */
            },

            cambiarMes(mes){
                if(mes === "Jan"){
                    return "01"
                }
                else if(mes === "Feb"){
                    return "02"
                }
                else if(mes === "Mar"){
                    return "03"
                }
                else if(mes === "Apr"){
                    return "04"
                }
                else if(mes === "May"){
                    return "05"
                }
                else if(mes === "Jun"){
                    return "06"
                }
                else if(mes === "Jul"){
                    return "07"
                }
                else if(mes === "Aug"){
                    return "08"
                }
                else if(mes === "Sep"){
                    return "9"
                }
                else if(mes === "Oct"){
                    return "10"
                }
                else if(mes === "Nov"){
                    return "11"
                }
                else if(mes === "Dec"){
                    return "12"
                }
                else {
                    console.log("error leyendo el mes")
                }

            },

            llamarServicio(){
                console.log("estoy en la funcion llamarServicio");
                this.mostrar = true;
                if(this.variableSD == null){
                    //declaracion del json

                    let fechaInicio = this.selectedInitial + '';
                    let fechaInicioSplit = fechaInicio.split(" ");
                    let fechaInicioServFinal =  fechaInicioSplit[3] + "-" + this.cambiarMes(fechaInicioSplit[1]) + "-" + fechaInicioSplit[2] + "T00:00:00.000+0000";
                    let fechaFinal = this.selectedFinal + '';
                    let fechaFinSplit = fechaFinal.split(" ");
                    let fechaServFinal =  fechaFinSplit[3] + "-" + this.cambiarMes(fechaFinSplit[1]) + "-" + fechaFinSplit[2] + "T23:59:59.000+0000";
                    console.log("la fecha queda configurada como:", fechaServFinal);
                    let json = {
                        "categoria_id": this.categoria,
                        "tipoEncuesta": this.tipoDeEncuesta,
                        "region_id": this.region,
                        "fechaInicial": fechaInicioServFinal,
                        "fechaFinal": fechaServFinal
                    };

                    //servicio de envio del json
                    console.log("el json que quiero enviar es:", json);
                    const auth = {
                        headers: {'Authorization':'Bearer ' + 'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250cmFzZW5hIjoiJDJhJDEwJGtsblN6Tm9oNHF5M1RQOS9scXhCN3VpdmdQeG9XTVZNZ2F0eVIwb0taVC4vRnl2Qi42S0RLIiwicm9sIjoxLCJjb3JyZW8iOiJhZG1pbkBtYWlsLmNsIiwiYWN0aXZvIjp0cnVlfQ.g78PzR0At1xVkHqXYPIVJmHWmF8YHmtQu6nXG8AoEnU'}
                    };
                    this.$http.post('http://localhost:8092/encuestados/graphics', JSON.stringify(json), auth).then(response => {
                        this.dataGr = response.data;
                        console.log('data de grafico obtenido es:', this.dataGr);
                    }, (response) => {
                        console.log('no obtiene data grafico');
                    });
                    //this.crearGrafico();
                }

                else {
                    //declaracion del json para SD
                    console.log("las fechas son: ", this.selectedInitial.split(" "), this.selectedFinal);
                    let fechaInicio = this.selectedInitial + "T23:59:59.000+0000";
                    let fechaFin = this.selectedFinal + "T00:00:00.000+0000";

                    let json2 = {
                        "categoria_id": this.categoria,
                        "tipoEncuesta": this.tipoDeEncuesta,
                        "region_id": this.region,
                        "variableSD": this.variableSD,
                        "fechaInicial": fechaInicio,
                        "fechaFinal": fechaFin
                    };

                    //servicio para SD
                    console.log("el json que quiero enviar es,", json2);

                    this.$http.post('http://localhost:8092/encuestados/graphicsSD', JSON.stringify(json2)).then(response => {
                        this.dataGr = response.data;
                        console.log('data de graficoSD obtenido es:', this.dataGr);
                    }, (response) => {
                        console.log('no obtiene data graficoSD');
                        this.error = true;
                    });

                   // this.crearGrafico();
                }
               // this.crearGrafico();
            },


            crearGrafico(){
                this.llamarServicio()
                 this.pieData = {};
                 this.showd=true
            }
        }
    }
</script>

<style scoped>

</style>