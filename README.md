Crypto Historical Price and ShakepayStats Functions
Description
These functions allow you to retrieve historical cryptocurrency prices and summarize Shakepay transaction data for a given month.

Usage
Go to the Github repository for the Crypto Historical Price and ShakepayStats functions.
Copy the function code for the function you want to use.
Open your Google Sheets document.
Click on "Tools" and then "Script editor".
Paste the copied code into the script editor.
Save the script with an appropriate name.
You can now use the custom function in your Google Sheets document.
getCryptoPrice Function
The getCryptoPrice function retrieves the historical price of a specified cryptocurrency in a specified fiat currency at a given date and time.

Syntax
scss
Copy code
getCryptoPrice(timestamp, cryptocurrency, fiatcurrency)
Parameters
timestamp - Required. The date and time in ISO 8601 format "yyyy-mm-ddThh:mm:ss+00", e.g. "2023-03-01T02:27:37+00".
cryptocurrency - Optional. The cryptocurrency of choice. Valid values are "BTC" and "ETH". Defaults to "BTC" if not specified.
fiatcurrency - Optional. The fiat currency to return the cryptocurrency price in. Valid values are "USD" and "CAD". Defaults to "CAD" if not specified.
Example
python
Copy code
=getCryptoPrice(B2, "BTC", "CAD")
Assuming cell B2 contains a date "2023-03-01T02:27:37+00", this will return the price of Bitcoin in Canadian dollars on March 1st, 2023.

getShakeyStats Function
The getShakeyStats function summarizes Shakepay transaction data for a given month.

Syntax
scss
Copy code
getShakeyStats(range)
Parameters
range - Required. The range of data to summarize. This should include columns A through K.
Example
scss
Copy code
=getShakeyStats(Sheet1!A:K)
Assuming the transaction data is in columns A through K of Sheet1, this will return a monthly summary of Shakepay transaction data in a new sheet.
