# X-ModalProof-Supplementary-Code-Figures
This archive contains all code, data, and instructions required to reproduce the main figures, tables, and experimental claims in the paper

# X-ModalProof Supplementary Code & Figures

This archive contains all code, data, and instructions required to reproduce the main figures, tables, and experimental claims in the paper:

**"X-ModalProof: Real-Time Explainable Ownership Verification for Multimodal and Edge-Deployed AI Models"**  
_Mohammad Othman Nassar, Feras Fares AL-Mashagba_

---

## **Contents**

README.md
requirements.txt
generate_xmodalproof_figures.py
simulate_attacks.py
onnx_export_and_latency.py
generate_trigger_masks.py
generate_trigger_datasets.py
text_trigger_set.json # Sample text triggers
image_trigger_set.json # Sample image trigger file list


---

## **Figure/Table Reproducibility Mapping**

| Manuscript Figure/Table | Script/Section                     | Output File(s)                           |
|------------------------|------------------------------------|------------------------------------------|
| Fig. 1 (Flowchart)     | `generate_xmodalproof_figures.py`  | xmodalproof_figures/fig1_flowchart.png   |
| Fig. 2 (Accuracy)      | `generate_xmodalproof_figures.py`  | xmodalproof_figures/fig2_accuracy.png    |
| Fig. 3 (Robustness)    | `generate_xmodalproof_figures.py`  | xmodalproof_figures/fig3_robustness.png  |
| Fig. 4 (Attribution)   | `generate_xmodalproof_figures.py`  | xmodalproof_figures/fig4_alignment.png   |
| Fig. 5 (SHAP)          | `generate_xmodalproof_figures.py`  | xmodalproof_figures/fig5_shap_realistic.png |
| Fig. 6 (Grad-CAM)      | `generate_xmodalproof_figures.py`  | xmodalproof_figures/fig6_gradcam_realistic.png |
| Fig. 7 (Latency)       | `generate_xmodalproof_figures.py`  | xmodalproof_figures/fig7_latency.png     |
| Fig. 8 (Radar Chart)   | `generate_xmodalproof_figures.py`  | xmodalproof_figures/fig8_radar.png       |

---

## **How to Use**

### **1. Install requirements**
```bash
pip install -r requirements.txt


python generate_xmodalproof_figures.py

2. Generate all main figures
bash
Copy
Edit
python generate_xmodalproof_figures.py
This will create all figures in xmodalproof_figures/ and archive them as XModalProof_All_Figures.zip.

3. Model attack simulation
bash
Copy
Edit
python simulate_attacks.py
Contains template code for pruning, fine-tuning, and distillation attacks.

Adapt to your specific model and dataloader as needed.

4. ONNX export & latency evaluation
bash
Copy
Edit
python onnx_export_and_latency.py
Exports PyTorch models to ONNX and measures inference latency using ONNXRuntime.

Adapt sample input/model as needed.

5. Generate trigger masks (for attribution alignment)
bash
Copy
Edit
python generate_trigger_masks.py
Generates and saves a sample mask (e.g., for image triggers).

6. Generate sample trigger datasets
bash
Copy
Edit
python generate_trigger_datasets.py
Outputs text_trigger_set.json and image_trigger_set.json.

Notes
Reproducibility:
All values and results in the code match the corresponding tables and figures in the submitted manuscript.
Figures and tables are regenerated using hardcoded or sample values for reviewer validation.

ONNX/Edge Latency:
For true device results, run ONNX script on Jetson Nano, Raspberry Pi, or other edge device.

Mask & Trigger Examples:
Adapt scripts for your specific trigger/mask logic if needed for your own data or to check attribution alignment.

Contact
For any clarification, please contact:

Dr. Mohammad Othman Nassar
moanassar@aau.edu.jo




