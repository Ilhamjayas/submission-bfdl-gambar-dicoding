# Proyek Klasifikasi Gambar — Animals-10

Run ID: 20261015T130914Z_2dcf3d3c
Epoch selesai: 8
Train accuracy: 0.984939
Test accuracy: 0.962821

Arsitektur: Sequential, MobileNetV2 + Conv2D/Pooling head.
Split: 70% training, 15% validation, 15% testing.
Input: RGB 224x224, float32 / 255.0. Label: tflite/label.txt.
TFJS merupakan GraphModel (gunakan tf.loadGraphModel).
