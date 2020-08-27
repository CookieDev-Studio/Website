<template>
    <div class="contact-container">
        <CookieHeader headerMessage="Reach out" />
        <h1>How to contact</h1>
        <hr />
        <div class="contact-instructions">
            <p>The easiest way to get in contact with us is to reach out to our email at <a href="mailto:cookiedevstudio@outlook.com">cookiedevstudio@outlook.com</a>. If you're interested in talking with us about a project or anything else, feel free to shoot us a message!
            <p>If you would like to contribute code to our projects, they are all open source on our Github <a href="https://github.com/CookieDev-Studio" target="_blank">here</a>. We write our software with C# on .NET Core 3.1, JavaScript with Vue.js and Nuxt.js, and Postgres.</p>
            <p>If you like what you see, please consider donating to us on Patreon! We love what we do and your support helps us out a ton! You can find our Patreon <a href="https://patreon.com/cookiedevstudio" target="_blank">here</a>.</p>
        </div>        
    </div>
</template>

<script>
import CookieHeader from '../components/CookieHeader';

export default {
    components: {
        CookieHeader
    }
}
</script>

<style scoped>
.contact-container {
  width: 100vw;
  display: flex;
  flex-direction: column;
}

.contact-container > h1 {
  color: #333;
  font-size: 34px;
  text-align: center;
  margin: 30px 0 10px 0;
  padding-bottom: 5px;
}

.contact-container > hr {
  width: 30vw;
  align-self: center;
}

.contact-instructions {
    max-width: 860px;
    width: 70vw;
    margin: auto;
    background: #333;
    color: #fff;
    padding: 40px;
    border-radius: 20px;
    margin-top: 20px;
    margin-bottom: 45px;
}

.contact-instructions p, .contact-instructions a {
    font-size: 18px;
    line-height: 1.5;
}

@media (max-width: 440px) {
    .contact-instructions {
        width: 90vw;
        padding: 10px;
    }

    .contact-instructions p, .contact-instructions a {
        font-size: 16px !important;
    }
}
</style>