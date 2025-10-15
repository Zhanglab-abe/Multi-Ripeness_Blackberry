# 🌾 [Sensing and Automation in Agri-System (SAAS) Lab](https://sites.google.com/view/xin-zhang-lab/home)

🏛️ [**School of Environmental, Civil, Agricultural & Mechanical Engineering**](https://engineering.uga.edu/schools/ecam/), [**University of Georgia**](https://www.uga.edu/)  


---

# ❓ Why do we create this repo?

This repository accompanies the publication:

**IN-FIELD MULTI-RIPENESS BLACKBERRY DETECTION FOR SOFT ROBOTIC HARVESTING**  
Published in *Journal of the American Society of Agricultural and Biological Engineers* (2025)  
📄 [ASABE Link]()


---


# 📄 Abstract
Blackberry harvesting is a crucial step for the fresh market production, requiring multiple passes of hand-picking because the berries do not ripen simultaneously, even on a plant, during the harvesting season. The blackberry harvesting process encounters several major hurdles in the U.S., including the shortage of agricultural labor and postharvest fruit quality since the blackberries are highly delicate and sensitive. Developing a computer vision-enabled robotic system for selectively picking blackberries can mitigate issues and secure the profitability of fresh blackberry growers. In-field blackberry detection and localization are extremely challenging attributing to several driving-factors, such as small size of the target berries, multiple levels of berry ripeness, and
great variation of outdoor lighting conditions. This study aims to assess and compare the feasibility, accuracy, and efficiency of a series of stateof-the-art YOLO (You Only Look Once) models in detecting multi-ripeness blackberries in the farm conditions. A total of 1,086 images containing three different ripeness levels of blackberries were observed during the two-year harvesting season, including ripe berries (in black color), berries in the ripening stage (in pink color), and unripe berries (in green color). The computer vision pipeline developed in this study had the ability to detect and localize all berries at different ripeness levels, while detecting
the ripe berries only was a particular focus. Overall, nine YOLO models (i.e., YOLOv5-x6, YOLOv6-l6, YOLOv7-base, YOLOv7-x, YOLOv7-e6e,
YOLOv8-n, YOLOv8-x, YOLOv12-n, and YOLOv12-x were trained and validated using randomly partitioned 760 (70%) and 108 images (10%),
respectively. Among these models, YOLOv7-base outperformed the others in balancing mean Average Precision (mAP) and frames-persecond (FPS) on the test set, which comprised 218 images (20%). More specifically, YOLOv7-base achieved the mAP of 91.1%, F1-score of
84.9%, and inference speed of 12.6 ms per image with 1,024 × 1,024 pixels across all classes of ripeness. In addition, its mAP on the ripe
berries was 92.4%, making YOLOv7-base a reliable tool for near realtime, in-field blackberry detection for soft robotic selective harvesting. The full imagery dataset, annotated labels, and trained weights of all YOLO models in this study are published to the community in the GitHub repository via [GitHub](https://github.com/Zhanglab-abe/Multi-Ripeness_Blackberry).

---

# 📂 How to use this repo?

### 🗂️ Repository Overview


This repository provides the complete dataset and best-trained YOLO weights generated from five randomized datasets derived from the full dataset for multi-ripeness blackberry detection.
The following links correspond to the trained weights used for model evaluation.

⚠️ If you use any of the provided models or datasets, please cite the references listed at the end of this README.

[YOLOv5-x6](https://outlookuga-my.sharepoint.com/:f:/g/personal/tt43037_uga_edu/EtdTl6EyoWJFmwwlmpuUWfwB1M6lfk8nf-I1RheOhFxWaQ?e=JKf9Wp) 
[YOLOv6-l6](https://outlookuga-my.sharepoint.com/:f:/g/personal/tt43037_uga_edu/EtilEj60j-tDlyEKhdLkDxIBwaRsCFtC0cjBHnIq2dgYCQ?e=fyJXom) 
[YOLOv7-base](https://outlookuga-my.sharepoint.com/:f:/g/personal/tt43037_uga_edu/EjZlpUI2JpRPlFnJNE6wbeQBZPGDGz8Na84vf1OsGjx-JA?e=ZWozh1) 
[YOLOv7-x](https://outlookuga-my.sharepoint.com/:f:/g/personal/tt43037_uga_edu/Ei7_njuWSYtJvdFOaRMBRtcBlOSh7tVsYm4AUG7VWHidtQ?e=TlXyz4) 
[YOLOv7-e6e](https://outlookuga-my.sharepoint.com/:f:/g/personal/tt43037_uga_edu/EtY1qfZhUypFjgHHGoiuQccBcQdsRWEi1KnKxgW6GD883A?e=BPHS2y)
[YOLOv8-n](https://outlookuga-my.sharepoint.com/:f:/g/personal/tt43037_uga_edu/EitSVXs7dC9LmMfPaurqVisBTiYKefDyve407stagPQCDA?e=bTi3v7) 
[YOLOv8-x](https://outlookuga-my.sharepoint.com/:f:/g/personal/tt43037_uga_edu/Eq-N72vxWDNCkDFOxkacLIcBqwBbvOzsiNk9YkK_qGobgg?e=U6bwqR) 
[YOLOv12-n](https://outlookuga-my.sharepoint.com/:f:/g/personal/tt43037_uga_edu/Eqb4zzXuIqJFn5JARKxb9ZsBvjdAuafAmY70vrP8aMsf3A?e=ESIvEy)
[YOLOv12-x](https://outlookuga-my.sharepoint.com/:f:/g/personal/tt43037_uga_edu/Es6sxlQJWAJIiWeu1VxSqhQBZXgyaalSk1O31t3XHHxZLg?e=FOQqOa)

## 🚀 Getting Started

### 🛠️ Installation
Please visit the corresponding YOLO repositories to learn how to install the dependencies and packages in your Conda environment before training:

[YOLOv5](https://github.com/ultralytics/yolov5) <br>
[YOLOv6](https://github.com/meituan/YOLOv6) <br>
[YOLOv7](https://github.com/WongKinYiu/yolov7) <br>
[YOLOv8](https://github.com/ultralytics/ultralytics) <br> 
[YOLOv12](https://github.com/sunsmarterjie/yolov12) <br>


For training and validation, use the model-specific approaches described in the above repositories.  
The following default hyperparameters were used to generate the reported results:  

---

### 🧠 Training

| Parameter              | Value  |
|:------------------------|:-------|
| Image size             | 1024   |
| Weights                | Corresponding pre-trained weight |
| Data                   | Use `data/main_1.yaml` for all models except YOLOv6; use `data/mainV6.yaml` for YOLOv6 |
| Epochs                 | 300    |
| Batch size             | 8      |
| Initial learning rate  | 0.01   |
| Learning rate factor   | 0.01   |
| Box                    | 7.5    |

---

### ✅ Validation

| Parameter              | Value  |
|:------------------------|:-------|
| Image size             | 1024   |
| Weights                | Trained weights |
| Batch size             | 8      |
| Task                   | test   |
| Data                   | Use `data/main_1.yaml` for all models except YOLOv6; use `data/mainV6.yaml` for YOLOv6 |
| Box                    | 7.5    |



# 📖 How to properly cite us if you find this repo useful?
*To cite this repo in your works, use the following BibTeX entry:*

```bibtex

```
