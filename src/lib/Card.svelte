<script>
import { crossfade } from "svelte/transition";

const shuffle = () => {
    for (let i = deck.length -1; i > 0; i--) {
    let j = Math.floor(Math.random() * i)
    let k = deck[i]
    deck[i] = deck[j]
    deck[j] = k
    }
}

</script>

<img src="{card.image}" alt="{card.name}">