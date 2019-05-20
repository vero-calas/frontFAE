<template>

    <div class="container">
        <div class="row">
            <div class="col-md-5  toppad  pull-right col-md-offset-3 ">
                <br>
            </div>
            <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6 col-xs-offset-0 col-sm-offset-0 col-md-offset-3 col-lg-offset-3 toppad" >


                <div class="panel panel-info">
                    <div class="panel-heading">
                        <h3 class="panel-title">{{datos[0].nombre}}</h3>
                    </div>
                    <div class="panel-body">
                        <div class="row">
                            <div class="col-md-3 col-lg-3 " align="center"> <img alt="User Pic" src="../src/img/usuario.png" class="img-circle img-responsive"> </div>
                            <div class=" col-md-9 col-lg-9 ">
                                <table class="table table-user-information">
                                    <tbody>
                                    <tr>
                                        <td>E-mail:</td>
                                        <td>{{datos[0].correo}}</td>
                                    </tr>
                                    <tr>
                                        <td>Teléfono</td>
                                        <td>{{datos[0].telefono}}</td>
                                    </tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                    <div class="panel-footer">
                       <span class="pull-right">
                        </span>
                    </div>

                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "empresaUserInfo.vue",
        props: ['datos'],
        data: () => ({


        }),
        created(){


        }


    }
</script>

<style scoped>

</style>