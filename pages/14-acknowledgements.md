---
layout: default
color: amber-light
class: h-full w-full overflow-hidden relative
---

<div class="credits-scroller absolute left-0 w-full flex flex-col items-center">

<div class="grid grid-cols-3 w-3/4 gap-y-8 text-lg items-center pt-8">

<div class="col-span-3 text-center mb-6 text-4xl font-bold text-amber-600">
Thank you!
</div>

<div class="col-span-1 text-right mr-6 text-gray-500 dark:text-gray-400">
Authors
</div>
<div class="col-span-2 text-left leading-relaxed text-gray-800 dark:text-gray-100">
<strong>Angelo Schillaci</strong><br>
<strong>Daniele Tambone</strong>
</div>

<div class="col-span-1 text-right mr-6 text-gray-500 dark:text-gray-400 flex justify-end">
  <Rough 
  type="crossed-off" 
  color="#ef4444" 
  :strokeWidth="3" 
  :delay="4500" 
  :animationDuration="800" 
  :show="$nav.currentPage === $page"
>
  <span class="inline-block px-1">Funding</span>
</Rough>
</div>
<div class="col-span-2 text-left text-gray-800 dark:text-gray-100">
University of Catania
</div>

</div>

<div class="h-[45vh]"></div>

<div class="text-center text-7xl text-gray-800 dark:text-gray-100 font-bold">
Questions?
</div>

</div>

<style>
/* Rimuove i margini di default per permettere l'ingresso dal bordo inferiore */
.slidev-layout { padding: 0 !important; }

.credits-scroller {
/* Partenza: Bordo superiore del blocco ancorato al bordo inferiore invisibile dello schermo */
top: 100%;
/* Modificato: da 7s a 9s per uno scorrimento leggermente più lento e leggibile */
animation: movie-credits-stop 20s cubic-bezier(0.25, 1, 0.4, 1) forwards;
animation-delay: 0.5s;
}

@keyframes movie-credits-stop {
100% {
/* Arrivo: Il bordo superiore si posiziona al centro dello schermo (50%) */
top: 50%;
/* Tiriamo su il blocco per l'intera sua altezza (-100%) e lo spingiamo giù di 60px 
(che equivale a metà dell'altezza del testo "Questions?") per centrarlo al millimetro! */
transform: translateY(calc(-100% + 60px));
}
}
</style>