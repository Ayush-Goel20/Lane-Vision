# Lane-Vision
# 🚦 Traffic Flow Analysis  
**Lane-wise Vehicle Counter using YOLOv8 + OpenCV**  

A Google Colab–ready AI system to detect, track, and count vehicles **lane by lane in real time** using **YOLOv8** and **OpenCV**.  
Counts are triggered only when a vehicle crosses a **virtual line** in its lane, preventing duplicate counts.  

---

## 📌 Features
- 🚗 Detects **cars, buses, trucks, motorcycles**  
- 🎯 Tracks vehicles using **IoU + Hungarian algorithm**  
- 📊 Counts only on **line crossing in correct lane** (no duplicates)  
- 📑 Exports results to **CSV** (Vehicle ID, Lane, Timestamp)  
- 🎥 Produces an **overlay video** with live counts & bounding boxes  
- ☁ Runs fully in **Google Colab**  

---

## 🛠️ Tech Stack

| Tool     | Purpose                                |
|----------|----------------------------------------|
| **YOLOv8** | Vehicle detection                     |
| **OpenCV** | Video processing & drawing overlays   |
| **NumPy / SciPy** | Tracker & math operations      |
| **yt-dlp** | Download YouTube videos in Colab      |

---

## 🚀 How It Works

1. **Input Video** → Example: [Sample Video](https://youtu.be/MNn9qKG2UFI?si=2Ri4dRrgg_aj5egb)  
2. **YOLOv8 Detection** → Finds vehicles in each frame  
3. **Tracking** → Matches vehicles across frames using IoU + Hungarian algorithm  
4. **Counting** → Each lane has a virtual line; a vehicle is counted once when its centroid crosses the line  
5. **Overlay Video**  
   - 🔴 Red lines = counting lines  
   - 🟩/🟧 Boxes = tracked vehicles  
   - 📊 Top-left = live lane counts  

---

## 💡 Use Cases
- Smart city **traffic monitoring**  
- **Lane usage analytics** for infrastructure planning  
- **Accident detection** & traffic management  
- **Adaptive traffic signal control** systems  

---

## 📂 Project Structure
```bash
Traffic_Flow_Analysis/
│── notebooks/       # Google Colab notebooks
│── data/            # Input videos / datasets
│── output/          # Processed results (CSV, overlay video)
│── README.md        # Documentation


