<template>
    <div>
        <h2>Formulario de Registro</h2>
        <Form :validation-schema="schema" @submit="onSubmit">
            <div class="form">
                <label for="nombre">Nombre:</label>
                <Field id="nombre" name="nombre" type="text" placeholder="Ingrese su nombre" />
                <ErrorMessage name="nombre"></ErrorMessage>
            </div>            
            <div class="form">
                <label for="correo">Correo:</label>            
                <Field type="email" id="correo" name="correo" placeholder="Ingrese su Email" />
                <ErrorMessage name="correo"></ErrorMessage>                
            </div>            
            <div class="form">
                <button type="submit">Registrar</button>
            </div>            
        </Form>        
    </div>
</template>

<script setup>
    import {Form, Field, ErrorMessage} from 'vee-validate';
    import {schema} from '../schemas/validationSchema';

    const onSubmit = () =>{
        console.log('Envio de form');
    };

</script>

<style scoped>
    .form {
        margin-bottom: 10px;
    }
</style>
