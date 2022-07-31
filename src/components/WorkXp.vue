<template>
    <h1 class="name">Work experience</h1>
    <div>
        <p class="name">Plural Investimentos</p>
        <p class="period">07/2019 - Current</p>
        <ul>
            <li v-for="items in exp">
                {{ items.PluralInv }}
            </li>
        </ul>

    </div>
    <div>
        <p class="name">Itaú Personnalité</p>
        <p class="period">07/2015 - 07/2019</p>
        <ul>
            <li v-for="items in expB">
                {{ items.PluralInv }}
            </li>
        </ul>

    </div>

</template>

<script>
export default {
    name: 'WorkXp',
    data() {
        return {
            exp: [
                { PluralInv: 'Evaluate risk parameters while analyzing proposed investment prospects on a daily basis.' },
                { PluralInv: 'Analyze the impact mergers, acquisitions, and other business practices will have on the market and economy.' },
                { PluralInv: 'Compile analysis findings into a compact report that is useful, accessible, and as in-depth as possible.' },
                { PluralInv: 'Present created report at board meetings clearly and concisely to aid in market decision making.' },
                { PluralInv: 'Gather data to create tools that aid analysis through alternative and traditional sources. Using Python, JavaScript and VBA.' },

            ],
            expB: [
                { PluralInv: 'Conduct comprehensive review of client portfolios, including meeting with clients, lawyers and advisors to assess strategies based on objectives and risk profile, identify opportunities, and prepare customized asset allocation suggestions.' },
                { PluralInv: 'Exceptional understanding of wide range of investment vehicles, including equities, structured products, foreign exchanges, and derivatives' },
                { PluralInv: 'Successfully explain and promote complex financial products to customers.' },

            ]
        }
    }

}
</script>

<style scoped>
li {
    list-style-type: disc;
    color: white;
}

.name {
    font-size: 22px;
    font-weight: 900;
}

div {
    padding: 5%;
}

p {
    margin-left: 0;

}

ul {
    margin-top: 10px;
}

li {
    padding: 0.5%;
    margin-left: 16px;
}

.period {
    font-size: small;
    font-style: italic;
}
</style>