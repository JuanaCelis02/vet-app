<template>
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link rel="stylesheet" href="/css/styles.css">
        <!-- <script src="https://www.google.com/recaptcha/api.js" async defer></script> -->
        <div class="g-recaptcha" data-sitekey="tu-clave-de-sitio-recaptcha"></div>
        <title>Login</title>
    </head>

    <body>
        <section>
            <h2>Login Veterinaria</h2>
            <form id="loginForm">
                <label>Mail</label>
                <input type="email" placeholder="..." id="email" required autofocus>
                <label>Contraseña</label>
                <input type="password" placeholder="..." id="password" required>
                <input type="submit" value="Ingresar">
                <div class="g-recaptcha" data-sitekey="6LfF1PQnAAAAABAKnlDnQdragoFNGYkOx3anuxqz"></div>
            </form>
            <p>No tienes una cuenta? <a href="/html/signup.html">Registro</a></p>
        </section>
        <!-- <script src="/js/login.js"></script> -->
    </body>
</template>

<script lang="ts">
export default {
    mounted() {
    // Cargar el script de Google reCAPTCHA después de que se cargue la página
    const script = document.createElement('script');
    script.src = 'https://www.google.com/recaptcha/api.js';
    script.async = true;
    script.defer = true;
    
    // Agregar el script al final del cuerpo del documento
    document.body.appendChild(script);

    // Ahora puedes utilizar las funciones de reCAPTCHA después de que se cargue
    // Ejemplo de uso:
    // grecaptcha.render('tu-elemento-recaptcha', {
    //   sitekey: 'tu-clave-de-sitio-recaptcha',
    //   // Otras opciones personalizadas
    // });
    }
}
</script>

<style scoped></style>