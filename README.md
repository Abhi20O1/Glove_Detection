# Gloved vs. Ungloved Hand Detection

## Project Overview
This project is a computer vision-based system designed to detect gloves. It processes images and identifies two classes:
- 'gloved_hand'
- 'ungloved_hand'

The system is build using **Yolov8**, capable of real-time detection, and generates both annotation images and detailed JSON logs for auditing purposes.

---

## Dataset

* **Name:** Gloves - Object Detection
* **Source:** [Roboflow Universe](https://universe.roboflow.com/glove-uylxg/glove-q7czq/dataset/1)
* **Classes:** `gloved_hand`, `ungloved_hand`
* **Dataset Size:** 500 images
* **Split:** 70% Train, 20% Validation, 10% Test

---

## Model and Training
* **Model:** **YOLOv8n**.
* **Framework:** Ultralytics
* **Image Size:** 640x640
* **Epochs:** 20
* **Preprocessing:**
  * Auto-orientation
  * Resizing to 640px

---

## How to Run the Script

1.  **Setup Environment:**
    * Clone the repository.
    * Install the required packages:
        ```bash
        pip install -r requirements.txt
        ```

2.  **Prepare Files:**
    * Place the selected model weights, **`glove_model3/weights/best.pt`**, in the project's root directory.
    * Add your test `.jpg` images into a folder (e.g., `sample_images/`).

3.  **Execute Detection:**
    * Run the script from the command line inside the `Glove_Detection/` directory.
    * You must provide the path to your model and input images.

    **Example Command:**
    ```bash
    python detection_script.py --model_path glove_model3/weights/best.pt --input_dir sample_images/
    ```

4.  **Check Results:**
    * Annotated images will be saved in the `output/` folder.
    * JSON logs for each image will be saved in the `logs/` folder.
  
---

### Outputs

<table>
  <tr>
    <td align="center"><b>Original Image</b></td>
    <td align="center"><b>Annotated Image</b></td>
  </tr>
  <tr>
    <td><img src="Part_1_Glove_Detection/sample_images/S__34734373_jpg.rf.4c8486ba8572c6888ce2be85fd330ffa.jpg" width="100%"></td>
    <td><img src="Part_1_Glove_Detection/output/S__34734373_jpg.rf.4c8486ba8572c6888ce2be85fd330ffa.jpg" width="100%"></td>
  </tr>
</table>
