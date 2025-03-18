# Smart-Retail-Product-Detection-and-Analysis-Using-YOLOv8-and-Hand-Keypoint-Detection

GDG OnCampus VIT-AP AI/ML & Data Analytics Team - Team id: 3 

 Team Members:
Khushi Rawat 23BCE7131,
Dhani Sinha 24BCE7569,
Ramsha Annam 23BCE8215


This project aims to develop a smart retail product detection system using computer vision to detect products picked by customers in a retail store environment. The system leverages two YOLOv8 models to detect grocery items and hand. By identifying hand-to-product interactions, it can accurately determine which products customers have picked. The solution integrates with a Flask-based web application, allowing users to upload videos or images for product and hand detection. The system processes these inputs in real time, stores the results in a database, and provides actionable insights on customer behaviour.


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
   - If 5 or more of the hand overlap with a product’s bounding box, it is marked as "picked."

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
![WhatsApp Image 2025-03-18 at 09 04 12_217c7880](https://github.com/user-attachments/assets/feefc4c7-ea72-4231-928a-6739b1f0a205)


References:
Research papers-

• Retail store customer behavior analysis system: Design and Implementation by Tuan Dinh Nguyena, Keisuke Hiharab, Tung Cao Hoanga, Yumeka Utadab, Akihiko Toriib,Naoki Izumib, Nguyen Thanh Thuya and Long Quoc Trana,∗

• Retail Store Analytics Using Facial Recognition by Nishant Sawant, Akansha Rai, Saiprasad Parab, Bansi Ghanva

• Revolutionizing Retail Analytics: Advancing
Inventory and Customer Insight with AI by
Ahmed Hossam, Ahmed Ramadan, Mina Magdy, Raneem Abdelwahab, Salma Ashraf, Zeina Mohamed

•Deep learning and multi-modal fusion for real-time multi-object tracking: Algorithms, challenges, datasets, and comparative study by Xuan Wang, Zhaojie Sun, Abdellah Chehri, Gwanggil Jeon, Yongchao Song
