# Data analysis exercises
## Project Overview & Dataset
This project was a great opportunity for me to level up my data analysis skills, with a specific focus on Data Modeling. For this project, I wanted to challenge myself with architecting a solid Star Schema where the dataset does not have a clean relationships between tables

A quick look at the data I worked with:
<p align="left">
   <br>
    <img alt="Picture1d" src="https://github.com/user-attachments/assets/51281980-68b6-4f6c-92c2-9070853d8591" />
</p>
ad: Contains all the ad-related info, using video_id as the primary key.
<p align="left">
   <br>
    <img width="837" height="252" alt="908fd708-9e53-4884-a46e-5c1f588f9f14" src="https://github.com/user-attachments/assets/66ff48b3-1bdd-4169-bfad-eb80d47b69af" />
</p>
video_order: Gives more context about each video, using order_id as primary key
<p align="left">
   <br>
  <img width="840" height="388" alt="39019a81-ee3a-4ff7-a06b-01595fa0e899" src="https://github.com/user-attachments/assets/af5c7db6-e02d-46b7-a15c-f74414e95f76" />
</p>
order: This table includes the info by order_id (primary key) 
<p align="left">
   <br>
<img width="840" height="388" alt="39019a81-ee3a-4ff7-a06b-01595fa0e899" src="https://github.com/user-attachments/assets/cfb0c319-32cc-4c22-90fc-fdf45a24dc7b" />
</p>
order_item: This is the heart of the model. Since one order can have multiple products, you’ll see order_id appearing more than once here, making it the perfect Fact table to track sales at a granular level.

## Modeling Steps
To get the model running smoothly, I spent a lot of quality time in Power Query. Here are steps I have done to build data model:
<p align="left">
   <br>
  <img width="1919" height="1079" alt="5ce2bb6f-5479-4802-8e8b-d585e2887317" src="https://github.com/user-attachments/assets/e16c742e-b9ef-4850-88da-2e8d29e2789a" />
</p>

- **Data Pre-processing**: I made sure every column was in the right format and ready to talk to other tables.<br>
- **Merging & Linking**: I used Merge and other transformation tools to organize the data into clear Dimension and Fact tables.<br>
- **Designing the Star Schema:** My main goal was to build an optimal "Star" structure, ensuring that the relationships between tables were logical, clean, and efficient for reporting.

## What I have learned

- **Preparation is everything:** Good pre-processing makes modeling a hundred times easier.
- **The "Big Picture":** Building a robust schema helped me visualize exactly how different parts of the business (Ads, Videos, Orders) connect with each other.
- **Data Integrity:** I realized that a well-built model doesn't just look good. It actually protects the data. It helped me spot missing information and ensured that my final numbers stayed consistent and accurate.
