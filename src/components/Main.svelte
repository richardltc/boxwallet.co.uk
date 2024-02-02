<script lang="ts">
    import Step from "./Step.svelte";
    import Progress from "./Progress.svelte";

    let steps = [
        {
            name: "ReddCoin",
            icon: "fa-solid fa-building",
            description:
                "",
        },
    ];

    let benefits = [
        {
            metric: "10x",
            name: "Runs on a Pi!",
            description:
                "You can run as many wallets as your Pi will allow, securely, on your own local network," +
                " and access from any browser on any device!",
        },
        {
            name: "Keep staking whilst your main computer is off!",
            description:
                "You can run BoxWallet on a Pi or another PC on your network, and leave it staking whilst your laptop is off.",
        },
        {
            name: "Mobile friendly!",
            description:
                "Want to check-out how many stakes you've earned from the comfort of your couch? Just point your " +
                "mobile browser to your BoxWallet server and easily control BoxWallet from there.",
        },
        {
            name: "Run more than one wallet, at the same time!",
            description:
                "BoxWallet allows you to run more than one wallet, and stake easily, at the same time.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
            id="introPage"
            class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
                class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! Welcome to the <span class="poppins text-green-400">BoxWallet</span> fundraising site.
                <br />
                <br />Let's get your project
                <span class="poppins text-green-400">added!</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                How? It's <span class="text-green-400 font-bold">easy!</span> simply send your coin of choice to the wallet address
                below, and the first coin to reach their goal, gets <span class="text-green-400">added!</span> Simples!
            </p>
        </div>
<!--        <Progress/>-->
    </section>
    <section>

    </section>
    <table class="table-auto">
        <thead>
        <tr>
            <th class="text-left text-green-400">Coin</th>
            <th class="text-left text-green-400">Fundraising Address</th>
            <th class="text-left text-green-400">Download Core Files</th>
            <th class="text-left text-green-400">Upgrade Core Files</th>
            <th class="text-left text-green-400">Sync Blockchain</th>
            <th class="text-left text-green-400">Staking</th>
            <th class="text-left text-green-400">Transactions</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td>RDD</td>
            <td class="font-mono">RrziAFXvr9Lv5eWyzANn1vS3bDT69jnteU</td>
            <td class="opacity-50">Complete</td>
            <td class="opacity-50">Complete</td>
            <td class="font-bold">In Progress...</td>
            <td>Waiting for funding</td>
            <td>Waiting for funding</td>
        </tr>
        <tr>
            <td>DIVI</td>
            <td class="font-mono">DDfZy57R9FVeN2WdgcsTik6WbFcmPe5GtZ</td>
            <td>Waiting for funding</td>
            <td>Waiting for funding</td>
            <td>Waiting for funding</td>
            <td>Waiting for funding</td>
            <td>Waiting for funding</td>
        </tr>
        <tr>
            <td>PIVX</td>
            <td class="font-mono">D61Q6tjWkGackqQkjtAN2yhDdoALHpB9Zu</td>
            <td>Waiting for funding</td>
            <td>Waiting for funding</td>
            <td>Waiting for funding</td>
            <td>Waiting for funding</td>
            <td>Waiting for funding</td>
        </tr>
        </tbody>
    </table>

    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Which <span class="poppins text-green-400">coins</span> have already been added?
            </h3>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    <strong class="text-green-400">ReddCoin</strong>
                     <strong
                        class="text-green-400"></p>
            </Step>
        </div>
    </section>
    <section
            id="about"
            class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
        <div
                class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-green-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-green-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                About <span class="poppins text-green-400">BoxWallet</span>...
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            Why choose BoxWallet . . ?
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p
                            class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>