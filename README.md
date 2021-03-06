farmersmarketoak
================

Oak's learning on how to organize a farmer's market on the web...

So, I had already designed state machines with HTTP diagrams, so I took those:

[Market](http://i.imgur.com/hEnrSFw.png?1)

[User](http://i.imgur.com/lsLkRfW.png?1)

[Farmer](http://i.imgur.com/iwqdVZQ.png?1)

...and then have to combine the elements of usability of all three to create the html structure for it:

index.html
inventory.html
farmer_submit.html

And now...documentation:

index.html

I took some template html code from a random site I was playing with a couple months ago that wasn't very structured, but could #be used as a template

`

<!DOCTYPE html>
<html>
<head>
    <title>My first web page</title>
    <link rel="stylesheet" href="style.css">
    
</head>
<h1>My first web page</h1>

<h2>What this is</h2>
<p>A simple page put together using HTML. <em>I said a simple page put together using HTML.</em> A simple page put together using HTML. A simp`le page put together using HTML. A simple page put together using HTML. A simple page put together using HTML. A simple page put together using HTML. A simple page put together using HTML. A simple page put together using HTML.</p>

<h2>Why this is</h2>
<ul>
    <li>To learn HTML</li>
    <li>
        To show off
        <ol>
            <li>To my boss</li>
            <li>To my friends</li>
            <li>To my cat</li>
            <li>To the little talking duck in my brain</li>
        </ol>
    </li>
    <li>Because I have fallen in love with my computer and want to give her some HTML loving.</li>
</ul>

h1 {
    color: #ffc;
    background-color: #009;
}

`

I then tossed out what wasn't needed for the uses of this assignment, then started to look into structure needed to support the HTTP request diagrams I created. 

I took the code directly from the slides for the form and href, which I then repurposed around what I needed. 

After making the three sheets, then getting the templated query links connected, I made sure there was a "home" page on each of the pages to go back to index.html, that the home page had the necessary links to the order and inventory update pages, and it was pretty much together. I will come back to this and see if there's more functionality that it needs, but I think I got what was needed for the assignment...

Deliverable #1: For each method supported by each resource in your service, specify what kinds of representation (if any) it requires, and what kinds of representations, including status codes, it might return. Be sure to consider possible error conditions. Add this specification to your repository.


The index.html "home page" will yield a "OK 200" code, and have two hyperlinks within leading to farmer_submit.html and inventory.html. Those will be GET requests and will respond with a OK 200 code unless the links somewhow get broken, which they would then give a Not Found 404 code.

In the inventory.html page, the user comes to a page with the inventory of the farmers market for the week with unique IDs for items and the related info on the farm, the item, etc. There is an order form within which the user can order the products sending a POST request to the server to order the item, get back a "CREATED 201" status code and be prompted to pay. The "home" button will send a GET request back to the index.html page.

The farmer_submit.html page contains a form for the farmer to input the items that they wish to sell that week. They will send a POST request and recieve a CREATED 201 status code if all is working well, or an UNAUTHORIZED 401 status code if they aren't signed in. 
