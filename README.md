| Category   | DFANet | UNet  | DANet     | DABNet    | CE2P      | ParseNet  |      |      |      |      |      |      |
| ---------- | ------ | ----- | --------- | --------- | --------- | --------- | ---- | ---- | ---- | ---- | ---- | ---- |
| Background | 88.12  | 89.36 | **93.04** | 90.36     | 92.78     | 92.61     |      |      |      |      |      |      |
| Skin       | 89.69  | 91.90 | 93.15     | 91.27     | **93.17** | 93.05     |      |      |      |      |      |      |
| Nose       | 83.96  | 87.45 | 88.92     | 86.04     | 88.54     | 88.26     |      |      |      |      |      |      |
| EyeGlass   | 69.29  | 75.27 | 84.04     | 72.62     | 84.44     | **84.94** |      |      |      |      |      |      |
| LeftEye    | 69.19  | 77.62 | 80.65     | 73.69     | 81.95     | **82.39** |      |      |      |      |      |      |
| RightEye   | 69.12  | 78.05 | 80.84     | 74.38     | 82.03     | **82.51** |      |      |      |      |      |      |
| LeftBrow   | 66.04  | 72.53 | **75.63** | 69.78     | 75.55     | 75.43     |      |      |      |      |      |      |
| RightBrow  | 66.05  | 71.96 | **75.37** | 69.25     | 75.51     | 75.09     |      |      |      |      |      |      |
| LeftEar    | 66.52  | 75.08 | 78.93     | 72.28     | 78.35     | **78.96** |      |      |      |      |      |      |
| RightEar   | 65.85  | 74.20 | 78.29     | 70.83     | 77.82     | **78.65** |      |      |      |      |      |      |
| Mouth      | 70.23  | 81.98 | 85.45     | 78.41     | 85.65     | **86.02** |      |      |      |      |      |      |
| UpperLip   | 66.17  | 78.00 | 80.41     | 73.91     | 80.89     | **81.30** |      |      |      |      |      |      |
| LowerLip   | 70.26  | 80.97 | **83.52** | 78.37     | 83.57     | 83.38     |      |      |      |      |      |      |
| **Hair**   | 86.25  | 88.37 | **91.31** | 88.52     | 91.18     | 90.93     |      |      |      |      |      |      |
| Hat        | 61.02  | 56.07 | 75.87     | 63.56     | **76.13** | 74.40     |      |      |      |      |      |      |
| Earring    | 25.68  | 39.61 | 52.78     | 36.23     | 52.47     | **53.54** |      |      |      |      |      |      |
| Necklace   | 0.00   | 0.00  | 9.46      | 0.01      | 19.73     | **19.91** |      |      |      |      |      |      |
| Neck       | 76.38  | 79.39 | **83.55** | 78.74     | 83.53     | 83.28     |      |      |      |      |      |      |
| Cloth      | 60.21  | 62.82 | **78.07** | 67.27     | 76.30     | 76.01     |      |      |      |      |      |      |
| **mIOU**   | 65.79  | 71.61 | 77.33     | 70.36     | 77.87     | **77.93** |      |      |      |      |      |      |
| **Acc**    | 91.85  | 93.02 | **95.09** | 93.24     | 95.00     | 94.89     |      |      |      |      |      |      |
| **fps**    | 71.94  | 79.37 | 12.85     | **99.01** | 29.76     | 52.08     |      |      |      |      |      |      |



ParseNet设计思路：

1. **Hierarchical Global Attention Mechanism：**利用层级上下文信息对通道进行重新编码，显示地建模特征通道的依赖关系；
2. **Semantic Gap Compensation Block：** 不同层级特征图之间的语义信息差异过大，不能简单通过Add操作直接相加；可以利用孔洞卷积让他们的感受野在同一个量级上，减少语义差异的影响。同时，提取不同尺度上下文信息促进模型对不同大小物体的学习能力。
3. **Boundary Branch：** 
4. **Boundary Loss**

