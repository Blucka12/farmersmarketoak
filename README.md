farmersmarketoak
================

Oak's learning on how to organize a farmer's market on the web...

So, I had already designed state machines with HTTP diagrams, so I took those:

[Farmer](http://i.imgur.com/hEnrSFw.png?1)

[User](http://i.imgur.com/lsLkRfW.png?1)

[Market](http://i.imgur.com/iwqdVZQ.png?1)

...and then have to combine the elements of usability of all three to create the html structure for it:

index.html

<table>
<!doctype html>
<html>
<head>
<meta charset="UTF-8">

</head>

<body>
<header>
	<h1>Monkeynubbins Farmer's Market</h1>
		<p>Come one, Come all! Enjoy our tastiness!!! Please check out our inventory below and easy order directions on that page!</p>
			
	<nav>
		</ol>
    	<ol class="farmers">
			<li class="navigation">
				<a href="inventory.html" rel="inventory">Inventory</a> </li>
			<li class="navigation">
				<a href="farmer_submit.html" rel="farmer_submission">Farmers check in HERE!!!</a> </li>
			</li> 
		</ol>
    </nav>
</header>

<div id="mainContent">

<div id="rightColumn">Please feel free to contact us at: sexyfarmermonkeymarket@eatyourgreens.com for more information or to special order some items! Thanks!</div>

</div>

<footer>
Copyright 2014 BabyGotBlackEyedPeas Produce Consortium

</footer>
</body>
</html>
</table>
-------------------------------

inventory.html

<!doctype html>
<html>
<head>
<meta charset="UTF-8">
<title>Monkeynubbins Farmer's Market - What We Have</title>


</head>

<body>
<header>
<h1>Sexy Monkey Farmers Inventory</h1>
<p>Check out what's available this week with all the details!</p>

</header>

<div id="mainContent">
<article>
  <section>
  <h2>Inventory</h2>
  <p>This produce is so delicious, I would be surprised if you didn't have some form of accident as a result. Relax and enjoy the deliciousness...</p>
  
	<nav>
		<ol class="farmers"> 
			<li class="farmer">
				<span class="Item_ID">#12345</span>
				<span class="week_picked">06/01/2014</span>
				<span class="vegetable">Yellow Squash</span> 
				<span class="organic_no">Organic</span>
				<span class="price_per_unit">$10.00</span>
			</li>
			<li class="farmer">
				<span class="Item_ID">#12346</span>
				<span class="week_picked">06/01/2014</span>
				<span class="vegetable">Yellow Squash</span> 
				<span class="organic_no">Not Organic</span>
				<span class="price_per_unit">$8.00</span>
			</li>
			<li class="farmer">
				<span class="Item_ID">#12347</span>
				<span class="week_picked">06/01/2014</span>
				<span class="fruit">Apple</span>
				<span class="organic_no">Organic</span>
				<span class="price_per_unit">$7.00</span>
			</li>
			<li class="farmer">
				<span class="Item_ID">#12348</span>
				<span class="week_picked">06/01/2014</span>
				<span class="fruit">Apple</span> 
				<span class="organic_no">Not Organic</span>
				<span class="price_per_unit">$5.00</span>
			</li>
			<li class="farmer">
				<span class="Item_ID">#12349</span>
				<span class="week_picked">06/01/2014</span>
				<span class="fruit">tomato</span> 
				<span class="organic_no">Not Organic</span>
				<span class="price_per_unit">$9.00</span>
			</li>
	<h2>Order and Checkout</h2>
  <p>Go ahead and order as much of these goodies as we have!</p>
		<div class="customer_order">
			<form method="post" action="/checkout">
				<input type="text" name="vegetable" value=""/> 
				<input type="text" name="fruit" value=""/> 
				<input type="text" name="price" value=""/> 
				<input class="create" type="submit"/>
  			</form>
		</div>
    </nav>
	</section>
</article>

<div id="rightColumn">Please feel free to contact us at: sexyfarmermonkeymarket@eatyourgreens.com for more information or to special order some items! Thanks!</div>

</div>

<footer>
Copyright 2014 BabyGotBlackEyedPeas Produce Consortium

</footer>

</body>
</html>


---------------------------------

farmer_submit.html

<!doctype html>
<html>
<head>
<meta charset="UTF-8">
<title>Monkeynubbins Farmer's Market - What We Have</title>


</head>

<body>
<header>
<h1>Farmer's Hub</h1>
<p>Hey guys, we want to take good care of you, so take good care of us by entering all your goodies for this week!</p>

</header>

<div id="mainContent">
<article>
  <section>
  <h2>Inventory</h2>
  <p>Enter into the form what you have and price/unit along with your farmer ID, and we'll handle the rest. Thanks!</p>
  
	<nav>
		<div class="produce_submission">
<form method="post" action="/inventory">
<input type="text" name="" value="Vegetable"/> <input type="text" name="fruit" value=""/> <input type="text" name="price" value=""/> <input class="create" type="submit"/>
  </form>
</div>
		<li class="navigation">
				<a href="index.html" rel="homepage">Home</a>
    </nav>
	</section>
</article>

<div id="rightColumn">If you have questions about payment and follow-up procedures, contact us at: sexyfarmermonkeymarket@eatyourgreens.com for more information or to special order some items! Thanks!</div>

</div>

<footer>
Copyright 2014 BabyGotBlackEyedPeas Produce Consortium

</footer>

</body>
</html>
