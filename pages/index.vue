<template>
  <div class="home-container">
    <CookieHeader headerMessage="Software with a sweet side" />
    <h1>Projects</h1>
    <hr />
    <div class="projects-container">
      <ProjectCard v-for="project in projects" 
        :key="project.id"
        :id="project.id"
        :name="project.name"
        :description="project.description"
        :leftAligned="project.leftAligned"
        :url="project.projectPageUrl"
        :image="project.imageUrl"
        class="project-wrapper"
      />
    </div>
  </div>
</template>

<script>
import CookieHeader from '../components/CookieHeader';
import ProjectCard from '../components/ProjectCard';

export default {
  components: {
    CookieHeader,
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
          projectPageUrl: 'https://github.com/CookieDev-Studio/Sharp',
          imageUrl: 'sharp-screenie.png'
        },
        {
          id: 2,
          name: 'Website',
          description: 'The Cookie Dev Studio site is a web app built on Nuxt.js.',
          leftAligned: true,
          projectPageUrl: 'https://github.com/CookieDev-Studio/Website',
          imageUrl: 'website-screenie.jpg'
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

.home-container > h1 {
  color: #333;
  font-size: 34px;
  text-align: center;
  margin: 30px 0 10px 0;
  padding-bottom: 5px;
}

.home-container > hr {
  width: 30vw;
  align-self: center;
}

.projects-container {
  width: 100vw;
  max-width: 860px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  align-self:center;
}

</style>