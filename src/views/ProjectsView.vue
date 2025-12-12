<template>
    <ProjectsTemplate
    :isLoading="isLoading"
    :projects="projects"
    />
  </template>
  
  <script lang="ts">
  import { Options, Vue } from "vue-class-component";
  import ProjectsTemplate from "@/components/templates/ProjectsTemplates.vue";
  
  @Options({
    components: {
        ProjectsTemplate
    },
  })
  export default class Project extends Vue {
    isLoading = true;
    projects= [
        {
          image: "pokemonRL.png",
          title: "Pokémon Emerald RL Agent",
          description: "A deep reinforcement learning agent trained with DQN to autonomously play and complete Pokémon Emerald",
          skills: ["DQN", "CNN", "LibTorch", "exploration vs exploitation"],
          github: "https://github.com/AndresTY/Pok-mon-Emerald-RL-Agent"
        },
        {
          image: "MangekyoCode.png",
          title: "MangekyoCode",
          description: "a modular, containerized online code judge. It provides a secure sandbox for code execution, a REST API, and a modern web interface — all orchestrated via Docker Compose.",
          skills: ["Docker", "Python", "Vue.js", "JavaScript", "Nginx", "Microservice"],
          github: "https://github.com/AndresTY/MangekyoCode"
        },
        {
          image: "IaDetecter.png",
          title: "IA DETECTER",
          description: "academic-oriented monitoring system designed to detect and block the use of AI and LLM-based tools.",
          skills: ["Python", "Cross-Platform Development ", "Multi-Client Management", "OS Automation","Client-Server Architecture"],
          github: "https://github.com/AndresTY/IA-Detecter"
        },
        {
          image: "WebUPME.png",
          title: "Upme Front RAG Service",
          description: "This is a frontend development intended for consuming a RAG system provided through FastAPI for the Mining and Energy Planning Unit (UPME).",
          skills: ["Frontend Development", "FastAPI Integration", "RAG", "API Consumption"],
          github: "https://github.com/AndresTY/WebUPME"
        },
        {
          image: "Asteroids.png",
          title: "Asteroids",
          description: "It is a recreation of the classic arcade video game Asteroids (1979) developed as a learning project focused on the use of C++ and the SFML library to handle graphics and user input.",
          skills: ["C++", "SFML ", "Game Development", "Keyboard & Controller Input"],
          github: "https://github.com/AndresTY/Asteroids"
        },
        {
          image: "garderov.png",
          title: "Garderov",
          description: "This is a demo of a smart wardrobe using IoT and AI.",
          skills: ["C++", "ESP32","Raspberry Pi", "MQTT", "Sensors","Tensorflow","Web Service"],
          github: "https://github.com/AndresTY/Garderob"
        },
        {
          image: "AWS.png",
          title: "Rekognizer",
          description: "Simple web scraper designed to extract structured information from target websites, deployed using AWS services and automated through a CI/CD pipeline.",
          skills: ["Web Scraping", "AWS Cloud Services", "CI/CD Pipelines", "Python Automation","REST Data Handling"],
          github: "https://github.com/AndresTY/Rekognizer"
        },
      ];
     mounted() {
        setTimeout(() => this.isLoading = false, 2000);
      }
  }
  
  </script>
  