# Data analysis exercises
## 1. Project Overview & Dataset
This project was a great opportunity for me to level up my data analysis skills, with a specific focus on Data Modeling. For this project, I wanted to challenge myself with architecting a solid Snowflake Schema where the dataset does not have a clear relationships between tables

A quick look at the data I worked with:
<p align="left">
   <br>
    <img width="837" height="422" alt="458daa9e-a24f-4394-ba00-674386ea8283" src="https://github.com/user-attachments/assets/a798a110-c76b-42c1-9e2b-54800af99cdd" />
</p>

`ad`: Contains all the ad-related info, using `video_id` as the primary key.
<p align="left">
   <br>
    <img width="837" height="252" alt="908fd708-9e53-4884-a46e-5c1f588f9f14" src="https://github.com/user-attachments/assets/66ff48b3-1bdd-4169-bfad-eb80d47b69af" />
</p>

`video_order`: Gives more context about each video, using `video_id` as primary key
<p align="left">
   <br>
  <img width="840" height="490" alt="2d2ea742-8ed9-4af3-8646-a80b8ec7c98f" src="https://github.com/user-attachments/assets/6df64389-ef8a-4283-b44c-3a166650a4f2" />
</p>

`order`: This table includes the info by `order_id` (primary key) 
<p align="left">
   <br>
<img width="840" height="388" alt="39019a81-ee3a-4ff7-a06b-01595fa0e899" src="https://github.com/user-attachments/assets/cfb0c319-32cc-4c22-90fc-fdf45a24dc7b" />
</p>

`order_item`: This is the heart of the model. Since one order can have multiple products, you’ll see `order_id` appearing more than once here, making it the perfect Fact table to track sales at a granular level.

## 2. Modeling Steps
To get the model running smoothly, I spent a lot of quality time in Power Query. Here are steps I have done to build data model:
<p align="left">
   <br>
  <img width="1919" height="1079" alt="83eed999-6d26-457e-ad61-1a107c760903" src="https://github.com/user-attachments/assets/88f6fe03-8544-40a6-8126-b6b5e7efd572" />
</p>

- **Data Pre-processing**: I made sure every column was in the right format and ready to talk to other tables.<br>
- **Merging & Linking**: I used Merge and other transformation tools to organize the data into clear Dimension and Fact tables.<br>
- **Designing the Schema:** My main goal was to build an optimal Snowflake structure, ensuring that the relationships between tables were logical, clean, and efficient for reporting.

## 3. What I have learned

- **Preparation is everything:** Good pre-processing makes modeling a hundred times easier.
- **The "Big Picture":** Building a robust schema helped me visualize exactly how different parts of the business (Ads, Videos, Orders) connect with each other.
- **Data Integrity:** I realized that a well-built model doesn't just look good. It actually protects the data. It helped me spot missing information and ensured that my final numbers stayed consistent and accurate.
