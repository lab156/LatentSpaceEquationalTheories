---
layout: default
title: The Latent Space of Equational Theories - Research Summary
---

<header>
    <h1>The Latent Space of Equational Theories</h1>
    <p class="authors">Luis Berlioz & Paul-André Melliès</p>
    <p class="metadata">arXiv:2601.20759v1 [cs.LO]</p>
</header>

<div class="abstract">
    <h2>Abstract</h2>
    <p>Building on the collaborative <strong>Equational Theories project</strong> initiated by Terence Tao fifteen months ago, and combining it with ideas from machine learning and finite model theory, we construct a <strong>latent space of equational theories</strong>. In this space, each equational theory is located at a specific coordinate determined by its logical properties. This experiment enables us to observe for the first time how reasoning flows and produces surprisingly oriented and well-structured chains of logical implications within the landscape of universal algebra.</p>
</div>

<section>
    <h2>Main Points</h2>
    <p>This study introduces an experimental approach to logic by treating mathematical concepts as vertices in a geometric latent space.</p>
    
    <div class="highlight-box">
        <strong>The Main Objective:</strong> To map the relationships between 4,694 distinct equational theories and visualize the underlying structure of mathematical reasoning.
    </div>

    <ul>
        <li><strong>Methodology:</strong> The researchers utilized <strong>Principal Component Analysis (PCA)</strong> to reduce the dimensionality of the feature space into a 3D representation.</li>
        <li><strong>Theoretical Foundation:</strong> The work uses the concept of <em>Stone pairing</em> originating from finite model theory to bridge the gap between categorical logic and statistical learning.</li>
        <li><strong>Discovery:</strong> The experiment reveals a rich, well-organized landscape where logical implications form visible "flows," illustrating the benefits of an experimental approach to pure logic.</li>
    </ul>
</section>

<section>
    <h2>Implementation & Visualization</h2>
    <p>To derive the latent space, the following steps were taken:</p>
    <ol>
        <li>Analysis of <code>n = 20,000</code> magmas of size 8 to extract feature variability.</li>
        <li>Computation of the center of gravity and covariance matrix for the 4,694 theories.</li>
        <li>Application of PCA to keep the first three principal components (X, Y, Z), which capture the majority of the data's variability.</li>
    </ol>
</section>


<section>
<h2>Visualizing the PCA of Individual Equations</h2>
<p>
The signature of an equation is the ordered pair with the number of operations on the left and right hand side of the equation respectively. In the figure below, the points are colored according to signature with the following values.
   </p>

<div class="table-container">
  <table>
    <tr>
      <td><span style="color: red;">(0,4)</span></td>
      <td><span style="color: blue;">(1,3)</span></td>
      <td><span style="color: green;">(2,2)</span></td>
    </tr>
    <tr>
      <td><span style="color: purple;">(0,3)</span></td>
      <td><span style="color: cyan;">(1,2)</span></td>
      <td><span style="color: yellow;">(1,1) </span></td>
    </tr>
    <tr>
      <td><span style="color: pink;">(0,2) </span></td>
      <td><span style="color: pink;">(0,1) </span></td>
      <td><span style="color: pink;">(0,0) </span></td>
    </tr>
  </table>
</div>

<div style="width: 100%; height: 600px; overflow: hidden; border: 1px solid #eaecef; border-radius: 6px;">
        <iframe 
            src="{{ site.baseurl }}Images/figure_6.html" 
            width="100%" 
            height="600px" 
            frameborder="0" 
            scrolling="yes">
        </iframe>
    </div>
    <p>
    The code is available in <a href="http:/Notebooks/Sampling%204x4%20and%208x8%20magmas.ipynb">Notebooks/Sampling 4x4 and 8x8 magmas.ipynb</a>
    </p>

    <h3>Changing the Magma Sizes</h3>
    Finite magmas are represented as a bidimensional array of size $n\times n$ of numbers between $1$ and $n$. The following video shows how the positions of the equations' PCA changes when the size of their corresponding magmas is varied:
    <video controls loop style="max-width: 100%; width: 100%; height: auto; border-radius: 6px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
        <source src="{{ site.baseurl }}Images/yzpca.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</section>

## Visualizing the Implications
True implications are visualized as arrows going from the point representing the hypothesis to the tail, i.e., the conclusion.

<div style="width: 100%; height: 600px; overflow: hidden; border: 1px solid #eaecef; border-radius: 6px;">
        <iframe 
            src="{{ site.baseurl }}Images/figure_13.html" 
            width="100%" 
            height="600px" 
            frameborder="0" 
            scrolling="yes">
        </iframe>
    </div>
    
<footer>
    <p>Source Content: <a href="https://arxiv.org/abs/2601.20759">arXiv:2601.20759v1</a> &bull; Formatted for Project Documentation (2026)</p>
</footer>
