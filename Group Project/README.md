<article class="markdown"><h1 id="btc-deep-forecasting">
  BTC Deep Forecasting
  <a class="anchor" href="#btc-deep-forecasting">#</a>
</h1>
<p><img src="images/btc.gif" alt=""></p>
<p>In this project we will be forecasting the price of an asset or commodity. To exponentially increase your cool factor within your social network, you are tasked to predict the daily (trading days only) closing price in USD of Bitcoin (BTC).</p>
<hr>
<p>DISCLAIMER</p>
<p>THIS IS A CLASS PROJECT POSTED FOR EDUCATIONAL PURPOSES ONLY. IF YOU FOLLOW THE METHODS AND PREDICTIONS POSTED BY STUDENTS, YOU ARE ALMOST CERTAINLY GUARANTEED TO LOOSE ALL YOUR CRYPTO OR REAL MONEY. THE REASON IS SIMPLE: ALTHOUGH WE DO NOT CONSTRAINT THE PREDICTOR VARIABLES OR THE APPROACHES, MOST OF THE STUDENTS WILL IMPLEMENT A FORECASTING METHOD BASED ON HISTORICAL BTC DATA. SINCE <strong>ALL</strong> FUTURE PRICES MOVE AS A RESULT OF THOUSANDS OF OTHER FACTORS (DATA) OTHER THAN HISTORICAL PRICES, YOU WILL SUFFER THE INEVITABLE SHOULD YOU BE FOOL ENOUGH TO BET ON SUCH PREDICTIONS. THE AUTHOR OF THIS PROJECT DESCRIPTION BEARS NO RESPONSIBILITY FOR YOUR IRRESPONSIBLE TRADING ACTIONS.</p>
<hr>
<h2 id="environment-set-up-0-points">
  Environment set up (0 points)
  <a class="anchor" href="#environment-set-up-0-points">#</a>
</h2>
<p>You will use google Colab for authoring your forecaster. You are also welcomed to set up an AWS account and use the <a href="https://docs.aws.amazon.com/forecast/latest/dg/what-is-forecast.html">AWS Forecast</a> service. No matter what you do however we can provide limited support for IT issues in your environment.</p>
<h2 id="data-10-points">
  Data (10 points)
  <a class="anchor" href="#data-10-points">#</a>
</h2>
<p>In this project you don’t need to think about Kafka and other pub/sub or message broker technologies that ingest data in production systems. You may retrieve and store all historical data you want to use (there is no time limit on the past) but you will implement a system that can update its models as “new” data are coming in.</p>
<p>So lets assume you define as a <em>window</em> data between <code>collection_start_date</code> and <code>collection_end_date</code>. You are free to collect as many windows of data as you wish and you are also free to determine the best window size.  The only constraint is that predictions you will report results on must be all trading days between Nov 1st 2021 and Dec 1st 2021 without repetition (aka. without predicting twice the same date).</p>
<!-- You will be predicting the BTC-USD price for **each of the last T=7 calendar days** of your window.  

![](images/forecasting.drawio.png) -->
<h2 id="tweet-sentiment-analysis-30-points">
  Tweet Sentiment Analysis (30 points)
  <a class="anchor" href="#tweet-sentiment-analysis-30-points">#</a>
</h2>
<p>Use the Twitter API and Python libraries that can access it to bring tweets you consider as relevant to the price prediction.</p>
<ol>
<li>You need to implement a tweet feed filter that will an encoder that will embed each tweet in a vector space and allow you to determine its sentiment (15 points)</li>
<li>You are also responsible for figuring out how to transform (eg average) the sentiments themselves so that they can be used by the price predictor (15 points)</li>
</ol>
<h2 id="price-predictor-development-50-points">
  Price Predictor Development (50 points)
  <a class="anchor" href="#price-predictor-development-50-points">#</a>
</h2>
<p>Follow <a href="https://www.analyticsvidhya.com/blog/2021/06/download-financial-dataset-using-yahoo-finance-in-python-a-complete-guide/">these</a> instructions to bring the BTC-USD price data required in this project.</p>
<h3 id="deepar-15-points">
  DeepAR (15 points)
  <a class="anchor" href="#deepar-15-points">#</a>
</h3>
<p>In <a href="https://arxiv.org/pdf/1704.04110.pdf">this paper</a> a methodology for producing accurate probabilistic forecasts, based on
training an auto-regressive recurrent network model is shown. RNNs will be covered in our lectures so there is no need to panic.</p>
<p>You will implement <a href="https://github.com/arrigonialberto86/deepar">in TF</a> or PyTorch the method and present your predictions.</p>
<h3 id="facebook-prophet-15-points">
  Facebook Prophet (15 points)
  <a class="anchor" href="#facebook-prophet-15-points">#</a>
</h3>
<p>You need to understand the principles behind the <a href="https://facebook.github.io/prophet/">Prophet prediction method</a> and implement it for the problem at hand.</p>
<h3 id="predictor-documentation-20-points">
  Predictor Documentation (20 points)
  <a class="anchor" href="#predictor-documentation-20-points">#</a>
</h3>
<p>You will write a 2-page single spaced summary (excludes figures) in markdown on how <em>each</em> predictor works (4 pages total min). You need to refer to corresponding code sections as you describe the functions.</p>
<h2 id="results-10-points">
  Results (10 points)
  <a class="anchor" href="#results-10-points">#</a>
</h2>
<ol>
<li>Post a table with your prediction vs actual price as well as include a plot of the two time series over time.</li>
<li>Provide any intuition around the forecasting method you adopted.</li>
</ol>
<p>Our advice is to create a skeleton of the project first with all parts involved without spending a lot of time on algorithm finetuning. Finetune after you have your draft predictions first.</p>
</article>