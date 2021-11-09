# seven-segment-display

A seven segment display that operates through a 7-bit binary code powered by [Svelte](https://svelte.dev).

## How numbers as displayed

The user input is passed down as a prop to the `Display` component and its value is used to index through the binary list. The binary list is stored in `bin.ts` as a array object string. The string is split by its indivisual character (byte) and each are fed in conditionally rendered svelte components. (you can also view the outputted binary by if you go to the console in the live version [here](http://seven-segment-display.vercel.app/))

By containg this whole process in a single `Display` component, it makes it possible to render multiple numbers (number being split into an array like the binary string) and show the nessasary outputs when needed by using Sveltes `{#each}` block.
