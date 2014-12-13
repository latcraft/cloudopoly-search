W00t?
==================

This repository contains description of the first Cloudopoly challenge. Cloudopoly is a set of challenges targeted towards raising awareness of AWS stack. Winners will get prizes from AWS! The first Cloudopoly will have 3 challenges, one per month. By getting 3 times in top 3 you will win a special prize from LatCraft.

Problem definition
==================

Publish a simple web service that accepts 3 keywords as a search criteria. 

Web service must respond with the most popular book (with the highest average rating) for each keyword on the following Amazon websites:

 * amazon.co.uk
 * amazon.fr
 * amazon.de

Expected input: 

        

Expected JSON response:

```
[
  "Practical Vim", 
  "The Linux Command Line", 
  "Mac OS X Snow Leopard"
]
```

# Average book rating calculation

Book rating should be calculated using the following formula:

   R = (R<sub>afr</sub> * N<sub>afr</sub> + R<sub>ade</sub> * N<sub>ade</sub> + R<sub>auk</sub> * N<sub>auk</sub>) / (N<sub>afr</sub> + N<sub>ade</sub> + N<sub>auk</sub>)

- R<sub>afr</sub> - average rating on amazon.fr
- N<sub>afr</sub> - number of ratings on amazon.fr
- R<sub>ade</sub> - average rating on amazon.de
- N<sub>ade</sub>  - number of ratings on amazon.de
- R<sub>auk</sub> - average rating on amazon.co.uk
- N<sub>auk</sub> - number of ratings on amazon.co.uk

NOTE: Only books with **at least 15 reviews** should be considered for result.

# Example searches

The following list shows example URLs that return book query results for a given KEYWORD on the web:

- [amazon.co.uk](http://www.amazon.co.uk/s/ref=nb_sb_noss_1?url=search-alias%3Dstripbooks&field-keywords=<KEYWORD>&sort=review-rank):
    - `http://www.amazon.co.uk/s/ref=nb_sb_noss_1?`
    - `url=search-alias%3Dstripbooks&`
    - `field-keywords=[KEYWORD]&`
    - `sort=review-rank`
- [amazon.de](http://www.amazon.de/s/ref=nb_sb_noss_2?url=search-alias%3Dstripbooks&field-keywords=<KEYWORD>&sort=review-rank):
    - `http://www.amazon.de/s/ref=nb_sb_noss_2?`
    - `url=search-alias%3Dstripbooks&`
    - `field-keywords=[KEYWORD]&`
    - `sort=review-rank`
- [amazon.fr](http://www.amazon.fr/s/ref=nb_sb_noss_2?url=search-alias%3Denglish-books&field-keywords=<KEYWORD>&sort=review-rank):
    - `http://www.amazon.fr/s/ref=nb_sb_noss_2?`
    - `url=search-alias%3Denglish-books&`
    - `field-keywords=[KEYWORD]&`
    - `sort=review-rank`

# Requirements

- Any programming language, any operating system
- Deploy your service to *AWS* *EC2* (free tier)
- Use smallest instance type (`t2.micro`)
- Send IP address of your service before `06.01.2015 16:00` to contest@latcraft.lv
- At `17:00` we start the test! 

# Winner election

Web services, which return the expected result faster, will win.

### Good luck!
