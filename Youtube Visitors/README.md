<article class="markdown"><h1 id="mle---poisson-assignment">
  MLE - Poisson Assignment
  <a class="anchor" href="#mle---poisson-assignment">#</a>
</h1>
<p>Say you started a YouTube channel about a year ago. You’ve done quite well so far and have collected some data. You want to know the probability of at least x visitors to your channel given some time period. The obvious choice in distributions is the <a href="https://en.wikipedia.org/wiki/Poisson_distribution">Poisson distribution</a> which depends only on one parameter, λ, which is the average number of occurrences per interval. We want to estimate this parameter using Maximum Likelihood Estimation.</p>
<ol>
<li>(50 points) Simulate 100 visits to your youtube channel, assuming that they will a Poisson distribution with a mean of 10 visits per minute. Plot the arrival time vs visitor index.</li>
</ol>
<p>NOTE: To do this task make sure you read carefully the section Definitions and Probability Mass Function in <a href="https://en.wikipedia.org/wiki/Poisson_distribution">Poisson distribution</a> entry of wikipedia and <a href="https://towardsdatascience.com/the-poisson-process-everything-you-need-to-know-322aa0ab9e9a">this blog post</a>.</p>
<ol start="2">
<li>(50 points)  Assume that you are given the visitation data generated in Step 1, implement a Gradient Descent algorithm from scratch that will estimate the Poisson distribution according to the Maximum Likelihood criterion. Plot the estimated mean vs iterations to showcase convergence towards the true mean.</li>
</ol>
<p>NOTE: To do this step, read <a href="https://towardsdatascience.com/understanding-maximum-likelihood-estimation-fa495a03017a">this blog post</a> and note the negative  log likelihood function.</p>
<p>RUBRIC:</p>
<ol>
<li>If you provide just the plots/code, you will be granted 50% of the points. To win the remaining 50% you will need clear documentation (see below).</li>
<li>We need to see a clear explanation of all the stages of developing (1) and (2) above which means that you need to explain the code in a way that the writeup is understood by fellow students.</li>
<li>Type inline with your Colab notebook your tutorial explanations. Equations can be typed in markdown using Latex syntax notation.  If you prefer plain Python you can also include markdown as a separate file but you do need to ensure that all plots are inline to that markdown document and are parsed correctly by Github.</li>
<li>Submit by sharing the Colab or Github with the TA.</li>
</ol>
</article>