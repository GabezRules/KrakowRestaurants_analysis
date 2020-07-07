# Krakow restaurants analysis
How the location and menu options affect the popularity and ratings of visitors? Data that I collect, analyze, and visualize by myself - to learn.

Repo will include:
  * two CSV files with restaurant data and reviews left by users,
  * two scrappers: one to get links to restaurants and one to get reviews and data of specific restaurants
  * analysis of the files where I will try to answer the questions asked before
  * a ML model to predict the rating of the restaurant based on location and options like cuisine type or prices
  
Technologies used so far: Python 3, Selenium, BeautufilSoup, Matplotlib, Seaborn

# How to use scrapper:

BEFORE RUNNING THE CODE MAKE SURE YOU HAVE A CHROMEDRIVER INSTALLED

Complete variables:

 * CHROME_PATH - a path where your chrome web driver is saved
 * PATH_TO_SAVE_COMMENTS - path to the file where the CSV with comments will be saved
 * PATH_TO_SAVE_LINKS - path to the file where the CSV with scrapped links will be saved
 * PATH_TO_SAVE_RESTAURANTS - path to the file where the CSV with scrapped restaurants info will be saved
 * (optional) MAX_LINKS - number of restaurants you want to scrap
 * main_url - the URL you want to start scraping from
 
Run the code with uncommented lines:
  collector = LinkCollector(main_url)
  collector.setup_link_collector()
 
The LinkCollector should end the work by itself. If you want to stop scrapping, close your web driver and run lines:
  save_links()
  setup_scrapper_and_start_process()
  
After that, the SinglePageScrapper will start collecting data for you. It may take a while (my first run took more than 24 hours), but you can close your web driver to stop, and then run the lines below to save your data:
  save_dataframe()
  save_places()
