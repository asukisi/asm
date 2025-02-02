<script setup>
import { ref } from "vue";
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Article from "./components/Article.vue";
import Footer from "./components/Footer.vue"

import imgIntel from "./components/icons/assembly-intel.svg";
import imgVax from "./components/icons/assembly-vax.svg"
import imgAMD from "./components/icons/assembly-amd.svg"

const text = ref(
  "VAX (Virtual Address eXtension) — 32-битная компьютерная архитектура, была разработана в середине 1970-x годов Digital Equipment Corporation как развитие линии PDP-11 в рамках проекта Star."
);
const textIntel = ref(
  "x86 assembly language is a family of low-level programming languages that are used to produce object code for the x86 class of processors. These languages provide backward compatibility with CPUs dating back to the Intel 8008 microprocessor, introduced in April 1972.[1][2] As assembly languages, they are closely tied to the architecture's machine code instructions, allowing for precise control over hardware. In x86 assembly languages, mnemonics are used to represent fundamental CPU instructions, making the code more human-readable compared to raw machine code.[3] Each mnemonics corresponds to a basic operation performed by the processor, such as arithmetic calculations, data movement, or control flow decisions. Assembly languages are most commonly used in applications where performance and efficiency are critical. This includes real-time embedded systems, operating-system kernels, and device drivers, all of which may require direct manipulation of hardware resources. Additionally, compilers for high-level programming languages sometimes generate assembly code as an intermediate step during the compilation process. This allows for optimization at the assembly level before producing the final machine code that the processor executes."
);
const img = ref(imgIntel); 
const img2 = ref(imgVax);
const img3 = ref(imgAMD);
</script>

<template>
<Header></Header>
  <Main>
    <Article :imgSource="img" :textArticle="textIntel"></Article>
    <Article :imgSource="img2" :textArticle="text" > </Article>
    <Article :imgSource="img3" :textArticle="text" > </Article>
    <Article :imgSource="img" :textArticle="textIntel" > </Article>
    <Article :imgSource="img3" :textArticle="text" > </Article>
  </Main>
  <Footer></Footer>
</template>
