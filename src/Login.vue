<template class="login">
    <div class="mb-3">
       <form action="">
           <h2>Pagina de Login</h2>
           <div>
                <input type="text" class="form-control" placeholder="Admin" aria-label="Username" aria-describ v-model="login" />
           </div>
            <div>
                <input type="password" class="form-control" placeholder="Senha" aria-label="Username" aria-describ v-model="senha" />
            </div>
            <div>
                <button type="submit" class="btn btn-primary" @click="logar">Logar</button>
            </div>
       </form>
    </div>
</template>

<script>
    export default {
        name: 'TelaLogin',
        data() {
            return {
                login: '',
                senha: '',
            }
        },
        methods: {
            logar() {
                if (this.login === 'admin' && this.senha === '123') {
                    alert('Logado com sucesso!')
                } else {
                    alert('Login ou senha incorretos!')
                }
            }
        }
    }
</script>

<style scoped>
    div {
        padding: 10px;
    }

    h2 {
        text-align: center;
        padding: 10px;
        font: optional;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        color: blue;
    }

    input {
        margin: 10px;
    }

    button {
        margin: 10px;
    }

    .mb-3 {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        background: rgb(245, 247, 248);
    }

    form {
        justify-content: center;
        align-items: center;
        border: 2px solid #ccc;
        border-radius: 10px;
    }

    .form-control {
        width: 200px;
    }

    .btn {
        margin-top: 10px;
    }

</style>