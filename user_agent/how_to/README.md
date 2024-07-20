# USER AGENT 

## how i've found it:

in home page at the bottom click on © BornToSec a page will shown.
inspect and start expending all div's, a dive is commented once you read it you'll find text : ( You must come from : "https://www.nsa.gov/" ), continue reading to find the next they recomend a certain browser : ( Let's use this browser : "ft_bornToSec". It will help you a lot. )

* 1_ reload the page and intercept the request with burpsuite
* 2_ change User-Agent browser to ft_bornToSec
* 3_ change Referer to https://www.nsa.gov/
* 4_ enjoy the flag (^_^)

## how to resolev patch

1_ secret information must be never kept in frontEnd
2_ you can detect that the user is browsing on a mobile device using CSS media queries which you could use to show/hide a warning saying that the page is only available to mobile/desktop devices.