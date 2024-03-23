<script setup lang="ts">
const blogPostPreview = {
    image: new URL('../assets/images/illustration-article.svg', import.meta.url).href,
    category: 'learning',
    publishDate: '21 Dec 2023',
    title: 'HTML & CSS foundations',
    description: 'These languages are the backbone of every website, defining structure, content, and presentation.',
    author: {
        name: 'Greg Hooper',
        image: new URL('../assets/images/image-avatar.webp', import.meta.url).href
    }
}
</script>

<template>
    <main class="container">
        <div class="card">
            <img class="image" :src="blogPostPreview.image" />

            <div class="content">
                <div class="category">
                    {{ blogPostPreview.category }}
                </div>

                <span class="publish-date">
                    Published {{ blogPostPreview.publishDate }}
                </span>

                <h2 class="title">
                    {{ blogPostPreview.title }}
                </h2>

                <p class="description">
                    {{ blogPostPreview.description }}
                </p>
            </div>

            <div class="author">
                <img class="author-image" :src="blogPostPreview.author.image" />

                <span class="author-name">{{ blogPostPreview.author.name }}</span>
            </div>
        </div>
    </main>
</template>

<style scoped>
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    min-height: 100vh;
    padding: 9.75rem 1.5rem;
    background-color: var(--yellow);
}

.card {
    width: 100%;
    max-width: 20.5rem;
    padding: 1.5rem;
    border-radius: 1.25rem;
    background-color: #fff;
    border: var(--black) solid;
    filter: drop-shadow(0.5rem 0.5rem #000);

    @media screen and (min-width: 640px) {
        max-width: 24rem;
    }
}

.image {
    display: block;
    width: 100%;
    border-radius: 0.625rem;
}

.content {
    margin: 1.5rem 0;
}

.category {
    margin-bottom: 0.75rem;
    width: fit-content;
    padding: 0.25rem 0.75rem;
    font-size: 0.75rem;
    font-weight: 800;
    background-color: var(--yellow);
    border-radius: 0.25rem;
    text-transform: capitalize;

    @media screen and (min-width: 640px) {
        font-size: 0.875rem;
    }
}

.publish-date {
    font-size: 0.75rem;
    font-weight: 500;

    @media screen and (min-width: 640px) {
        font-size: 0.875rem;
    }
}

.title {
    margin: 0.75rem 0;
    font-size: 1.25rem;
    font-weight: 800;

    @media screen and (min-width: 640px) {
        font-size: 1.5rem;
    }
}

.title:hover {
    color: var(--yellow);
    cursor: pointer;
}

.description {
    font-size: 0.875rem;
    font-weight: 500;
    color: var(--grey);

    @media screen and (min-width: 640px) {
        font-size: 1rem;
    }
}

.author {
    display: flex;
    align-items: center;
}

.author-image {
    margin-right: 0.75rem;
    width: 2rem;
    height: 2rem;
}

.author name {
    font-size: 0.875rem;
    font-weight: 800;
}
</style>