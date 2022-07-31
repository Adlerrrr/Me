<template>
    <div class="container">
        <div class="info">
            <img src="../assets/img/eu.jpg" alt="Wilson Adler Junior">
        </div>
        <div class="info">
            <p class="name">Wilson Adler Junior</p>
            <p class="role">Front-end Developer</p>
        </div>
        <div class="info">
            <ul>
                <li><span class="material-icons">mail_outline</span>{{ dados.email }}</li>
                <li><span class="material-icons">phone</span> {{ dados.telefone }}</li>
                <li><a href="https://github.com/Adlerrrr"><img src="../assets/img/github.png" class="gitImg">{{
                        dados.github
                }}</a></li>
                <li><a href="https://www.linkedin.com/in/wilson-adler-junior"><img src="../assets/img/linkedin.png"
                            class="gitImg">{{ dados.linkedin }}</a></li>
            </ul>

        </div>
        <div class="info education">
            <p class="name">Education</p>
            <p class="course">{{ dados.education }}</p>
        </div>
        <div class="info name skills">
            <p>Skills</p>
            <ul>
                <li v-for="items in lang">
                    {{ items.langu }}
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Title',
    data() {
        return {
            dados: {
                telefone: '+55 11 98873-5656',
                email: 'wilson.adlerr@gmail.com',
                github: 'github.com/Adlerrrr',
                linkedin: 'linkedin.com/wilson-adler-junior',
                education: 'BS Business administration'
            },
            lang: [
                { langu: 'JavaScript' },
                { langu: 'Vue' },
                { langu: 'Html' },
                { langu: 'Css' },
                { langu: 'Python' },
                { langu: 'Ruby' },
                { langu: 'React' },
                { langu: 'Angular' },
                { langu: 'Git' }
                
            ]

        }

    }
}
</script>

<style scoped>

img {
    max-width: 156px;
    border-radius: 50%;
    padding: 32px;
}

.info {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    width: 196px;
}

p {
    padding: 2%;
}

.name {
    font-size: 22px;
    font-weight: 900;
}

ul {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 16px;
    font-size: 12px;
    font-weight: 100;
    width: 100%;
}

li {
    padding: 5%;
    display: flex;
    align-items: center;

}

.gitImg {
    width: 24px;
    height: 24px;
    padding: 0;
    border-radius: 0%;
    padding: 3%;
}

a {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: inherit;
}

.education {
    margin-top: 16px;

}

.course{
    text-align: center;
    font-size: 12px;
}

.skills {
    margin-top: 16px;
}
</style>
