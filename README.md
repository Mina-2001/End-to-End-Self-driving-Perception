#  End-to-End Self-Driving Perception

This project demonstrates a **complete perception pipeline** for self-driving cars by combining three key tasks:

- **Object Detection** with [YOLOv8](https://github.com/ultralytics/ultralytics)  
  → Detects cars and traffic lights in road images.  
- **Traffic Light Classification**  
  → Identifies the color/state (red, yellow, green) of each detected traffic light.  
- **Road Segmentation** with [SegFormer](https://huggingface.co/nvidia/segformer-b0-finetuned-cityscapes-1024-1024)  
  → Marks the drivable area of the road with a teal overlay.  

All results are combined into a **single annotated image** showing:  
 - Cars (white boxes)  
 - Traffic lights with colored labels  
 - Drivable road area overlay  

---

##  Example Output
Cars, traffic lights (red/yellow/green), and drivable road area:

![Example Output](artifacts/output.png)

---

##  Features
- **YOLOv8 Detection** – robust real-time object detection.  
- **Traffic Light Color Classification** – HSV-based heuristic or CNN classifier.  
- **SegFormer Segmentation** – transformer-based segmentation model for urban scenes.  
- **Unified Overlay Visualization** – combines detection, classification, and segmentation.  
