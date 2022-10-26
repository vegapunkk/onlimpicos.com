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

                    </b-form-group>
                </b-form>
            </div>
        </b-col>
        <b-col sm="7"></b-col>
    </b-row>
</template>

<script>
export default{
    data() {
        return{
            form: {
                email: "",
                password:""
            }
        }
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
</style>