<template>
  <div class="home-container">
    <div class="cookie-header-wrapper">
      <div class="cookie-header">
        <p>Software with a sweet side</p>
      </div>
    </div>
    <div class="cookie-icon-wrapper">
      <div class="cookie-icon"></div>
    </div>
    <div class="projects-container">
      <ProjectCard v-for="project in projects" 
        :key="project.id"
        :id="project.id"
        :name="project.name"
        :description="project.description"
        :leftAligned="leftAligned"
        :url="projectPageUrl"
        :image="imageUrl"
      />
    </div>
  </div>
</template>

<script>
import ProjectCard from '../components/ProjectCard';

export default {
  components: {
    ProjectCard
  },
  data () {
    return {
      projects: [
        {
          id: 1,
          name: 'Sharp',
          description: 'Sharp is a Discord moderation bot built on C# and .NET Core 3.1.',
          leftAligned: false,
          projectPageUrl: '/Sharp',
          imageUrl: '../static/cookiedev.png'
        },
        {
          id: 2,
          name: 'Website',
          description: 'The Cookie Dev Studio site is a web app built on Nuxt.js.',
          leftAligned: true,
          projectPageUrl: '/',
          imageUrl: '../static/cookiedev.png'
        }
      ]
    }
  }
}
</script>

<style scoped>
.home-container {
  width: 100vw;
  display: flex;
  flex-direction: column;
}

.cookie-header-wrapper {
  width: 100vw;
  height: 200px;
  margin: 0;
  padding: 0;
  background-image: url('../static/cookie-header.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  z-index: 1;
}

.cookie-header {
  width: 100vw;
  height: 200px;
  margin: 0;
  padding: 0;
  background-color: rgba(0,0,0, 0.7);
  z-index: 3;
  display: flex;
  align-items: center;
  justify-content: center;
}

.cookie-header p {
  color: #fff;
  font-size: 22px;
  text-align: center;
}

.cookie-icon-wrapper {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background: linear-gradient(180deg, #FFFFFF 0%, rgba(255, 255, 255, 0) 100%), #EEEEEE;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  display: flex;
  align-self: center;
  justify-self: center;
  align-items: center;
  justify-content: center;
  margin-top: -50px;
  z-index: 5;
}

.cookie-icon {
  width: 80px;
  height: 80px;
  background-image: url('../static/cookiedev.png');
  background-size: cover;
  background-position: center;
  z-index: 6;
}
</style>