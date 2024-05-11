# Web-Scraping-Model-for-Amazon-Product-Data
This project is a Python-based web scraping model designed to extract product data from Amazon using BeautifulSoup and requests libraries. The model scrapes product titles, prices, ratings, number of reviews, and availability status from the search results of a given Amazon search query.

## How It Works

The scraping process involves the following steps:

1. *Sending a Request*: The script sends an HTTP GET request to the Amazon search results page using the requests library.

2. *Parsing HTML Content*: Once the page is fetched, BeautifulSoup is used to parse the HTML content of the page.

3. *Extracting Product Links*: The script extracts the links of individual product pages from the search results.

4. *Scraping Product Details*: For each product link, a new HTTP GET request is sent to fetch the respective product page. The script then extracts the product title, price, rating, number of reviews, and availability status using specific functions (get_title, get_price, get_rating, get_review_count, get_availability).

5. *Storing Data*: The extracted data is stored in a Pandas DataFrame and then saved to a CSV file named "amazon_data.csv".

## Usage

To use this model:

1. Replace the placeholder user-agent in the HEADERS variable with your actual user-agent string.
   
2. Set the desired Amazon search query URL in the URL variable.

3. Run the script. It will scrape the data from the Amazon search results and save it to a CSV file named "amazon_data.csv" in the same directory.

## Requirements

- Python 3.x
- BeautifulSoup
- requests
- pandas
- numpy

## Limitations and Considerations

- The script assumes a specific HTML structure of the Amazon search results page. Any changes to the structure may require modifications to the code.
- Continuous scraping of data from Amazon may violate their terms of service. Use this script responsibly and consider Amazon's policies on web scraping.
- The availability status may not always be accurate, especially for dynamically changing inventory.
<table>
  <tr>
    <th>Title</th>
    <th>Price</th>
    <th>Rating</th>
    <th>Reviews</th>
    <th>Availability</th>
  </tr>
  <tr>
    <td>OUBANG 2 Pack Controllers Work with PS4 Controllers</td>
    <td>$37.99</td>
    <td>4.8 out of 5 stars</td>
    <td>8 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>PlayStation 4 Slim 1TB Console</td>
    <td></td>
    <td>4.7 out of 5 stars</td>
    <td>15,164 ratings</td>
    <td></td>
  </tr>
  <tr>
    <td>PlayStation 4 Slim 1TB Console - Only On PlayStation Bundle</td>
    <td></td>
    <td>4.8 out of 5 stars</td>
    <td>8,860 ratings</td>
    <td>Only 3 left in stock - order soon</td>
  </tr>
  <tr>
    <td>Hunting Simulator - PlayStation 4</td>
    <td>$16.61</td>
    <td>4.3 out of 5 stars</td>
    <td>937 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>BlueFire Professional 3.5mm PS4 Gaming Headset...</td>
    <td></td>
    <td>4.4 out of 5 stars</td>
    <td>8,257 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>Horizon Zero Dawn Complete Edition Hits - PlayStation 4</td>
    <td>$22.45</td>
    <td>4.8 out of 5 stars</td>
    <td>10,127 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>Beastron PS4 Controller Charging Station, PS4 ...</td>
    <td></td>
    <td>4.4 out of 5 stars</td>
    <td>568 ratings</td>
    <td>Currently unavailable.</td>
  </tr>
  <tr>
    <td>PlayStation 4 Slim 1TB Limited Edition Console...</td>
    <td></td>
    <td>4.6 out of 5 stars</td>
    <td>711 ratings</td>
    <td></td>
  </tr>
  <tr>
    <td>PlayStation 4 500GB Console [Old Model][Discontinued]</td>
    <td></td>
    <td>4.6 out of 5 stars</td>
    <td>13,569 ratings</td>
    <td></td>
  </tr>
  <tr>
    <td>Sony Playstation PS4 1TB Black Console</td>
    <td>$619.00</td>
    <td>4.7 out of 5 stars</td>
    <td>853 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>PlayStation 4 Slim 1TB Gold Console [Discontinued]</td>
    <td></td>
    <td>4.6 out of 5 stars</td>
    <td>707 ratings</td>
    <td>Only 1 left in stock - order soon</td>
  </tr>
  <tr>
    <td>DualShock 4 Wireless Controller for PlayStation...</td>
    <td>$58.75</td>
    <td>4.7 out of 5 stars</td>
    <td>140,711 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>DualShock 4 Wireless Controller for PlayStation...</td>
    <td>$63.00</td>
    <td>4.7 out of 5 stars</td>
    <td>140,711 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>PS4 Stand Cooling Fan Station for PlayStation ...</td>
    <td>$25.99</td>
    <td>4.3 out of 5 stars</td>
    <td>6 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>Little Witch Nobeta – PlayStation 4</td>
    <td>$49.99</td>
    <td>Previous page of related Sponsored Products</td>
    <td></td>
    <td>This item will be released on June 30, 2023.</td>
  </tr>
  <tr>
    <td>PS4 Stand Cooling Fan Station for PlayStation ...</td>
    <td>$25.99</td>
    <td>4.3 out of 5 stars</td>
    <td>6 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>DualShock 4 Wireless Controller for PlayStation...</td>
    <td>$61.50</td>
    <td>4.7 out of 5 stars</td>
    <td>140,711 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>Sony PlayStation 4 Dualshock 4 Wireless Controller...</td>
    <td></td>
    <td>4.5 out of 5 stars</td>
    <td>1,545 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>NBA 2K23 - PlayStation 4</td>
    <td>$59.99</td>
    <td>4.5 out of 5 stars</td>
    <td>206 ratings</td>
    <td>In Stock</td>
  </tr>
  <tr>
    <td>【Upgraded】YUYIU Wireless Controller for Ps4 Re...</td>
    <td></td>
    <td>4.4 out of 5 stars</td>
    <td>455 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>Hermitshell Hard EVA Travel Case Fits Sony PlayStation...</td>
    <td>$75.99</td>
    <td>4.2 out of 5 stars</td>
    <td>111 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>NHL 23 - PlayStation 4</td>
    <td>$59.99</td>
    <td>4.3 out of 5 stars</td>
        <td>24 ratings</td>
    <td>In Stock</td>
  </tr>
  <tr>
    <td>HDMI Cable for Playstation 2 & Playstation 1 C...</td>
    <td></td>
    <td>4.5 out of 5 stars</td>
    <td>2,302 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>Wireless Controller, Console for Ps-4/Pro/Ps-3...</td>
    <td></td>
    <td>5.0 out of 5 stars</td>
    <td>5 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>Dying Light 2 Stay Human - PlayStation 4</td>
    <td>$29.99</td>
    <td>4.6 out of 5 stars</td>
    <td>944 ratings</td>
    <td>In Stock</td>
  </tr>
  <tr>
    <td>OUBANG 2 Pack Controllers Work with PS4 Contro...</td>
    <td>$37.99</td>
    <td>4.8 out of 5 stars</td>
    <td>8 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>NHL 22 (PS4)</td>
    <td>$18.92</td>
    <td>4.6 out of 5 stars</td>
    <td>282 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>eXtremeRate Blood Purgatory Patterned Custom F...</td>
    <td></td>
    <td>4.2 out of 5 stars</td>
    <td>4,357 ratings</td>
    <td>Not Available</td>
  </tr>
  <tr>
    <td>Ps4 Controller Skin Silicone Case Grip Glow in...</td>
    <td></td>
    <td>4.2 out of 5 stars</td>
    <td>1,415 ratings</td>
    <td>Not Available</td>
  </tr>
</table>
