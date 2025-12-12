<template>
  <HomeTemplate 
    :languages="languages"
    :isLoading="isLoading"
    @download="downloadPDF"
  />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import HomeTemplate from "@/components/templates/HomeTemplate.vue";

@Options({
  components: { HomeTemplate }
})
export default class Home extends Vue {
  isLoading = true;
  languages= [
        {
          imageUrl: require("@/assets/images/lang/c.png"),
          text: 'I am skilled in using pointers, dynamic memory allocation, and file handling. Additionally, I have extensive experience with system-level programming, optimizing code for performance, and writing efficient multithreaded applications.',
          progress: 90,
          isHovered: false
        },
        {
          imageUrl: require("@/assets/images/lang/ccpp.png"),
          text: 'My experience includes memory management, concurrency, template metaprogramming, and performance optimization, ensuring efficient and scalable software development.',
          progress: 90,
          isHovered: false
        },
        {
          imageUrl: require("@/assets/images/lang/python.png"),
          text: 'I\'m experienced in modern libraries for data processing, web development, and machine learning, and skilled in writing efficient, scalable, and maintainable code using type hints, generators, multiprocessing, and metaprogramming.',
          progress: 90,
          isHovered: false
        },
        {
          imageUrl: require("@/assets/images/lang/bash.png"),
          text: 'I\'m skilled in writing efficient and modular scripts, utilizing pipes, redirections, background processes, and regular expressions to streamline workflows and automate tasks.',
          progress: 75,
          isHovered: false
        },
        {
          imageUrl: require("@/assets/images/lang/sql.png"),
          text: 'I am experienced in writing optimized queries, designing normalized schemas, using indexes effectively, and managing data through views, joins, and stored procedures.',
          progress: 75,
          isHovered: false
        },
        {
          imageUrl: require("@/assets/images/lang/js.png"),
          text: 'With experience in ES6+ features, asynchronous programming (Promises, async/await), and DOM manipulation.',
          progress: 60,
          isHovered: false
        },
        {
          imageUrl: require("@/assets/images/lang/ts.png"),
          text: 'I am skilled in developing scalable and maintainable applications, leveraging TypeScript’s static typing to improve code quality and reduce runtime errors',
          progress: 60,
          isHovered: false
        },
        {
          imageUrl: require("@/assets/images/lang/xs.png"),
          text: 'With experience in object-oriented programming, LINQ, MVC, and asynchronous programming',
          progress: 50,
          isHovered: false
        },
        {
          imageUrl: require("@/assets/images/lang/java.png"),
          text: 'I\'m familiar with object-oriented programming, multithreading, collections framework, and basic Android development, as well as writing modular and maintainable code using interfaces, generics, and lambda expressions',
          progress: 45,
          isHovered: false
        },
        {
          imageUrl: require("@/assets/images/lang/PHP.png"),
          text: 'With experience in server-side scripting, form handling, and database interactions using MySQL. ',
          progress: 45,
          isHovered: false
        },
        {
          imageUrl: require("@/assets/images/lang/rust.png"),
          text: 'I\'m familiar with Cargo, error handling, and multithreading, and have experimented with writing safe and efficient code using Rust’s memory management model.',
          progress: 20,
          isHovered: false
        }
      ];
  
  mounted() {
    setTimeout(() => this.isLoading = false, 2000);
  }

  downloadPDF() {
    const link = document.createElement("a");
    link.href = 'docs/CV-ASDV.pdf';
    link.download = "ASDV_Curriculum_vitae.pdf";
    link.target = "_blank";
    link.click();
  }
}
</script>