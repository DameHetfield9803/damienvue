<template>
  <h1 class="header p-3 max-w-xs mx-auto bg-black rounded-xs shadow-xs flex-auto items-center" style="color: aqua">
    Hello there!
  </h1>
  <br />
  <div class="intro1 bg-black max-h-screen">
    <a href="../assets/logo.png" />

    <body class="pageBody">
      My name is Damien, and I am a developer that primarily uses C++ and C. Currently I'm
      trying to get into different web development frameworks such as vue.js and as it
      offers me a bigger perspective on how to create and style websites for production.
      To me, knowing low level codes are definitely important, but they require a website
      to document them. Which lead me to the rabid hole of exploring different web
      development frameworks.
    </body>
  </div>
  <br />
  <div class="codeintro bg-slate-300 text-violet-600 flex-auto grid place-content-center">
    <p>
      I usually enjoy writing codes that are similar to the code block that you will see
      below.
    </p>
    <br />
  </div>
  <div
    class="code1 mx-auto rounded-xl flex text-lg bg-slate-950 text-pink-600 mt-7 border-r-8 border-l-8 p-3 max-w-screen-xs max-h-screen-xs">
    <code>
        <pre>
    <code class="cpp">
            #include cstdio;
            int main() {
                printf("Hello World \n");
                return 0; }
            //Uses the c library to print out hello world using c++.
            </code>
  <code class="c">
            //Whereas in C, it's written like this 
            #include stdio.h;
            int main() {
                printf("Hello World \n");
                return 0;
            }
            </code>
  </pre>
    </code>
  </div>
</template>

<script setup></script>

<style scoped>
.header {
  display: flex;
  max-width: fit-content;
  max-height: fit-content;
  margin-bottom: 1.2rem;
  padding: 0.4rem;
  border-radius: 1rem;
  box-shadow: 0 10px 15px -5px rgba(100, 120, 80, 1),
    0 5px 10px -10px rgba(20, 80, 100, 1);
}

pre {
  white-space: pre-wrap;
  white-space: -moz-pre-wrap;
  word-wrap: break-word;
}

.intro1 {
  color: rgb(231, 94, 139);
  display: flex;
  max-width: 23rem;
  margin: 0 auto;
  padding: 0.8rem;
  border-radius: 1.4rem;
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
}

.codeintro {
  font-size: larger;
  font-family: sans-serif;
  display: flow-root;
  max-width: fit-content;
  margin: 0 auto;
  margin-top: 0.2rem;
  padding: 0.3rem;
  box-shadow: 0 10px 20px -8px;
  border-radius: 0.5rem;
}

.code1 {
  border-radius: 1.2rem;
  display: inline-block;
  display: flex-auto;
  max-width: fit-content;
  align-content: center;
  text-align: left;
  padding-right: 16rem;
  border-left-width: -2rem;
  margin-top: 20px;
  text-wrap: wrap;
  box-shadow: 0 10px 20px -8px;
}
</style>
