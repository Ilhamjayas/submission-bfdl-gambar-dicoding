# Proyek Klasifikasi Gambar — Animals-10

## Identitas
- **Nama**     : Ilham Jaya Saputra
- **Email**    : jayailham04@gmail.com
- **ID Dicoding** : Ilhamjayas

## Deskripsi Proyek
Proyek klasifikasi gambar hewan menggunakan dataset **Animals-10** dari Kaggle.
Model dibangun dengan arsitektur **Sequential** berbasis **MobileNetV2** (pretrained ImageNet)
ditambah custom Conv2D head untuk klasifikasi 10 kelas hewan.

## Dataset
- **Sumber**  : [Animals-10 (Kaggle)](https://www.kaggle.com/datasets/alessiocorrado99/animals10)
- **Total**   : ±26.000 gambar
- **Kelas**   : butterfly, cat, chicken, cow, dog, elephant, horse, sheep, spider, squirrel
- **Split**   : 70% Train / 15% Validation / 15% Test

## Arsitektur Model
- **Backbone** : MobileNetV2 (pretrained ImageNet, fine-tune 20 layer terakhir)
- **Head**     : Conv2D(64) → MaxPool → Conv2D(128) → MaxPool → GAP → Dense(256) → Dense(10)
- **Input**    : 224 × 224 × 3

## Hasil
| Set | Accuracy |
|-----|----------|
| Training   | ≥ 95% |
| Validation | ≥ 95% |
| Test       | ≥ 95% |

## Format Model Tersimpan
| Format | Lokasi | Kegunaan |
|--------|--------|----------|
| SavedModel | `saved_model/` | Deployment server/cloud |
| TF-Lite    | `tflite/model.tflite` | Mobile & embedded |
| TFJS       | `tfjs_model/` | Browser / JavaScript |

## Cara Menjalankan
```bash
pip install -r requirements.txt
jupyter notebook notebook.ipynb
```
