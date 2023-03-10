# Googlesheets Scripts: Crypto Historical Price and ShakepayStats Functions

## Description
The [Crypto historical price](https://github.com/securityiskey/Shakepay-Stats-Google-Sheets/blob/main/Crypto%20historical%20) price function allow you to retrieve historical cryptocurrency prices (BTC or ETH) and display them in (CAD or USD) at a given date and time, and the [ShakePaystats](https://github.com/securityiskey/Shakepay-Stats-Google-Sheets/blob/main/ShakePaystats) function helps you summarize Shakepay transaction data and break it down by month. They work independently from each other, so feel free to copy both functions to your Google Sheet or just one of them.

## Usage
1. Copy the function code for the function you want to use.
2. Open your Google Sheets document.
3. Click on "Extensions" and then "Apps Script".
4. Paste the copied code into the script editor.
5. Save the script with an appropriate name.
6. You can now use the custom function in your Google Sheets document.

### getCryptoPrice Function
The getCryptoPrice function retrieves the historical price of a specified cryptocurrency in a specified fiat currency at a given date and time.

#### Syntax
getCryptoPrice(timestamp, cryptocurrency, fiatcurrency)

#### Parameters
* `timestamp` - Required. The date and time in ISO 8601 format "yyyy-mm-ddThh:mm:ss+00", e.g. "2023-03-01T02:27:37+00".
* `cryptocurrency` - Optional. The cryptocurrency of choice. Valid values are "BTC" and "ETH". Defaults to "BTC" if not specified.
* `fiatcurrency` - Optional. The fiat currency to return the cryptocurrency price in. Valid values are "USD" and "CAD". Defaults to "CAD" if not specified.

#### Example
=getCryptoPrice(B2, "BTC", "CAD")
Assuming cell B2 contains a date "2023-03-01T02:27:37+00", this will return the price of Bitcoin in Canadian dollars on March 1st, 2023.

### getShakeyStats Function
The getShakeyStats function summarizes Shakepay transaction data for a given month.

#### Syntax
getShakeyStats(range)

#### Parameters
* `range` -The range of data to summarize. This should include columns A through K. If left blank, it will assume Columns A through K on your active sheet.

#### Example
=getShakeyStats(Sheet1!A:K)
Assuming the transaction data is in columns A through K of Sheet1, this will return a monthly summary of Shakepay transaction data in a new sheet. Feel free to copy it.

To see how to use these functions, check out the [Example Sheet](https://docs.google.com/spreadsheets/d/1zVC0OqCdjo41pWUnaLXuLWsBJiFGEoO6IHOo24GyuZQ/edit#gid=0).

![image](https://user-images.githubusercontent.com/92526489/223212389-bc16e588-b40d-478a-9090-e004a600a35c.png)
![image](https://user-images.githubusercontent.com/92526489/223526892-8f34537f-f64a-4cbf-917c-36120cd1bf40.png)

## Support
These functions were created as a hobby project to help others. If you encounter any issues or have questions about these functions, feel free to reach out to the creator at their Github user handle @securityiskey. If you'd like to show your support, you can buy the creator a coffee by sending Bitcoin at bc1qtaqvqs4l0psrvhazjggwzh6pxmg0d3ex82qng8 OR if you have Shakepay my username is @einvestor :) cheers
