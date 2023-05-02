<template>
  <div class="mt-8">
    <h2
      class="mt-6 text-3xl text-gray-700 font-bold capitalize dark:text-blue-200"
    >
      技術スタック
    </h2>
    <div class="mt-2">
      <h2
        class="mb-2 text-xl text-gray-700 font-bold dark:text-blue-200 capitalize"
      >
        Frontend
      </h2>

      <ul class="flex flex-wrap gap-4 items-center">
        <!-- <li class="flex items-center">
          <Html class="h-10 w-10 rounded-sm drop-shadow-sm"></Html>
        </li>

        <li class="flex items-center">
          <Css class="h-10 w-10 rounded-sm drop-shadow-sm"></Css>
        </li> -->
        <li class="flex items-center">
          <Javascript class="h-10 w-10"></Javascript>
        </li>
        <li class="flex items-center">
          <Bootstrap class="h-10 w-10"></Bootstrap>
        </li>
      </ul>
    </div>
    <div class="mt-4">
      <h2
        class="mb-2 text-xl text-gray-700 font-bold dark:text-blue-200 capitalize"
      >
        Backend
      </h2>
      <ul class="mb-6 flex flex-wrap gap-4">
        <li class="flex items-center">
          <Python class="h-10 w-10"></Python>
        </li>
        <li class="flex items-center">
          <Django class="h-10 w-10"></Django>
        </li>
        <li class="flex items-center">
          <Aws class="h-10 w-10"></Aws>
        </li>
        <li class="flex items-center">
          <Oracle class="h-10 w-10"></Oracle>
        </li>
        <li class="flex items-center">
          <Datadog class="h-10 w-10"></Datadog>
        </li>
        <li class="flex items-center">
          <Node class="h-10 w-10"></Node>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Javascript from "../assets/devicon/javascript.svg?inline";
import Html from "../assets/devicon/html.svg?inline";
import Css from "../assets/devicon/css.svg?inline";
import Vuejs from "../assets/devicon/vuejs.svg?inline";
import TailwindCss from "../assets/devicon/tailwindcss.svg?inline";
import Nuxt from "../assets/devicon/nuxt.svg?inline";
import Bootstrap from "../assets/devicon/bootstrap.svg?inline";
import Laravel from "../assets/devicon/laravel.svg?inline";
import Node from "../assets/devicon/node.svg?inline";
import Python from "../assets/devicon/icons8-python.svg?inline";
import Django from "../assets/devicon/django-logo-negative.svg?inline";
import Aws from "../assets/devicon/icons8-aws.svg?inline";
import Oracle from "../assets/devicon/icons8-oracle.svg?inline";
import Datadog from "../assets/devicon/datadoghq-icon.svg?inline";

export default {
  components: {
    Javascript,
    Html,
    Css,
    Bootstrap,
    Vuejs,
    TailwindCss,
    Nuxt,
    Laravel,
    Node,
    Python,
    Django,
    Aws,
    Oracle,
    Datadog
  },
};
</script>
