---
marp: true
theme: poster
paginate: false
size: 33:46
---

<!-- Start header -->
<div class="header">

<!-- Image in the upper left -->
<div>

<img src="https://www.sydney.edu.au/etc.clientlibs/corporate-commons/clientlibs/foundation/resources/corporate-frontend/assets/img/USydLogo.svg" width="100%" alt="headerlogo">

</div>

<!-- Title and author information -->
<div>

# Making posters via marp a lesson in markdowning

## <u>Joshua A. Simmons</u><span class=super>1*</span>


##### 1 - Data Analytics for Resources and Environment (DARE), ARC Industrial Transformation Training Centre, University of Sydney <br>![icon](./img/mail.png) [_joshua.simmons@sydney.edu.au_](mailto:joshua.simmons@sydney.edu.au) ![icon](./img/github.png) [_@dare-centre_](https://github.com/dare-centre)

</div>

<!-- Image on the upper right -->
<div>

<img src="https://darecentre.org.au/wp-content/uploads/2020/05/Dare-logo2.png" width="100%" alt="headerlogo">

</div>

<!-- End header -->
</div>

<!-- Summary box title -->

<span class='h3-noline'> Summary </span>

<!-- Summary box using 5 columns-->
<div class='box'>
<div class="columns-box">

<!-- Box col1 -->
<div>

- This is what we were interested in.

</div>

<!-- Box col2 -->
<div>

- We did this awesome thing.

</div>

<!-- Box col3 -->
<div>

- Then we did this other awesome thing.

</div>

<!-- Box col4 -->
<div>

- Finally, we did this amazing thing.

</div>

<!-- Box col5 -->
<!-- <div>

- This is what changes for you.

</div> -->

<!-- End columns and box -->
</div>
</div>

<!-- Start main 2 column split for poster -->
<div class="columns-main">

<!-- Start main column 1 -->
<div>

### Motivation

- Connectomes are rich sources of inspiration for architectures in artificial intelligence.
- Comparing connectomes could help elucidate which structural features are necessary for yielding the capabilities animal intelligences.
- Bilateral symmetry for connectomes is one such comparison; has been investigated, but not clearly defined as a network hypothesis.

### What are we going to do

<div class=columns2>
<div>

![center w:5.5in](https://darecentre.org.au/wp-content/uploads/2020/05/Dare-logo2.png)

**Fig 1A:** 3D rendering of a larval _Drosophila_ brain connectome [1] comprised of ~3k neurons and ~544k synapses.

</div>
<div>

![center w:5.1in](https://darecentre.org.au/wp-content/uploads/2020/05/Dare-logo2.png)

**Fig 1B:** Directed, binary adjacency matrix sorted by brain hemisphere. We compare $\color{#66c2a5} L \rightarrow L$ vs. $\color{#fc8d62} R \rightarrow R$ subgraphs.

</div>
</div>

<!-- Big question for this work -->

## Are the <span style="color:var(--left)"> left </span> and <span style="color:var(--right)"> right </span> networks "different"?

<br>

This is what we need to do for this work

### Thing we did 1

<div class=columns2>
<div>

![](https://darecentre.org.au/wp-content/uploads/2020/05/Dare-logo2.png)

</div>
<div>

![](https://darecentre.org.au/wp-content/uploads/2020/05/Dare-logo2.png)

</div>
</div>

<div class=columns2>
<div>

**Fig 2A:** Testing symmetry under Erdos-Renyi (ER) model [2] compares global connection probability (density), here via Fisher's exact test.

</div>
<div>

**Fig 2B:** Test comparing densities rejected ($p{<}10^{-23}$), even the simplest model parameter differs between hemispheres.

</div>
</div>

<!-- End main column 1 -->
</div>

<!-- Start main column 2 -->
<div>

### Thing we did 2

<div class="columns2">
<div>

<!-- Example of a table, here within a column split -->

#### With Kenyon cells

| Model |                       $H_0$ (vs. $H_A \neq$)                       |    p-value    |
| :---: | :----------------------------------------------------------------: | :-----------: |
| **1** |  $\color{#66c2a5} p^{(L)} \color{black} = \color{#fc8d62}p^{(R)}$  | ${<}10^{-23}$ |
| **2** | $\color{#66c2a5} B^{(L)} \color{black} = \color{#fc8d62} B^{(R)}$  | ${<}10^{-7}$  |
| **3** | $\color{#66c2a5}B^{(L)} \color{black}  = c \color{#fc8d62}B^{(R)}$ | ${<}10^{-2}$  |

</div>
<div>

#### Without Kenyon cells

| Model |                       $H_0$ (vs. $H_A \neq$)                       |    p-value    |
| :---: | :----------------------------------------------------------------: | :-----------: |
| **1** |  $\color{#66c2a5} p^{(L)} \color{black} = \color{#fc8d62}p^{(R)}$  | ${<}10^{-26}$ |
| **2** | $\color{#66c2a5} B^{(L)} \color{black} = \color{#fc8d62} B^{(R)}$  | ${<}10^{-2}$  |
| **3** | $\color{#66c2a5}B^{(L)} \color{black}  = c \color{#fc8d62}B^{(R)}$ |    $0.51$     |

</div>
</div>

### Thing we did 3

<!-- ![](../../../results/figs/thresholding_tests/edge_weight_dist_input_proportion.png) -->

<div class="columns2">
<div>

![](./results/thresholding_tests/../../../../../results/figs/thresholding_tests/thresholding_methods.svg)

</div>
<div>

![](../../../results/figs/thresholding_tests/input_threshold_pvalues_legend.svg)

</div>
</div>

<div class="columns2">
<div>

**Fig 5A:** Removed edges w/ weight (synapse count or percentage of input to downstream neuron) below some threshold, tested symmetry for each pair of networks.

</div>
<div>

**Fig 5B:** Did not detect asymmetry in networks of only top ~$50\%$ of edges (by input percentage) under models studied here. Not true using synapse counts edge weights (not shown).

</div>
</div>

### Limitations and extensions

- Other models to consider (e.g. random dot product graph [3])
- Other sensible neuron groupings for group connection test
- Matching nodes across networks leads to new models, likely more power

<!-- Code/Refs/Thanks/Funding - small section -->

###

<div class="columns2">
<div>

#### Code ![icon](./img/github.png)

[github.com/dare-centre/llara-soil-moisture](https://github.com/dare-centre/llara-soil-moisture)

#### Acknowledgements

<footer>
Marta Zlatic's lab, Albert Cardona's lab and all tracers for the amazing dataset and many ideas. NeuroData lab for feedback. Many at Microsoft Research for w/ graspologic.
</footer>

</div>
<div>

#### References

<!-- Need these breaks <br> between refs otherwise formatting breaks for some reason -->
<footer>
[1] Winding, Pedigo et al. "The complete connectome of an insect brain," In preparation (2022)
<br>
[2] Chung et al. "Statistical connectomics," Ann. Rev. Statistics and its Application (2021) <br>
[3] Athreya et al. "Statistical inference on random dot product graphs: a survey," JMLR (2017)
</footer>

#### Funding

<footer>
We thank the Australian Government for supporting this research through the Australian Research Council’s Industrial Transformation Training Centre in Data Analytics for Resources and Environments (DARE) (project IC190100031).
</footer>

</div>
</div>

<!-- End main column 2 -->
</div>
<!-- End main columns -->
</div>
