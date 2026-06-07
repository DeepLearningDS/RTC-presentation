---
layout: side-title
side: l
color: amber-light
titlewidth: is-4
align: rm-lm
title: Notation
---

:: title ::

# Notation <!-- # <mdi-arrow-right /> -->

:: content ::

<!-- Click 1 -->
<div v-click class="transition-opacity duration-500">

$\textcolor{#92400e}{t}$ indicates a controller timestep

</div>

<!-- Click 2 -->
<div v-click class="transition-opacity duration-500">

$\textcolor{#92400e}{o_t}$ is an observation

</div>

<!-- Click 3 -->
<div v-click class="transition-opacity duration-500">

$\textcolor{#92400e}{\pi(A_t,o_t)}$ is an action chunking policy

</div>

<div class="relative h-28 text-xl mt-4">
  <!-- Riga A: Appare al click 4 in alto, scende al click 6 -->
  <div class="absolute transition-all duration-500 w-full flex items-baseline gap-2 [&_p]:m-0" 
       :class="[$nav.clicks > 3 ? 'opacity-100' : 'opacity-0', $nav.clicks > 5 ? 'top-14' : 'top-0']">

  $\textcolor{#92400e}{A_t = }$

  <!-- Blocco formula unito: spezziamo la parentesi -->
  <div class="flex items-baseline">
  <Rough type="bracket" brackets="bottom" color="#92400e" :show="$nav.clicks > 5" class="relative">
  
  $\textcolor{#92400e}{[a_t, a_{t+1}, \cdots}$
  
  <div class="absolute -bottom-8 left-1/2 transform -translate-x-1/2 text-[0.8em] font-serif text-[#92400e] transition-opacity duration-700" 
         :class="$nav.clicks > 5 ? 'opacity-100' : 'opacity-0'">s</div>         
</Rough>

<!-- La parte finale della formula rimane fuori da Rough -->

$\textcolor{#92400e}{, a_{t+H-1}]}$

  </div>

  <!-- Testo allineato (puoi modificare 2px con 1px, 3px o -1px per aggiustarlo al millimetro al tuo occhio) -->
  <div class="translate-y-[2px]">is a chunk of future actions</div>

  </div>

  <!-- Riga B: Appare al click 5 in basso, sale al click 6 -->
  <div class="absolute transition-all duration-500 w-full" 
       :class="[$nav.clicks > 4 ? 'opacity-100' : 'opacity-0', $nav.clicks > 5 ? 'top-0' : 'top-14']">

  $\textcolor{#92400e}{H}$ is the *prediction horizon*

  </div>
</div>

<!-- Questi div invisibili assorbono i click della tastiera per far avanzare le variabili di $nav.clicks -->
<div v-click class="hidden"></div> <!-- Innesca il click 4 -->
<div v-click class="hidden"></div> <!-- Innesca il click 5 -->
<div v-click class="hidden"></div> <!-- Innesca il click 6 -->

<!-- La riga di 's' è ora slegata da v-click e ascolta il sesto click ($nav.clicks > 5) -->
<div class="transition-opacity duration-700 mt-4" :class="$nav.clicks > 5 ? 'opacity-100' : 'opacity-0'">

$\textcolor{#92400e}{s}$ is the *execution horizon* (e.g., $s \approx \textcolor{#92400e}{H}/2$)

</div>

<div v-click class="transition-opacity duration-500 flex items-center justify-center w-full mt-10 text-[#92400e] text-lg">
  <span class="font-semibold mr-3">Reactivity</span>
  <div class="relative flex items-center flex-grow">
    <mdi-arrow-left class="text-2xl" />
    <div class="h-[2px] bg-[#92400e] flex-grow -mx-1"></div>
    <mdi-arrow-right class="text-2xl" />
    <div class="absolute -bottom-6 left-1/2 transform -translate-x-1/2 text-[0.8em] font-serif text-[#92400e]">
      s
    </div>
  </div>
  <span class="font-semibold ml-3">Consistency</span>
</div>