# FindMyFace
FindMyFace is a face recognition tool that scans thousands of images across folders, compares each face with a reference photo using InsightFace embeddings, and saves the matching images to a separate folder. Ideal for quickly isolating your own photos from large event collections.


# 👤 Face Recognition Filter with InsightFace

This project scans through a collection of images and extracts only those that contain a matching face with a given reference image. It uses [InsightFace](https://github.com/deepinsight/insightface) for face detection and feature extraction.

---

## ✅ Features

- Deep learning-based face detection with InsightFace
- Face embedding extraction
- Cosine similarity matching
- Recursive folder scanning
- Saves matching images to a separate folder
- GPU support (optional)


---

## 🔁 Processing Steps

1. Load the `buffalo_l` InsightFace model.
2. Extract face embedding from your reference image.
3. Recursively find all `.jpg`, `.jpeg`, `.png` images from given folders.
4. Compare each detected face in those images with your reference using cosine similarity.
5. Save matching images to `my_face_photos/`.

---

## ⚙️ Setup Instructions

### 📦 Requirements

```text
opencv-python
numpy
tqdm
insightface
```

## 🧪 Usage Notes

- Reference image should be clear and front-facing.
- Adjust `SIMILARITY_THRESHOLD` (e.g., 0.5–0.7) depending on match strictness.
- Set `ctx_id=0` to use GPU or `ctx_id=-1` to use CPU.

---

## 🎉 Output

All matched images will be copied to:

```
my_face_photos/
```

You can now review all images where your face was detected!

---

