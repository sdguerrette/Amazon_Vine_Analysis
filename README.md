# Overview
This analysis was undertaken to help determine whether the Amazon Vine program, in which Amazon allows free products to be sent to consumers in exchange for reviews, breeds positive bias in the ratings left by the Vine reviewers. To accomplish this analysis, we used a dataset provided by Amazon that contained a large number of reviews in the Home Entertainment category. These reviews were read from an AWS S3 bucket into a Google Collab notebook using pyspark, after which they were manipulated into tables and written into an AWS RDS database linked with Postresql. One of these tables, regarding the Vine reviews, was then exported to Jupyter Notebooks in which we used the Pandas library to parse, filter, and compute the data into useable metrics.
# Results
The following results were computed from the Home Entertainment category on Amazon.
- There are 261 reviews that originated from the Vine program.
![Screen Shot 2022-07-10 at 7 32 24 PM](https://user-images.githubusercontent.com/100643755/178177910-ef025e78-80f0-4a03-b268-4c5902c6ac9a.png)
- There are 24040 non-Vine reviews. 
![Screen Shot 2022-07-10 at 7 33 10 PM](https://user-images.githubusercontent.com/100643755/178178018-4a044c04-4206-4925-a557-435ce0cddaab.png)
- 106 of the 261 Vine reviews were rated as 5-stars.
![Screen Shot 2022-07-10 at 7 33 49 PM](https://user-images.githubusercontent.com/100643755/178178124-964428e3-c8cd-4889-af1f-32e2077a143b.png)
- 10899 of the 24040 non-Vine reviews were rated as 5-stars.
![Screen Shot 2022-07-10 at 7 35 17 PM](https://user-images.githubusercontent.com/100643755/178178313-3482421e-4ac7-4d03-bb5e-96ff1b01738d.png)
- 40.61% of the Vine reviews were rated as 5-Stars.
![Screen Shot 2022-07-10 at 7 35 58 PM](https://user-images.githubusercontent.com/100643755/178178380-88c11e1a-2e37-4be4-970a-e02c7cafc27e.png)
- 45.34% of the non-Vine reviews were rated as 5-Stars.
![Screen Shot 2022-07-10 at 7 36 30 PM](https://user-images.githubusercontent.com/100643755/178178447-48033e89-ef41-4164-9dc9-d5d97357069a.png)

# Summary
Based on the dataset and analysis performed, it is our conclusion that the Vine program does not introduce any positive bias to the star ratings left on product reviews. In fact, non-Vine reviewers were about 5% more likely to give a product a perfect 5-Star score. While we feel confident in this result, further analysis could be completed to confirm and expand on these findings. We recommend repeating this analysis for 4-Star ratings as well, as there is a possibility that those who receive free products are more aware of the potential bias in there reviews, and therefore more likely to not give a perfect score. 
