# Smart-Retail-Product-Detection-and-Analysis-Using-YOLOv8

GDG OnCampus VIT-AP AI/ML & Data Analytics Team - Team id: 3 

 Team Members:
Khushi Rawat 23BCE7131,
Dhani Sinha 24BCE7569,
Ramsha Annam 23BCE8215


This project aims to develop a smart retail product detection system using computer vision to detect products picked by customers in a retail store environment. The system leverages two YOLOv8 models to detect grocery items, hand, store basket and trolly. By identifying hand-to-product and product-to-store-basket-or-trolly interactions, it can accurately determine which products customers have picked. The solution integrates with a Flask-based web application, allowing users to upload videos or images for product and hand detection. The system processes these inputs in real time, stores the results in a database, and provides actionable insights into customer behaviour.


⚙️ Project Modules:
1. User Authentication:
   - Secure login and signup functionality using Flask.  
   - Session management to control access to the dashboard.

2. Product and Hand Detection:  
   - YOLOv8 models trained to detect grocery items and hand.  
   - Detection pipeline processes both images and videos.  
   - Checks if hand overlaps with product bounding boxes to mark products as picked.

3. Data Storage and Management: 
   - Detected product and action data is stored in an SQL database.  
   - Stores customer interactions for further analysis.

4. Web Interface (Flask Dashboard):  
   - Upload videos or images for detection.  
   - View detected products and interactions in a user-friendly interface.  


🧠 Technology Stack:
- Backend: Flask (Python)
- Frontend: HTML, CSS, JavaScript
- Database: SQLite (SQLAlchemy ORM)
- Computer Vision: OpenCV, YOLOv8 (Ultralytics)
- Models:
    - Grocery Items Detection Model
    - Hand Keypoint Detection Model


🎥 Workflow:
1. User Authentication:  
   - Login or Signup to access the system.
   - Access is granted to the dashboard upon successful login.

2. Video/Image Upload:  
   - Upload videos or images via the web interface.
   - Files are processed and stored in the server.

3. Detection and Analysis:  
   - YOLOv8 models detect grocery items and hand.
   - If the box boundary of a hand overlap with a product’s bounding box, and later that of a product with a store basket or trolly, it is marked as "picked."

4. Data Storage: 
   - Detected actions and product information are stored in a SQLite database.
   - Results are visualized on the dashboard.

5. Report Generation: 
   - Users can view detected products and analyze customer behaviour.


🌐 Use Cases:
- Retail stores for smart shelf monitoring.
- Analyzing customer behaviour for product placement optimization.
- Enhancing the shopping experience with real-time product tracking.


 Architectural diagram:
![I](https://github.com/user-attachments/assets/3d4b251c-7733-42ac-9e9e-335195318b07)


Dataset Used:

We initially integrated a dataset we found online with 6000 images of Indian products, manually taken and labelled. Still, the results didn't come out great so we then implemented a small, 936 images, self-built images dataset on our project. We couldn't find any good store CCTV footage online that could be used to train the model with real-world data, so we relied on publicly available images of store items and simulated interactions like picking and placing products in a cart. However, not many relevant images were available online, out of which not all could be used for training, and the quality and compatibility of the chosen images varied significantly, resulting in a limited and inconsistent dataset for training YOLOv8.

link: 
1) 6000 images dataset: https://universe.roboflow.com/iit-patna-qg1jh/grocery_items-7i2em
2) self-built dataset: https://drive.google.com/drive/folders/18O4x3QUO2-m8umWrZw9lQgj_B6JjR2gd?usp=sharing

References:
Research papers-

• Retail store customer behaviour analysis system: Design and Implementation by Tuan Dinh Nguyen, Keisuke Hiharab, Tung Cao Hoanga, Yumeka Utadab, Akihiko Toriib, Naoki Izumib, Nguyen Thanh Thuya and Long Quoc Trana,∗

• Retail Store Analytics Using Facial Recognition by Nishant Sawant, Akansha Rai, Saiprasad Parab, Bansi Ghanva

• Revolutionizing Retail Analytics: Advancing
Inventory and Customer Insight with AI by
Ahmed Hossam, Ahmed Ramadan, Mina Magdy, Raneem Abdelwahab, Salma Ashraf, Zeina Mohamed

•Deep learning and multi-modal fusion for real-time multi-object tracking: Algorithms, challenges, datasets, and comparative study by Xuan Wang, Zhaojie Sun, Abdellah Chehri, Gwanggil Jeon, Yongchao Song
