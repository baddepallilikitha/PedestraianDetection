📁 Project Structure
This repository includes:

📓 yolo_comparison_for_pedestrian_detection.ipynb: Jupyter notebook containing full implementation

🧠 Code to load and train YOLO models (YOLOv5, YOLOv8, YOLOv11)

📸 Input image/video samples

📊 Output visualizations with bounding boxes

📈 Performance metrics for model comparison

🚀 How to Use
1. Clone the Repository
git clone https://github.com/your-username/yolo_comparison_for_pedestrian_detection.git
cd yolo_comparison_for_pedestrian_detection

2. Run in Google Colab (Recommended)
You can open the notebook directly in Colab for easier GPU access.

3. Install Dependencies
Inside the notebook or terminal, run:
pip install roboflow
pip install ultralytics
Make sure you're using an environment with GPU support (like Google Colab or a CUDA-compatible local setup).

4. Dataset Download via Roboflow
Replace the API key in the notebook with your own Roboflow API key:
from roboflow import Roboflow
rf = Roboflow(api_key="YOUR_API_KEY")
project = rf.workspace("training-data-kgqsn").project("pedestrian-detection-v6aln")
project.version(VERSION_NUMBER).download("yolov8")
All 15 dataset versions are merged automatically into a single training directory.

5. Train YOLO Models
The notebook will automatically train various models like:

YOLOv5n, YOLOv5s, YOLOv5m

YOLOv8n, YOLOv8s, YOLOv8m

YOLOv11n, YOLOv11s, YOLOv11m

Each trained model is saved under:

runs/detect/<model_name>
🧪 Results
✅ Outputs annotated image/video samples with bounding boxes

📈 Displays evaluation metrics: FPS, mAP, precision, and recall

🔁 Side-by-side visual and statistical comparisons across models

📝 Notes
The notebook has been compressed for GitHub upload.

If you find missing outputs or truncated cells, please re-run the notebook in Jupyter or Google Colab.

You can modify the training parameters (epochs, batch size, etc.) to fine-tune results.

📄 License
This project is released for educational and research purposes only. Feel free to fork and modify with proper attribution.
