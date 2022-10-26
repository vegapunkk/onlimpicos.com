<template>
    <b-row class="vh-100 vw-100 row-login">
        <b-col sm="5" class="d-flex justify-content-center align-items-center left-login">
            <div class="col-8">
                <b-form>
                    <b-form-group
                      label=""
                      label-for=""
                      >
                        <b-form-input
                          id="email"
                          type="email"
                          placeholder="Email ou Telefone"
                          autocomplete="off"
                          v-model="form.email"
                        ></b-form-input>
                    </b-form-group>

                    <b-form-group
                      label=""
                      label-for="password"
                      >
                        <b-form-input
                          id="password"
                          type="password"
                          placeholder="Senha"
                          v-model="form.password"
                        ></b-form-input>

                        <small><a href="#">Esqueceu sua senha?</a></small>

                    </b-form-group>

                    <b-button
                      type="button"
                      variant="primary"
                      block
                      @click="login">
                      <i class="fas fa-sign-in-alt"></i>Login
                    </b-button>

                    <hr>

                    <b-button
                      type="button"
                      variant="link"
                      block
                      @click="register">
                      <i class="fas fa-user-plus"></i>Registrar-se
                    </b-button>
                </b-form>
            </div>
        </b-col>
        <b-col sm="7" class="d-flex justify-content-center align-items-center">
            <img src="src\assets\image 1.jpg" class="img-login" />
        </b-col>
    </b-row>
</template>

<script>
import {required, minLength, email} from "vuelidate/lib//validators";

export default{
    data() {
        return{
            form: {
                email: "",
                password:""
            }
        }
    },

    validations:{
        form: {
            email: {
                required,
                email
            },

            password: {
                required,
                minLength: minLength(6)
            },
        }
    },

    methods: {
        login(){
            this.$v.$touch();
            if(this.$v,$error) {
                return;
            }
        },

        register() {}
    }
}

</script>

<style>
*,
*::after,
*::before {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    text-decoration: none;
}

.row-login {
    margin-left: 0;
}

.left-login{
    background-color: #E0D6D0;
}

.img-login{
    width: 600px;
    height: 600px;
}
</style>