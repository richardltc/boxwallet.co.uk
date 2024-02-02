<script lang="ts">
    import { createProgress, melt } from '@melt-ui/svelte';
    import { writable } from 'svelte/store';

    export const value = writable(1);
    export let coins_goal = 75;
    export let coin_address = 'XXXX'
    export let coin_name = 'Unknown';

    const {
        elements: { root },
        options: { max },
    } = createProgress({
        value,
        max: coins_goal,
    });

    const sleep = (ms: number) =>
        new Promise((resolve) => setTimeout(resolve, ms));
    sleep(1000).then(() => {
        value.set(75);
    });
</script>

<div class="flex flex-wrap">
    <div class="w-[50px]">{coin_name}</div>
    <div class="w-[50px]">{coin_address}</div>
    <div use:melt={$root} class="relative h-6 w-[1000px] overflow-hidden rounded-[99999px] bg-black/40">
        <div
                class="h-full w-full bg-[white] transition-transform duration-[660ms]
        ease-[cubic-bezier(0.65,0,0.35,1)]"
                style={`transform: translateX(-${
      100 - (100 * ($value ?? 0)) / ($max ?? 1)
    }%)`}
        />
    </div>

</div>
