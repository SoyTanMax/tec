<template>
    <div>
        <button class="button login-button" @click="showModal = !showModal">
            Registrarse
        </button>
        <div class="modal" :class="{ 'is-active': showModal, 'is-clipped': showModal }">
            <div class="modal-background"></div>
            <div class="modal-content">
                <div class="box">
                    <div class="has-text-centered has-text-weight-medium is-size-5 inicia">Llena el formulario de solicitud</div>
                    <form @submit.prevent>
                        <div class="field">
                            <div class="control">
                                <label for="nombre" class="label">Nombre de la organización</label>
                                <input type="text" class="input" id="nombre">
                            </div>
                        </div>
                        <div class="field">
                            <div class="control">
                                <label for="correo" class="label">Correo electrónico</label>
                                <input type="email" class="input" id="correo">
                            </div>
                        </div>
                        <div class="field">
                            <div class="control">
                                <label for="razon" class="label">Razón</label>
                                <textarea type="text" class="razon" id="razon"></textarea>
                            </div>
                        </div>
                        <button class="button is-fullwidth login has-text-white has-text-weight-bold">Enviar</button>
                    </form>
                </div>
            </div>
            <button class="modal-close is-large" @click="showModal = !showModal"></button>
        </div>

    </div>
</template>

<script>
    export default {
        name: 'Signup',
        data() {
            return {
                showModal: false
            }
        },
    }
</script>

<style scoped>
.login-button{
    border: none;
    background: hsl(209, 75%, 45%);
    font-family: 'Manrope', sans-serif;
    border-radius: 8px;
    font-size: 14px;
    color: white;
    padding: 20px 32px;
    font-weight: 700;
}
/* modal */
.box{
    padding: 48px 84px;
    font-family: 'Manrope', sans-serif;
}
.inicia{
    margin-bottom: 48px;
}
.label{
    color: rgb(116, 116, 116);
    font-weight: 500;
}
.field{
    margin-bottom: 24px;
}
.login{
    border: none;
    border-radius: 8px;
    background: hsl(209, 75%, 36%);
    height: 48px;
    font-family: 'Manrope', sans-serif;
}
.modal{
    z-index: 99;
}
.razon{
    height: 150px;
    width: 100%;
    border: 1px solid #e4e4e4;
    border-radius: 8px;
    box-shadow: none;
    padding: 8px;
}
@media screen and (max-width: 1024px){
    .login-button{
        background:  hsl(204, 92%, 58%);
        color: white;
        width: 100%;
    }
}
</style>