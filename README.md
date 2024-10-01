# femur-3D-segmentation 
3D segmentation of femur from CT using nnUNet

## Project Overview:
This project addresses the 3D segmentation of the femur from CT scans. Due to issues with TotalSegmentator cropping the femoral head, manual labeling of 29 datasets was conducted to improve segmentation accuracy using the nnUNet model.

## Objective:
- Perform femur segmentation from CT scans using **nnUNet** with manually corrected 29 masks.
- Mitigate issues related to the femoral head cropping, improving segmentation accuracy. (TotalSegmentator)

## Dataset:

### Data Overview
| Feature               | Description                                     |
|-----------------------|-------------------------------------------------|
| **Resolution**         | `512x512` pixels, `Z slices` (Approx. 50 slices per scan) |
| **Manual Labels**      | 29 manually labeled datasets                   |

- **Fold Configuration**:
  - 5-Fold Split:
    - **23** for Training 
    - **6** for Validation

## Workflow:
1. **Data Preparation**:
   - 29 CT scans of the femur were manually labeled for segmentation.
   - The dataset was split into **5 folds**, with **23 scans used for training** and **6 scans for validation** in each fold.

2. **Model Training**:
   - The **nnUNet** architecture was employed to train on the manually labeled data.
   - A 5-fold cross-validation approach was used to assess model performance.

3. **Results**:
   - The training process leveraged the newly labeled masks for more accurate segmentation outcomes.
   - Future steps involve the refinement of the model based on validation feedback and the integration of the segmentation masks into downstream tasks and further analysis.

## Improved Mask Comparison

Here is a comparison between the original mask and the improved mask:

**Original Mask:**

![Original Mask](https://github.com/user-attachments/assets/6d438db9-db4c-434c-9cb7-91deaa1232df)

**Improved Mask:**

![Improved Mask](https://github.com/user-attachments/assets/a25b6100-fbee-42d4-a519-afb0086e8434)

## Future Research Directions:
This project aims to support **downstream research** related to the femur by providing high-quality segmentation masks.


