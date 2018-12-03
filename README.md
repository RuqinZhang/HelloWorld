# Price Comparison Tool: Find your favorite snacks near Columbia University!
## What is it?

**Price Comparison Tool** is a program which compares the prices of the same product
in different shops near Columbia University, and dispalys a list of prices,sales information and image link to the buyer. It helps the buyer to decide on the best place to buy the product. Besides, this program also offers the function of sending discount information via E-mail.


## Main Features

**Crawler**: Grocery information of H-mart, Westside Market and SeasonsKosher (typical shops near Columbia Unversity) is crawled and exported to a csv file.

**Price comparison**: 
The final result is presented in the form of GUI. Users run gui.ipynb, enter the product they want, and sort by price or sale information.

**Discount reminder**: When users leave their E-mail address in our GUI, they will be automatically notified if there is discount on the products they searched.

## Where to get it
The source code is currently hosted on GitHub at: https://github.com/RuqinZhang/HelloWorld.git


## Users' Guide

**Part 1- Prepare for Web Crawler**
Installation:

1. Install selenium package

   ```sh
   pip install selenium
   ```

2. Make sure you have Firefox browser and download geckodriver from the following links:
   https://github.com/mozilla/geckodriver/releases

3. Unzip geckodriver and put it into the following folder:  
./Anaconda/Scripts

**Part 2 - Use our GUI!**
  GUI testing process:
1. Run gui.ipynb
2. Enter the product name in the first entry, click Search button.
3. Click Price button to sort by price and Sale button to sort by sale.
4. Enter your email address and click "Confirm Email and Subscribe" button.
5. Close GUI. 

**DO NOT RUN GUI ON VIRTUAL MACHINE!**

**Part 3- Subscribe Sales Email**

The searching history in GUI will be recorded in **"Searching_log.txt"**

We run **"Email_sender.ipynb"** daily and notify the users. 

## Guide for test

1. Install relevant packages:

   ``pandas`` >= 0.23.4

   ``csv`` >= 1.0

   ``bs4`` >= 4.6.0

   ``selenium`` >= 3.141.0

   ``urllib``

   ``tkinter``

   ``sys``
2. Run ``Hmart.ipynb``, ``Seasons.ipynb``, ``Westside.ipynb``

   Output: ``Hmart_allgroceries.csv``, ``Seasons_allgroceries.csv``, ``Westside_allgroceries.csv``

3. Run ``read_data.ipynb`` 

4. Run ``gui.ipynb`` and test GUI

   Enter the product name in the first entry, click Search button.
   
   Click Price button to sort by price and Sale button to sort by sale.  
   
   Enter your email address and click "Confirm Email and Subscribe" button.  
   
   Close GUI.
   
   Automatically create ``Searching_log.txt``, record the subscriber and search history.
 
5. Run ``Email_sender.ipynb`` to send subscribers emails
