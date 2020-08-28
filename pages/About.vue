<template>
    <div class="about-container">
        <CookieHeader headerMessage="About Us" />

        <h1>Devs with a sweet tooth</h1>
        <hr />
        <div class="about-text-wrapper">
            <p>Cookie Dev Studio is a pair of devs who've come together to make some open source software. Committed to writing efficient, scaleable and maintainable code, Cookie Dev is excited to build tools and products people find pleasant and efficient to use.</p>
            <div class="skillset-title">
                <hr />
                <p>Our skillset includes</p>
                <hr />
            </div>
            <ul>
                <li id="csharp" @click="toggleSkillInfo">
                    <div class="skill-info">C# programming language for the back-end.</div>
                </li>
                <li id="dotnet" @click="toggleSkillInfo">
                    <div class="skill-info">
                        .NET Core framework for our back-end.
                    </div>
                </li>
                <li id="javascript" @click="toggleSkillInfo">
                    <div class="skill-info">
                        JavaScript (ES7)  for the front-end.
                    </div>
                </li>
                <li id="vue" @click="toggleSkillInfo">
                    <div class="skill-info">
                        Vue.js framework for the front-end.
                    </div>
                </li>
                <li id="postgres" @click="toggleSkillInfo">
                    <div class="skill-info">
                        Postgresql for our data.
                    </div>
                </li>
            </ul>
            <hr />
            <br />
            <p>We rapidly iterate over a wide variety of projects targetting the web, consoles, and other neat stuff (ex. Discord bots!). If you have an app idea, we'd love to hear it! Feel free to visit our <a href="/Contact">contact page</a>.</p>
            <p id="button-group-precursor">You can learn more about our projects here:</p>
            <div class="button-group">
                <v-btn class="btn" to="/">Projects</v-btn>
                <v-btn class="btn" href="https://github.com/CookieDev-Studio" target="_blank">Github</v-btn>                
            </div>
            <p>If you like our work and want to support us:</p>
            <a href="https://patreon.com/cookiedevstudio" target="_blank" class="patreon-cta">
                <img src="../static/Digital-Patreon-Logo_White.png" alt="Patreon logo" /> Become a Patron
            </a>            
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
    },
    methods: {
        toggleSkillInfo: (e) => {
            if (e.target.classList.contains('skill-info')) {
                const info = e.target;
                info.classList.remove('show-info');
                return;
            }

            const info = e.target.children[0];

            if (info.classList.contains('show-info')) {
                info.classList.remove('show-info');
            } else {
                const siblings = Array.from(e.target.parentElement.children);

                siblings.forEach(sibling => 
                    sibling.children[0].classList.remove('show-info'));

                info.classList.add('show-info');
            }
        }
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

.about-text-wrapper p {
    text-align: center;
}

.about-text-wrapper ul {
    list-style-type: none;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 20px;
}

.about-text-wrapper li {
    border: 1px solid #ccc;
    border-radius: 50%;
    width: 100px;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
    text-align: center;
    cursor: pointer;
}

.about-text-wrapper li .skill-info {
    display: none;
    margin-top: 60px;
    background:rgba(20, 20, 20, .95);
    color: #fff;
    padding: 20px;
    font-size: 16px;
    border-radius: 10px;
    max-width: 600px;
    width: 30vw;
    height: auto;
    z-index: 5;
}

.about-text-wrapper > hr {
    width: 90%;
    display: flex;
    justify-self: center;
    align-self: center;
    margin: 30px auto;
}

.show-info {
    display: inline-block !important;
    position: absolute;
}

#csharp {
    background-image: url('../static/csharp-logo.png');
    background-position: center;
    background-size: cover;
}

#dotnet {
    background-image: url('../static/dotnetcorelogo.png');
    background-position: center;
    background-size: cover;
}

#javascript {
    background-image: url('../static/js-logo.png');
    background-position: center;
    background-size: cover;
}

#vue {
    background-image: url('../static/vuelogo.png');
    background-position: center;
    background-size: cover;
}

#postgres {
    background-image: url('../static/postgres-logo.png');
    background-position: center;
    background-size: cover;
}

.skillset-title {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
}

.skillset-title hr, .skillset-title p {
    display: inline;
}

.skillset-title hr {
    width: 20vw;
    align-self: center;
}

.skillset-title p {
    font-weight: bold;
    text-align: center;
    align-self: center;
    margin-bottom: 0;
    margin-left: 30px;
    margin-right: 30px;
}

.button-group {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-bottom: 50px;
}

.button-group .btn {
    font-size: 18px;
    margin: 0 20px;
    padding: 25px;
    font-weight: bold;
} 

.patreon-cta {
    display: flex;
    align-items: center;
    justify-content: center;
    background: #FF424D;
    padding: 15px;
    text-transform: uppercase;
    text-decoration: none;
    font-size: 22px;
    color: #fff;
    width: 50%;
    margin: auto;
}

.patreon-cta > img {
    width: 40px;
    margin-right: 20px;
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
    background: rgba(20, 20, 20, 0.85);
    width: 70%;
    display: flex;
    flex-direction: column;
    margin: auto;
    border-radius: 5px;
    margin-bottom: 20px;
    padding: 20px;
    box-shadow: 1px 1px 10px #000;
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

@media (max-width: 670px) {
    .about-text-wrapper ul {
        flex-wrap: wrap;
        padding: 0 !important;
    }

    .about-text-wrapper ul li {
        margin-top: 10px;
        margin-bottom: 10px;
        width: 150px;
        height: 150px;
    }

    .show-info {
        display: none !important;
    }
}

@media (max-width: 500px) {
    .about-text-wrapper ul li {
        width: 100px;
        height: 100px;
    }

    #button-group-precursor {
        margin-top: 30px;
        display: inline-block;
    }

    .button-group {
        margin-bottom: 60px;
    }

    .patreon-cta {
        width: 80vw;
    }

    .images-wrapper {
        flex-direction: column;
    }

    .team-img {
        width: 200px;
        max-width: 200px;
        height: 200px;
    }

    .team-description {
        margin-bottom: 40px;
        width: 60%;
        padding: 10px;
    }

    .team-description h2 {
        font-size: 20px;
    }

}
</style>