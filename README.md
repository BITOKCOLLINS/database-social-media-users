# database-social-media-users

Week 10-14
Average income for the users on the dataset is 15014.8230
![image](https://github.com/BITOKCOLLINS/database-social-media-users/assets/160725857/ead88f5f-58fb-4544-a3e8-4025fc6adcc6)

shows the number of users for each gender,
![image](https://github.com/BITOKCOLLINS/database-social-media-users/assets/160725857/61b9acfd-66f3-49b1-9933-89e1dca2b1a3)

Week 15
The Mission:
1. Data Dive
   Importing data is quite easy and great
   the data cover wide number of users
2. Data Fun
   COUNT() =>  counts all rows in the table, giving the total number of userS.
   ![image](https://github.com/BITOKCOLLINS/database-social-media-users/assets/160725857/4c397c16-caa9-4318-bea1-74a6571b026c)
   AVG() => calculates the average income across all users.
             SELECT profession, AVG(income) AS avg_income
             FROM `users-on-social-media`
             GROUP BY profession;
   ![image](https://github.com/BITOKCOLLINS/database-social-media-users/assets/160725857/85391fa8-45c3-4ef0-bd0a-eb56e1452e5a)

  SUM() => sums up the income of all users.
            SELECT SUM(income) AS total_income 
            FROM `users-on-social-media`;
   
   ![image](https://github.com/BITOKCOLLINS/database-social-media-users/assets/160725857/a26244bb-134f-492c-b3fd-0a595c80e7e2)

4. Ask Away
   Which social media platform is most popular among high-income users?
            SELECT platform, COUNT(*) AS high_income_users
            FROM `users-on-social-media`
            WHERE income > 15000
            GROUP BY platform
            ORDER BY high_income_users DESC;
   
   ![image](https://github.com/BITOKCOLLINS/database-social-media-users/assets/160725857/e07c4bbd-30f8-4c55-ad17-a8056eb3ddd4)
   
   In which countries do we find the highest proportion of users interested in Travel content?
            SELECT location, 
                   COUNT(*) AS total_users,
                   SUM(CASE WHEN interests = 'Travel' THEN 1 ELSE 0 END) AS travel_users,
                   (SUM(CASE WHEN interests = 'Travel' THEN 1 ELSE 0 END) * 100.0 / COUNT(*)) AS travel_percentage
            FROM `users-on-social-media`
            GROUP BY location
            HAVING COUNT(*) > 5  
            ORDER BY travel_percentage DESC;
   ![image](https://github.com/BITOKCOLLINS/database-social-media-users/assets/160725857/9270ab99-fcff-4ac0-b4ab-d0cd9ccee68e)

Week 16
4. Showtime!
https://github.com/BITOKCOLLINS/database-social-media-users/blob/main/Bar_graph_average_income.jpg
https://github.com/BITOKCOLLINS/database-social-media-users/blob/main/Pie_chart_Platform.jpg
https://github.com/BITOKCOLLINS/database-social-media-users/blob/main/line_graph_average_income_per_age.jpg

5. Presentation PITCH DECK
https://gamma.app/docs/Social-Media-User-Dataset-Analysis-ad1wro42qr19az3




   
