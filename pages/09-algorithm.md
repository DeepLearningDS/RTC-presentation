---
layout: top-title
side: l
color: amber-light
align: l
title: Algorithm
---

:: title ::

# Algorithm

:: content ::

<div class="border-b-[1px] border-black mb-2"></div>
<div class="grid grid-cols-2 gap-x-6 font-serif text-[0.7em] [&_p]:inline [&_p]:m-0 overflow-hidden h-full">

<div>

<div class="transition-all duration-300 py-1 origin-top-left" :class="[$nav.clicks === 1 ? 'text-[#92400e] opacity-100 scale-110 font-bold' : ($nav.clicks === 0 || $nav.clicks >= 5 ? 'opacity-100' : 'opacity-25')]">

<div class="alg-line">
<div class="alg-num">1:</div>
<div class="alg-code">
<b>procedure </b>
<span class="small-caps">InitializeSharedState</span>
</div>
</div>

<div class="alg-line">

<div class="alg-num">2:</div>

<div class="alg-code indent-1 [&_p]:inline [&_p]:m-0">

$t = 0$; $\mathbf{A}_{\text{cur}} = \mathbf{A}_{\text{init}}$, $\mathbf{o}_{\text{cur}} = \text{null}$

</div>

</div>
</div>

<br>

<div class="transition-all duration-300 py-1 origin-top-left" :class="[$nav.clicks === 2 ? 'text-[#92400e] opacity-100 scale-110 font-bold' : ($nav.clicks === 0 || $nav.clicks >= 5 ? 'opacity-100' : 'opacity-25')]">

<div class="alg-line">
<div class="alg-num">3:</div>
<div class="alg-code [&_p]:inline [&_p]:m-0">
<b>function </b>
<span class="small-caps">GetAction</span>

$(\mathbf{o}_{\text{next}})$

  </div>
  </div>
  
<div class="alg-line">
<div class="alg-num">4:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">
<b>with </b>

$\mathcal{M}$ acquired 
<b>do</b>

</div>

</div>

<div class="alg-line">
<div class="alg-num">5:</div>
<div class="alg-code indent-3 [&_p]:inline [&_p]:m-0">

$t = t + 1$

</div>

</div>

<div class="alg-line">
<div class="alg-num">6:</div>
<div class="alg-code indent-3 [&_p]:inline [&_p]:m-0">

$\mathbf{o}_{\text{cur}} = \mathbf{o}_{\text{next}}$

</div>

</div>

<div class="alg-line">
<div class="alg-num">7:</div>
<div class="alg-code indent-3 [&_p]:inline [&_p]:m-0">

notify $\mathcal{C}$

</div>

</div>

<div class="alg-line">
<div class="alg-num">8:</div>
<div class="alg-code indent-3 [&_p]:inline [&_p]:m-0">
<b>return </b>

$\mathbf{A}_{\text{cur}}[t - 1]$

</div>

</div>
</div>

<br>

<div class="transition-all duration-300 py-1 origin-bottom-left relative" :class="[$nav.clicks === 4 ? 'text-[#92400e] opacity-100 scale-110 font-bold z-10' : ($nav.clicks === 0 || $nav.clicks >= 5 ? 'opacity-100 z-0' : 'opacity-25 z-0')]">

<div class="alg-line">
<div class="alg-num">9:</div>
<div class="alg-code">
<b>function </b>
<span class="small-caps">GuidedInference</span>

$(\pi, \mathbf{o}, \mathbf{A}_{\text{prev}}, d, s)$

</div>
</div>

<div class="alg-line">
<div class="alg-num">10:</div>
<div class="alg-code indent-1 [&_p]:inline [&_p]:m-0">
<b>for </b>

$\tau = 0$ to $1$ with step size $1/n$ <b>do</b>

</div>
</div>

<div class="alg-line">
<div class="alg-num">11:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

$f_{\widehat{\mathbf{A}}^1} = \mathbf{A}' \mapsto \mathbf{A}' + (1 - \tau)\mathbf{v}_\pi(\mathbf{A}', \mathbf{o}, \tau)$

</div>
</div>

<div class="alg-line">
<div class="alg-num">12:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

$\mathbf{e} = \left(\mathbf{A}_{\text{prev}} - f_{\widehat{\mathbf{A}}^1}(\mathbf{A}^\tau)\right)^\top \text{diag}(\mathbf{W})$ 

</div>
</div>

<div class="alg-line">
<div class="alg-num">13:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

$\mathbf{g} = \mathbf{e} \cdot \frac{\partial f_{\widehat{\mathbf{A}}^1}}{\partial \mathbf{A}'} \Big|_{\mathbf{A}'=\mathbf{A}^\tau}$

</div>
</div>

<div class="alg-line">
<div class="alg-num">14:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

$\mathbf{A}^{\tau + \frac{1}{n}} = \mathbf{A}^\tau + \frac{1}{n} \left( \mathbf{v}_\pi(\mathbf{A}^\tau, \mathbf{o}, \tau) + \min\left(\beta, \frac{1 - \tau}{\tau \cdot r_\tau^2}\right) \mathbf{g} \right)$

</div>
</div>

<div class="alg-line">
<div class="alg-num">15:</div>
<div class="alg-code indent-1 [&_p]:inline [&_p]:m-0">

<b>return</b> $\mathbf{A}^1$

</div>
</div>
</div>

<!-- Questo div chiude il div della prima colonna -->
</div> 

<div>

<div class="transition-all duration-300 py-1 origin-top-right" :class="[$nav.clicks === 3 ? 'text-[#92400e] opacity-100 scale-110 font-bold' : ($nav.clicks === 0 || $nav.clicks >= 5 ? 'opacity-100' : 'opacity-25')]">

<div class="alg-line">
<div class="alg-num">16:</div>
<div class="alg-code">
<b>procedure </b>
<span class="small-caps">InferenceLoop</span>
</div>

</div>
  
<div class="alg-line">
<div class="alg-num">17:</div>
<div class="alg-code indent-1 [&_p]:inline [&_p]:m-0">

acquire $\mathcal{M}$

</div>

</div>

<div class="alg-line">
<div class="alg-num">18:</div>
<div class="alg-code indent-1 [&_p]:inline [&_p]:m-0">

$Q = \text{new Queue}([d_{\text{init}}], \text{maxlen}=b)$

</div>

</div>
  
<div class="alg-line">
<div class="alg-num">19:</div>
<div class="alg-code indent-1 [&_p]:inline [&_p]:m-0">
<b>loop</b>
</div>
</div>
  
<div class="alg-line">
<div class="alg-num">20:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

wait on $\mathcal{C}$ until $t \ge s_{\min}$

</div>

</div>

<div class="alg-line">
<div class="alg-num">21:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

$s = t$

</div>

</div>
  
<div class="alg-line">
<div class="alg-num">22:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

$\mathbf{A}_{\text{prev}} = \mathbf{A}_{\text{cur}}[s, s + 1, \dots, H - 1]$

</div>
</div>

<div class="alg-line">
<div class="alg-num">23:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

$\mathbf{o} = \mathbf{o}_{\text{cur}}$

</div>
</div>

<div class="alg-line">
<div class="alg-num">24:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

$d = \max(Q)$

</div>
</div>

<div class="alg-line">
<div class="alg-num">25:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">
<b>with </b>

$\mathcal{M}$ released
<b>do</b>

</div>
</div>

<div class="alg-line">
<div class="alg-num">26:</div>

<div class="alg-code indent-3 [&_p]:inline [&_p]:m-0">

$\mathbf{A}_{\text{new}} =$ <span class="small-caps">GuidedInference</span>$(\pi, \mathbf{o}, \mathbf{A}_{\text{prev}}, d, s)$

</div>
</div>

<div class="alg-line">
<div class="alg-num">27:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

$\mathbf{A}_{\text{cur}} = \mathbf{A}_{\text{new}}$

</div>
</div>

<div class="alg-line">
<div class="alg-num">28:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

$t = t - s$

</div>
</div>

<div class="alg-line">
<div class="alg-num">29:</div>
<div class="alg-code indent-2 [&_p]:inline [&_p]:m-0">

enqueue $t$ onto $Q$

</div>
</div>
</div>

</div>

<!-- <br> -->
</div>
<div class="border-t-[1px] border-black mt-2"></div>

<v-clicks :at="1">
    <div v-for="i in 5" :key="i" class="hidden"></div>
</v-clicks>

<style>
.alg-line { display: flex; align-items: flex-start; line-height: 1.5; margin-bottom: 2px; }
.alg-num { width: 1.5rem; flex-shrink: 0; text-align: right; margin-right: 0.5rem; color: #6b7280; font-size: 0.85em; user-select: none; }
.alg-code { flex-grow: 1; }
.alg-comment { color: #6b7280; float: right; font-size: 0.9em; padding-left: 10px; }
.indent-1 { margin-left: 1rem; }
.indent-2 { margin-left: 2rem; }
.indent-3 { margin-left: 3rem; }
.small-caps { font-variant: small-caps; }
/* Stile per una scrollbar pulita (opzionale ma consigliato per le slide) */
.custom-scrollbar::-webkit-scrollbar { width: 6px; }
.custom-scrollbar::-webkit-scrollbar-track { background: transparent; }
.custom-scrollbar::-webkit-scrollbar-thumb { background-color: #cbd5e1; border-radius: 10px; }
</style>