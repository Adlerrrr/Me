<template>
    <div class="container">
        <div>
            <h1 class="name">Carreer</h1>
            <p class="txtP">{{ carrerEn }}</p>
        </div>
        <div>
            <WorkXp />
        </div>
        <div>
            <h1 class="name">Languages</h1>
            <ul>
                <li class="languages" v-for="items in lang">
                    {{ items.lang }}({{ items.level }})
                </li>
            </ul>
        </div>
        <div class="others">
            <h1 class="name">Others Skills</h1>
            <ul>
                <li class="languages" v-for="items in others">
                    {{ items.others }}
                </li>
            </ul>
        </div>
    </div>
</template>


<script>
import WorkXp from './WorkXp.vue'
import Title from './Title.vue'
export default {
    name: "Carrer",
    components: WorkXp,
    data() {
        return {
            carrerEn: "I started coding when I finished high school with my friends in 2012. I went to university and studied business administration. I built my career outside the technological sphere, I worked at the largest bank in Brazil. I am currently a senior equity researcher and use technology as a tool to help me in my current role. I have a solid background in mathematics, statistics and logic. Focused on tasks, innovative and looking for new challenges. I am excited to get back to working directly with technology.",
            lang: [
                { lang: 'Portuguese ', level: ' Native ' },
                { lang: 'English ', level: ' Fluent ' },
                { lang: 'Spanish ', level: ' Intermediate ' },
            ],
            others: [
                { others: 'Certified Financial Analyst' },
                { others: 'Bloomberg - Bquant' },
                { others: 'Advanced Excel' },
                { others: 'VBA' }
            ]
        };
    },
    components: { Title, WorkXp }
}
</script>

<style scoped>
div {
    width: 750px;
}

.container {
    padding: 2%;
}

.container div{
    margin-top: 32px;
}

.name {
    font-size: 22px;
    font-weight: 900;
}

p {
    padding: 2%;
}

ul {
    display: flex;
    margin-top: 16px;
    justify-content: space-between;
}

.languages {
    list-style-type: disc;
    padding: 1%;

}
.others {
    margin-top: 32px;
}

.txtP{

line-height: 150%;
}
</style>