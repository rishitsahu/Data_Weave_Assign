# Data_Weave_Assign
## Steps to run
Keeping main.py, today.json and yesterday.json in the same file, run the following commands:
   pip install tqdm
   python main.py
## Tasks
# Task1 : Number of URLH which are overlapping (Common) in two files.
Made two sets of today's URLHs and yesterday's URLHs. For each of the URLH in the 1st set, checked for the occurence in the other set. If found, then appended it in a list of common_urlhs

# Task2 : For all the URLH which are overlapping, calculate the price difference (wrt available_price) if there is any between yesterday's and today's crawls (scraped data).               There might be duplicate URLHs in which case you can choose the first valid (with http_status 200) record.
Checked for each item in common_urlh that has http_status = 200 and available price difference not equal to zero and then stored the absolute value of price_difference
in a dictionary.

# Task3 :  Number of Unique categories in both files
Again made two sets for storing today's and yesterday's category. Then printed the length of the sets.

# Task4 : Display List of categories which is not overlapping (Common) from two given files
Used the previously created sets for the categories. For each item in set1, checked it's occurence in set2. If not found then appended the category in a separate list
for storing the uncommon categories.

# Task5 : Generate the stats with count of urlh for all taxonomies (taxonomy is concatenation of category and subcategory separated by " > ") for today's file.
Made a dictionary for storing the taxonomies. Checked for the presence of the taxonomy in the dictionary. If already present then increased it's counter by 1 else initialised it by 1.

# Task6 : Generate a new file where mrp is normalized. If there is a 0 or a non-float value or the key doesn't exist, make it "NA".
Checked for mrp in each row. Modified it, if it's value is 0 or it doesn't exist or it's a non-float value. Then generated a new file to show the relevant changes.

# Task7 : Display the title and price of 10 items having least price
The idea was to use a dictionary and keep the title as the key of the dictionary so that the price of the same could be kept in the values. So check the available price for the item and assign as the value to the key. Then sort it in ascending order on the basis of the price and take the top 10 values

# Task8 :  Display the top 5 subcategory having highest items.
Make a key value pair as subcategory,no. Of items . Checked for the presence of the key-value pair in the dictionary. If already present then increased it's counter by 1 else initialised it by 1. Sorted it and displayed top 5 items.

# Task9 : Display stats of how many items have failed status (http_status other than 200 is to be considered as failure.
For each row in the dataset, checked for the http_status. If not found 200 then increased its counter by 1 in the dictionary. If it was not present in the dictionary then initialised it by 1.

## Author

Name: Rishit Sahu

Email: rishitsahu17@gmail.com

Phone No.: +91 9588036568

https://github.com/rishitsahu
