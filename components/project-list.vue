<template>
    <p>Take a look at my Github projects</p>

    <section v-if="pending">Loading ...</section>
    <section v-else="error">something went wrong. Try again!</section>
    <section v-else>
        <ul class="grid grid-cols-1 gap-6 sm:grid-cols-2 md:grid-cols-2 mt-6">
            <li v-for="repo in data" :key="repo.id"
             class="border p-4 rounded shadow hover:shadow-lg transition duration-300 ease-in-out transform hover:-translate-y-1">
             <a :href="repo.html_url" target="_blank">
             <div class="flex items-center justify-between">
                <div class="font-bold">{{ repo.name }}</div>
             </div>
             <div>{{ repo.stargazers_count }} ★</div>
             <p class="text-sm">{{ repo.description }}</p>
             
             </a>
            </li>
        </ul>
    </section>
</template>



<script setup>
const { error, pending, data } = await useFetch('https://api.github.com/users/Bioprotron/repos')

/* const repos = computed(
    () => data.value.filter(repo => repo.description)
    .sort((a, b) => b.stargazers_count - a.stargazers_count)

)  */
</script>