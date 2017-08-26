<style scoped>

.form {
    width: 50%;
}

</style>

<template>

<div class="form">
    <i-form ref:form-validate :model="formValidate" :rules="ruleValidate" :label-width="80">
        <Form-item label="Nombre" prop="name">
            <i-input v-model="formValidate.name" placeholder="Introduzca un nombre"></i-input>
        </Form-item>
        <Form-item label="Email" prop="mail">
            <i-input v-model="formValidate.mail" placeholder="Introduzca un email"></i-input>
        </Form-item>
        <Form-item label="Ciudad" prop="city">
            <i-select :value.sync="formValidate.city" placeholder="Elija su ubicación">
                <i-option value="Caracas">Caracas</i-option>
                <i-option value="New York">New York</i-option>
                <i-option value="Londres">Londres</i-option>
            </i-select>
        </Form-item>
        <Form-item label="Seleccionar fecha">
            <Row>
                <i-col span="11">
                    <Form-item prop="date">
                        <Date-picker type="date" placeholder="Seleccionar fecha" v-model="formValidate.date"></Date-picker>
                    </Form-item>
                </i-col>
                <i-col span="2" style="text-align: center">-</i-col>
                <i-col span="11">
                    <Form-item prop="time">
                        <Time-picker type="time" placeholder="Elige el tiempo" v-model="formValidate.time"></Time-picker>
                    </Form-item>
                </i-col>
            </Row>
        </Form-item>
        <Form-item label="Sexo" prop="gender">
            <Radio-group v-model="formValidate.gender">
                <Radio label="male">Hombre</Radio>
                <Radio label="female">Mujer</Radio>
            </Radio-group>
        </Form-item>
        <Form-item label="Aficiones" prop="interest">
            <Checkbox-group v-model="formValidate.interest">
                <Checkbox label="Comer"></Checkbox>
                <Checkbox label="Dormir"></Checkbox>
                <Checkbox label="Correr"></Checkbox>
                <Checkbox label="Ver películas"></Checkbox>
            </Checkbox-group>
        </Form-item>
        <Form-item label="Introducción" prop="desc">
            <i-input v-model="formValidate.desc" type="textarea" :autosize="{minRows: 2,maxRows: 5}" placeholder="Por favor ingrese..."></i-input>
        </Form-item>
        <Form-item>
            <i-button type="primary" @click.native="handleSubmit('formValidate')">Enviar</i-button>
            <i-button type="ghost" @click.native="handleReset('formValidate')" style="margin-left: 8px">Restablecer</i-button>
        </Form-item>
    </i-form>

</div>

</template>

<script>

export default {
    data() {
            return {
                formValidate: {
                    name: '',
                    mail: '',
                    city: '',
                    gender: '',
                    interest: [],
                    date: '',
                    time: '',
                    desc: ''
                },
                ruleValidate: {
                    name: [{
                        required: true,
                        message: 'El nombre no puede estar vacío',
                        trigger: 'blur'
                    }],
                    mail: [{
                        required: true,
                        message: 'El email no puede estar vacío',
                        trigger: 'blur'
                    }, {
                        type: 'email',
                        message: 'El formato del email es incorrecto',
                        trigger: 'blur'
                    }],
                    city: [{
                        required: true,
                        message: 'Por favor seleccione la ciudad',
                        trigger: 'change'
                    }],
                    gender: [{
                        required: true,
                        message: 'Por favor seleccione sexo',
                        trigger: 'change'
                    }],
                    interest: [{
                        required: true,
                        type: 'array',
                        min: 1,
                        message: 'Elegir al menos una afición',
                        trigger: 'change'
                    }, {
                        type: 'array',
                        max: 2,
                        message: 'Elige hasta dos pasatiempos',
                        trigger: 'change'
                    }],
                    date: [{
                        required: true,
                        type: 'date',
                        message: 'Por favor, seleccione la fecha',
                        trigger: 'change'
                    }],
                    time: [{
                        required: true,
                        type: 'date',
                        message: 'Seleccione la hora',
                        trigger: 'change'
                    }],
                    desc: [{
                        required: true,
                        message: 'Ingrese una introducción personal',
                        trigger: 'blur'
                    }, {
                        type: 'string',
                        min: 20,
                        message: 'La introducción no puede ser inferior a 20 palabras',
                        trigger: 'blur'
                    }]
                }
            }
        },
        methods: {
            handleSubmit(name) {
                    this.$Message.success('Esta es una sugerencia exitosa');
                },
                handleReset(name) {
                    this.$Message.warning('Esto es una advertencia');
                }
        }
}

</script>
