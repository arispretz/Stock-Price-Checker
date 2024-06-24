# Stock-Price-Checker

This is one of my projects in the way to achieve "Information Security" certification at freeCodeCamp.org. It was designed using Nodejs, Javascript, html, css, MongoDB and Helmetjs.
Since all reliable stock price APIs require an API key, we've built a workaround. Use https://stock-price-checker-proxy.freecodecamp.rocks/ to get up-to-date stock price information without needing to sign up for your own key.
SET NODE_ENV to test without quotes and set DB to your MongoDB connection string
Complete the project in routes/api.js or by creating a handler/controller
You will add any security features to server.js
You will create all of the functional tests in tests/2_functional-tests.js
Note Privacy Considerations: Due to the requirement that only 1 like per IP should be accepted, you will have to save IP addresses. It is important to remain compliant with data privacy laws such as the General Data Protection Regulation. One option is to get permission to save the user's data, but it is much simpler to anonymize it. For this challenge, remember to anonymize IP addresses before saving them to the database. If you need ideas on how to do this, you may choose to hash the data, truncate it, or set part of the IP address to 0.

Write the following tests in tests/2_functional-tests.js:

Viewing one stock: GET request to /api/stock-prices/
Viewing one stock and liking it: GET request to /api/stock-prices/
Viewing the same stock and liking it again: GET request to /api/stock-prices/
Viewing two stocks: GET request to /api/stock-prices/
Viewing two stocks and liking them: GET request to /api/stock-prices/

You should set the content security policies to only allow loading of scripts and CSS from your server.
You can send a GET request to /api/stock-prices, passing a NASDAQ stock symbol to a stock query parameter. The returned object will contain a property named stockData.
The stockData property includes the stock symbol as a string, the price as a number, and likes as a number.
You can also pass along a like field as true (boolean) to have your like added to the stock(s). Only 1 like per IP should be accepted.
If you pass along 2 stocks, the returned value will be an array with information about both stocks. Instead of likes, it will display rel_likes (the difference between the likes on both stocks) for both stockData objects.
