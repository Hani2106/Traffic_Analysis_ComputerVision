📘 README.md — Traffic Analysis Using Computer Vision & Power BI
🚦 Traffic Flow Analysis using Computer Vision & Data Analytics

Technologies: OpenCV • Python • Vehicle Tracking • Line Crossing Algorithm • Power BI • Pandas

📌 Project Overview

This project performs automatic vehicle detection, tracking, and counting using a CCTV traffic video and then converts the results into structured data for business analytics.

The pipeline combines Computer Vision (CV) and Data Analytics to deliver:
=>Real-time vehicle detection using background subtraction
=>Object tracking using centroid tracking
=>Accurate vehicle counting using a virtual horizontal line
=>Direction detection (UP / DOWN)
=>Export to CSV with event details (vehicle_id, time, direction, cx, cy)
=>Power BI dashboard for traffic insights

This end-to-end workflow demonstrates how raw video can be transformed into actionable insights for transportation systems, smart cities, and traffic optimization.

🧠 Key Features
🔹 1. Computer Vision Pipeline

->Reads traffic video using OpenCV
->Detects motion using MOG2 background subtractor
->Noise removal using thresholding + morphological operations
->Extracts vehicle bounding boxes and centroids (cx, cy)

🔹 2. Vehicle Tracking

->Each moving vehicle gets a unique ID
->Tracks movement across frames
->Prevents double-counting (“counted” flag)
->Saves centroid positions for future analysis (e.g., speed, lane analysis)

🔹 3. Line-Crossing Vehicle Counting

->A horizontal line is drawn across the frame.
->A vehicle is counted when its centroid crosses the line:
->UP → crossing from bottom to top
->DOWN → crossing from top to bottom
->This allows direction-wise flow measurement.

🔹 4. CSV Data Export

Each crossing event is saved as:

vehicle_id	time_sec	direction	cx	cy
13	1.13	UP	1007	358
18	2.14	DOWN	343	360

This file becomes the foundation for analytics.

🔹 5. Power BI Dashboard
A clean, interactive dashboard was created featuring:

->Total Vehicles
->Total UP Vehicles
->Total DOWN Vehicles
->Traffic Flow Over Time (Line Chart)
->Direction Comparison (Bar Chart)
->Lane Distribution (Pie/Donut Chart)
->Slicers: Direction, Lane, Time Range
The dashboard provides a clear overview of traffic conditions across the video duration.

🛠 Tech Stack
🖥 Computer Vision
->Python
->OpenCV
->Background Subtraction (MOG2)
->Contour Detection
->Centroid Tracking Algorithm

📊 Analytics

->Pandas
->Power BI
->Data Cleaning & Transformation

📷 How It Works (Concept)

Video Frame → Foreground Extraction
Contours → Vehicles → Centroid Calculation (cx, cy)
Track centroids across frames
Detect line crossing → Count
Save data → CSV
Visualize insights in Power BI

📊 Insights Provided

->Total number of vehicles detected
->Direction-wise flow (UP vs DOWN)
->Traffic intensity across time
->Lane usage patterns using cx
->Visual analytics using Power BI

🚀 Results

=>Successfully detected & tracked vehicles in real traffic footage
=>Extracted structured data suitable for analytics
=>Built a clean, modern, and interactive dashboard
=>Demonstrated a practical CV + Data Analytics integration
=>Ready for real-world applications such as:
=>Smart traffic light systems
=>Congestion monitoring
=>Traffic planning
=>Vehicle flow analysis

🔮 Future Improvements
=>YOLO-based accurate vehicle detection
=>Multi-lane detection
=>Speed estimation
=>Vehicle classification (car, truck, bike)
=>Anomaly detection (wrong way, over-speeding)

!! You can find the Video from : https://www.kaggle.com/datasets/gauravduttakiit/highway-traffic

🧑‍💻 Author
Hani Patel
Linkedin : https://www.linkedin.com/in/hani-patel-6a9370265/
Email : hanipatel0621@gmail.com
⭐ If you found this useful, please star the repository!
