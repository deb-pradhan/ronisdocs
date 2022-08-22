# OEMS
For OEMS we Initially started by implementing and mounting Frosty-Bot. Before testing it, we tried IP siphoning to check if there is any third party in between Frosty-Bot and exchange. So for that we tested it out by placing some order on FTX. It took around 8-10 seconds for executing transaction. On the IP Siphoning part, the Frosty-Bot is using CCXT and now we looked into CCXT's code to verify if it pools the IP or directly places the order on the exchange using our IP. Frosty uses CCXT to execute the order. So we cannot be sure on the IP siphoning part as this is a trade that happens via CCXT. In conclusion we Tried to test with CCXT and Exchange API. we tried it both and these were the results.

##  CCXT

The CCXT library is a collection of available crypto _exchanges_ or exchange classes.

-   It uses exchange API for placing the order on specific exchanges. Frosty-Bot uses CCXT library dealing with Exchanges.
    

-   One stop solution for all exchanges.
    

-   If we go with CCXT route the latency might be little higher, but development process will be much quicker.
    

## Exchange API

HTTP-based API with full trading and asset management functionality, with public orderbook and trades data.

-   Every Exchange has its API by which we can directly place order without any using any other open source Library which decreases time latency by some milli-seconds.
    

-   Every Exchange has its API by which we can directly place order without any using any other open source Library which increases time latency by some milli-seconds.
    

-   If we go with Exchange API, latency will be lesser than CCXT, development process will be much more.