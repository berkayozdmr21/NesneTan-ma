🎯 YOLOv8 Nesne Tanıma (Colab)

Bu proje, YOLOv8 kullanılarak hem fotoğraflardan hem de videolardan nesne tespiti yapmayı sağlar.
Proje, Google Colab üzerinde kolayca çalıştırılabilir.

🔍 Özellikler

📸 Fotoğraflardan nesne tespiti

🎥 Videolardan nesne tespiti

⚡ Gerçek zamanlı kamera desteği (Colab destekliyorsa)

🎯 Yüksek doğruluk & hızlı tahmin

🚀 Kurulum (Colab)

Google Colab aç.

Gerekli kütüphaneleri yükle:

!pip install ultralytics opencv-python


YOLOv8 modelini indir:

from ultralytics import YOLO
model = YOLO("yolov8n.pt")  # küçük model


Fotoğraf üzerinde tahmin:

results = model("resim.jpg")
results.show()


Video üzerinde tahmin:

results = model("video.mp4")
results.save("output/")




📸 Kullanım Örnekleri
Fotoğraf
!yolo detect predict model=yolov8n.pt source='resim.jpg'

Video
!yolo detect predict model=yolov8n.pt source='video.mp4'

Webcam (Colab destekliyorsa)
!yolo detect predict model=yolov8n.pt source=0

🖼️ Çıktılar

Tespit edilen nesneler dikdörtgen kutularla işaretlenir.

Nesne adı ve güven skoru gösterilir.

<img width="1244" height="639" alt="Ekran görüntüsü 2025-08-24 174855" src="https://github.com/user-attachments/assets/cbee13fa-f2c3-489f-94eb-71a968f1b0e1" />


👨‍💻 Geliştirici

Berkay Özdemir
