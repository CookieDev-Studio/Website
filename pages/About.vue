<template>
    <div class="about-container">
        <CookieHeader headerMessage="About Us" />

        <h1>Devs with a sweet tooth</h1>
        <hr />
        <div class="about-text-wrapper">
            <p>Cookie Dev Studio is a group of software devs who've come together to make some open source software. Committed to writing efficient, scaleable and maintainable code, Cookie Dev is excited to build tools and products people find pleasant and efficient to use.</p>
            <p>We write our software with tried-and-true technologies. Our skillset includes:</p>
            <ul>
                <li>C#</li>
                <li>.NET Core 3.1</li>
                <li>JavaScript (ES7)</li>
                <li>Vue.js and Nuxt.js</li>
                <li>Postgresql</li>
            </ul>
            <br />
            <p>We iterate quickly over web sites and web applications off all kinds as well as various other projects (ex. Discord bots!). If you have an app idea, we'd love to hear it! Feel free to visit our <a href="/Contact">contact page</a>.</p>
            <div class="button-group">
                <p>If you would like to get to know us better, visit our GitHub <v-btn text class="btn" color="primary" href="https://github.com/CookieDev-Studio" target="_blank">here!</v-btn></p>
                <p>If you would like to see our projects, click <v-btn text class="btn" color="primary" href="/">here!</v-btn></p>
                <p>If you'd like to consider supporting us on Patreon, click <v-btn text class="btn" color="primary" href="https://patreon.com/cookiedevstudio" target="_blank">here!</v-btn></p>
            </div>
        </div>
        <div class="team-header">
            <h1>The Team</h1>
        </div>
        <div class="images-wrapper">
            <div class="team-member">
                <div class="team-img" id="cam" />
                <div class="team-description">
                    <h2>Cam</h2>
                    <hr />
                    <p>Back-end Developer</p>
                </div>
            </div>
            <div class="team-member">
                <div class="team-img" id="zach" />
                <div class="team-description">
                    <h2>Zach</h2>
                    <hr />
                    <p>Full-stack Developer</p>
                </div>
            </div>
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
.about-container {
  width: 100vw;
  display: flex;
  flex-direction: column;
}

.about-container > h1 {
  color: #333;
  font-size: 34px;
  text-align: center;
  margin: 30px 0 10px 0;
  padding-bottom: 5px;
}

.about-container > hr {
  width: 30vw;
  align-self: center;
}

.about-text-wrapper {
    font-size: 18px;
    line-height: 1.3;
    max-width: 860px;
    width: 85vw;
    margin: 20px 0;
    align-self: center;
}

.button-group {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.button-group .btn {
    padding: 0 !important;
    margin-top: -2px;
    font-size: 18px;
} 

.team-header {
    width: 100%;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25); 
    text-align: center; 
    z-index: 11;
}

.images-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    background: #ddd;
    box-shadow: 0 -8px 4px -4px inset rgba(0, 0, 0, 0.25);
    z-index: 9;
}

.team-img {
    width: 300px;
    max-width: 300px;
    height: 300px;
    flex-grow: 1;
    margin: 20px;
    border: 2px solid #a5844c;
    border-radius: 15px;
}

.images-wrapper #cam {
    background-image: url('../static/cam.jpg');
    background-position: center;
    background-size: cover;
}

.images-wrapper #zach {
    background-image: url('../static/zach.jpg');
    background-position: center;
    background-size: cover;
}

.team-description {
    background: rgba(20, 20, 20, 0.75);
    width: 70%;
    display: flex;
    flex-direction: column;
    margin: auto;
    border-radius: 5px;
    margin-bottom: 20px;
    padding: 20px;    
}

.team-description h2 {
    font-size: 26px;
    color: #ccc;
}

.team-description hr {
    width: 50%;
    margin-bottom: 15px;
}

.team-description p {
    color: #eaba8e;
    font-size: 14px;
}
</style>