<template>
    <div>
        <!-- Pagina General -->
        <md-app md-mode="overlap">
            <md-app-toolbar class="md-accent md-large">
                <div class="md-toolbar-row">
                    <md-button class="md-icon-button" @click="menuVisible = !menuVisible">
                        <md-icon>menu</md-icon>
                    </md-button>
                    <div style="float: right">
                        <span class="md-title">e-ematur</span>
                    </div>

                    <div class="md-toolbar-section-end">
                        <md-button @click="showDialogLogin = true">
                            Login
                        </md-button>
                        <md-button @click="showDialogRegister = true">
                            Registro
                        </md-button>
                    </div>
                </div>
            </md-app-toolbar>

            <md-app-drawer :md-active.sync="menuVisible" md-persistent="full" v-if="this.role === 0 || this.role === 1">
                <md-toolbar class="md-transparent" md-elevation="0">
                    <img src="../src/img/logo.png"/>
                </md-toolbar>

                <div class="list-group" v-if="this.role === 1">
                    <a v-on:click="setSelectedItemHome" href="#" class="list-group-item"><label class="labelSide">Home</label><md-icon class="position">home</md-icon></a>
                    <a v-on:click="setSelectedItemEmpresaInfo" href="#" class="list-group-item"><label class="labelSide">Mi perfil</label><md-icon class="position">local_play</md-icon></a>
                    <a v-on:click="setSelectedItemEmpresaView" href="#" class="list-group-item"><label class="labelSide">Empresa</label><md-icon class="position">local_play</md-icon></a>
                </div>
                <div class="list-group" v-if="this.role === 0">
                    <a v-on:click="setSelectedItemHome" href="#" class="list-group-item"><label class="labelSide">Home</label><md-icon class="position">home</md-icon></a>
                    <a v-on:click="setSelectedItemAdminView" href="#" class="list-group-item"><label class="labelSide">Estadísticas generales</label><md-icon class="position">local_play</md-icon></a>
                    <a v-on:click="setSelectedItemAdminEdit" href="#" class="list-group-item"><label class="labelSide">Editar encuesta</label><md-icon class="position">local_play</md-icon></a>
                   <a v-on:click="setSelectedItemAdminInfo" href="#" class="list-group-item"><label class="labelSide">Mi perfil</label><md-icon class="position">local_play</md-icon></a>
                </div>
            </md-app-drawer>

            <md-app-content class="md-content">
                <div>
                    <div v-if="this.eleccion == 1">
                        <home-component v-bind:datos="preguntas"></home-component>
                    </div>
                    <div v-if="this.eleccion == 2">
                        <admin-edit-component v-bind:datos="[usuarios, preguntas]"></admin-edit-component>
                    </div>
                    <div v-if="this.eleccion == 3">
                        <adminGraf-component v-bind:datos="[preguntas]"></adminGraf-component>
                    </div>
                    <div v-if="this.eleccion == 4">
                        <empresa-component v-bind:datos="regiones"></empresa-component>
                    </div>
                    <div v-if="this.eleccion == 5">
                        <admin2-component v-bind:datos="[regiones, encuestados]"></admin2-component>
                    </div>
                    <div v-if="this.eleccion == 6">
                        <admin-edit2-component v-bind:datos="[usuarios, preguntas]"></admin-edit2-component>
                    </div>
                    <div v-if="this.eleccion == 7">
                        <empresa-userInfo-component></empresa-userInfo-component>
                    </div>
                    <div v-if="this.eleccion == 8">
                        <admin-userInfo-component v-bind:datos="usuarios"></admin-userInfo-component>
                    </div>
                </div>
            </md-app-content>
        </md-app>
    </div>
</template>

<style lang="scss" scoped>
    .md-app {
        max-height: 100000px;
        border: 1px solid rgba(#000, .12);
    }
    // Demo purposes only
    .md-drawer {
        width: 230px;
        max-width: calc(100vw - 125px);
    }
    .md-color{
        background-color: #4F8A10;
    }
    .md-content{
        height: 11000px;
    }
    .md-dialog{
        width: 508px;
    }
</style>

<script>
    import home from './home.vue';
    import userForm from './userForm.vue';
    import adminEdit from './adminEdit.vue';
    import adminView from './adminView.vue';
    import empresaView from './empresaView.vue';
    import empresaInfo from './empresaUserInfo.vue';
    import adminEdit2 from './adminEdit2.vue';
    import adminView2 from './adminView2.vue';
    import adminGraf from './adminGraf.vue';
    import adminUserInfo from './adminUserInfo.vue';
    import {
        required,
        email
    } from 'vuelidate/lib/validators'
    import Vue from 'vue'
    import Vuelidate from 'vuelidate'
    Vue.use(Vuelidate)
    export default {
        components: {
            'home-component': home,
            'form-component': userForm,
            'admin-component': adminView,
            'adminGraf-component': adminGraf,
            'admin2-component': adminView2,
            'admin-edit-component': adminEdit,
            'admin-edit2-component': adminEdit2,
            'empresa-component': empresaView,
            'empresa-userInfo-component': empresaInfo,
            'admin-userInfo-component': adminUserInfo
        },
        name: 'Overlap',
        data: () => ({
            load: 0,
            //role 0 = admin; role 1 = empresa; role 2 = usuario natural
            //role: Number(localStorage.getItem('role'))-1,
            role: 0,
            error:false,
            showDialogLogin: false,
            showDialogRegister: false,
            menuVisible: false,
            eleccion: 0,
            nombre: null,
            phone: null,
            region: null,
            email: null,
            password: null,
            isInvalidEmail:false,
            isInvalidPass:false,
            loginjson:null,
            preguntas:null,
            regiones: null,
            usuarios: null,
            encuestados: null,
            usuariosE: null,
        }),
        validations:{
            email: {
                required,
                email
            },
            password:{
                required
            }
        },

        mounted(){

        },
        created() {
            const auth = {
                headers: {'Authorization':'Bearer ' + localStorage.getItem('authtoken')}
            };

            let roleAdmin ={
                headers: {'Authorization':'Bearer ' + 'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250cmFzZW5hIjoiYXNkZiIsInJvbCI6MSwiY29ycmVvIjoiYWRtaW5AbWFpbC5jbCIsImFjdGl2byI6dHJ1ZX0.TrVdJeaJ5km92RKv2hI0yot8gWwtON3azO1qPvfdjZ0'}
            };

            this.$http.get('http://134.209.49.245:8080/mongodb-v1/categories/all',auth).then(response => {
                this.preguntas = response.data;
                console.log('data de preguntas obtenido es:', this.preguntas);
                this.eleccion = 1;
                this.load += 33
            }, (response) => {
                this.error = true;
                console.log('no obtiene preguntas');
            });

            this.$http.get('http://134.209.49.245:8080/mongodb-v1/regiones/all',auth).then(response => {
                this.regiones = response.data;
                console.log('data de regiones obtenido es:', this.regiones);
                this.eleccion = 1;
                this.load += 33
            }, (response) => {
                this.error = true;
                console.log('no obtiene regiones');
            });
            this.$http.get('http://134.209.49.245:8080/mongodb-v1/usuarios/all', roleAdmin).then(response => {
                this.usuarios = response.data;
                console.log('data de usuarios obtenido es:', this.usuarios);
                this.eleccion = 1;
                this.load += 34
            }, (response) => {
                this.error = true;
                console.log('no obtiene usuarios');
            });
            this.$http.get('http://134.209.49.245:8080/mongodb-v1/encuestados/all', roleAdmin).then(response => {
                this.encuestados = response.data;
                console.log('data de encuestados obtenido es:', this.encuestados);
                this.eleccion = 1;
                this.load += 34
            }, (response) => {
                this.error = true;
                console.log('no obtiene encuestados');
            });

            setInterval(function(){
                var hours = 1;
                var now = new Date().getTime();
                var lstime = localStorage.getItem('time');
                if(now-lstime > hours*60*60*1000){
                    localStorage.clear();
                } }, 5*60*1000);

        },

        methods: {
            setSelectedItemHome(){
                this.eleccion=1;
            },
            setSelectedItemAdminEdit(){
                this.eleccion=2;
            },
            setSelectedItemAdminView(){
                this.eleccion=3;
            },
            setSelectedItemEmpresaView(){
                this.eleccion=4;
            },
            setSelectedItemAdminView2(){
                this.eleccion=5;
            },
            setSelectedItemAdminEdit2(){
                this.eleccion=6;
            },
            setSelectedItemEmpresaInfo(){
                this.eleccion=7;
            },
            setSelectedItemAdminInfo(){
              this.eleccion=8;
            },
            servicioLogin(){
                const config = {
                    headers: {'Content-Type': 'application/json'}};
                this.loginjson = {
                    correo: this.email,
                    contrasena: this.password
                }

                this.$http.post('http://134.209.49.245:8080/mongodb-v1/usuarios/login',JSON.stringify(this.loginjson),config).then((response) => {
                    localStorage.setItem('authtoken',response.body.Authorization);
                    localStorage.setItem('name',response.body.nombre);
                    localStorage.setItem('role',response.body.rol);
                    localStorage.setItem('time', new Date().getTime());
                    console.log("Se hizo el login",response);
                }, (response) =>{
                    console.log("No se logro el login",response)
                });

            },
            servicioLogout(){
                localStorage.clear();
            }
        },
        ready: function() {
            $('.dropdown-submenu a.test').on("click", function(e){
                $(this).next('ul').toggle();
                e.stopPropagation();
                e.preventDefault();
            });
        }
    }
</script>

<style scoped>
    .position {
        position: absolute;
        right: 15px;
    }
    .md-toolbar.md-theme-default.md-accent {
        background-color: #202C39;
    }
    .md-toolbar.md-theme-default.md-accent .md-title{
    @import url('https://fonts.googleapis.com/css?family=Francois+One');
        font-family: 'Lobster Two', cursive;
        font-size: 35px;
        color: #FABC3C;
        margin-left: 20px;
    }
    .md-drawer.md-theme-default {
        background-color: #202C39;
    }
    a.list-group-item:focus, a.list-group-item:hover, button.list-group-item:focus, button.list-group-item:hover {
        background-color: #4F5C66;
    }
    a.list-group-item{
        background-color: #202C39;
    }
    .labelSide{
    @import url('https://fonts.googleapis.com/css?family=Francois+One');
        font-family: 'Francois One', sans-serif;
        font-size: 18px;
        color: #F2D492;
    }
    .md-content.md-theme-default{
        background-color: #FDFBF5;
    }
    body{
        background: #FAEFD7 ;
    }
    p {
        background-image: url("img/logo.png");
    }
</style>