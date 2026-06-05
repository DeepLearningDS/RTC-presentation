---
layout: side-title
side: l
color: amber-light
titlewidth: is-4
align: rm-lm
title: Flow matching
---

<script setup>
import { ref } from 'vue'
const activeTab = ref('definition')
</script>

:: title ::

<div class="animate-fade-in animate-duration-500">

# Flow matching

</div>

:: content ::

<div class="animate-fade-in animate-duration-500 relative h-full">

  <div class="flex gap-4 mb-6">
    <button @click="activeTab = 'definition'" 
      class="px-4 py-1 rounded shadow-sm transition-all font-semibold"
      :class="activeTab === 'definition' ? 'bg-[#92400e] text-white' : 'bg-gray-200 text-gray-500 hover:bg-gray-300'">
      Definition
    </button>
    <button @click="activeTab = 'animation'" 
      class="px-4 py-1 rounded shadow-sm transition-all font-semibold"
      :class="activeTab === 'animation' ? 'bg-[#92400e] text-white' : 'bg-gray-200 text-gray-500 hover:bg-gray-300'">
      Animation
    </button>
  </div>

  <div class="relative min-h-[350px]">
    <div v-if="activeTab === 'definition'" class="animate-fade-in animate-duration-300">
Let

* $x_1 \sim q(x_1)$
* $p_t$ be a probability path such that $p_0 = p$ is a simple distribution
* $p_1$ be approximately equal in distribution to $q$
    
Given a target probability density path $p_t(x)$ and a corresponding vector field $u_t(x)$, we define the **Flow Matching (FM)** objective as:
    
$$
\textcolor{#92400e}{\mathcal{L}_{FM}(\theta) = \mathbb{E}_{t,p_t(x)}||v_t(x)-u_t(x)||^2}
$$

</div>
<div v-if="activeTab === 'animation'" class="animate-fade-in animate-duration-300 mt-4">
<video :src="'/animation/flow-matching.mov'" autoplay loop muted playsinline class="w-full rounded-lg shadow-md"></video>
</div>

</div>

</div>

<div class="absolute bottom-4 text-sm font-extralight opacity-70">Yaron Lipman, Ricky TQ Chen, Heli Ben-Hamu, Maximilian Nickel, and Matt Le. Flow matching for generative modeling. arXiv preprint arXiv:2210.02747, 2022.</div>
