# Book-Recommendation-System
Building Recommendation System based on user-based collaborative filtering and content based approaches.

# Book-Crossing
The Book-Crossing dataset is a collection of user ratings of books. It comes with both explicit ratings (1-10 stars) and implicit ratings
(user interacted with the book). The data was compiled by Cai-Nicolas Ziegler of IIF and can be found here at
http://www2.informatik.uni-freiburg.de/~cziegler/BX/.

# Following files are required for the ratings:
BX-Book-Ratings.csv (referred to as the ratings file)
BX-Users.csv (referred to as the users file)
BX-Books.csv (referred to as the books file)
All three files are available in the CSV dump file (BX-CSV-Dump.zip).

# The converting script is run as follows:
./bookcrossing.py BX-Book-Ratings.csv BX-Users.csv BX-Books.csv

# NOTE
The converting script prunes users and books in the following manner:
1. Any entry in the rating file that does not match to a book in the books file or a user in the user file is removed.
2. Any user in the users file is removed if they do not have at least one rating saved from the rating file.
3. In this manner invalid reviews and invalid (and inactive) users are removed before the conversion to JSON.
