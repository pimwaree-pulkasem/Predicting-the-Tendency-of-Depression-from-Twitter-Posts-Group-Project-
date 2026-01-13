# Predicting Depression Tendency from Twitter Posts

โปรเจกต์นี้เป็นส่วนหนึ่งของงานด้าน Machine Learning และ Natural Language Processing (NLP)  
มีวัตถุประสงค์เพื่อทำนายแนวโน้มภาวะซึมเศร้าของผู้ใช้จากข้อความที่โพสต์บน Twitter

## Objective
พัฒนาโมเดล Machine Learning สำหรับจำแนกข้อความว่า  
ผู้โพสต์มีแนวโน้มเป็นโรคซึมเศร้าหรือไม่ โดยใช้ข้อมูลข้อความจากโซเชียลมีเดีย

## Dataset
- แหล่งที่มา: Kaggle (Mental Health Social Media Dataset)
- ขนาดข้อมูล: 20,000 ข้อความ
- จำนวนคลาส:
  - 0 = No Depression (10,000 ข้อความ)
  - 1 = Depression (10,000 ข้อความ)
- ข้อมูลมีความสมดุล และไม่มี missing data
- ใช้เฉพาะข้อมูลข้อความ (text) สำหรับการวิเคราะห์

## Methodology
1. Exploratory Data Analysis (EDA)
2. Text Preprocessing & Cleaning
   - แปลงคำย่อเป็นคำเต็ม
   - Lemmatization
   - ปรับ Part of Speech ให้สอดคล้องกับ WordNet
3. Feature Extraction / Vectorization
   - แปลงข้อความเป็นข้อมูลเชิงตัวเลข
4. Feature Selection
   - ANOVA
   - LASSO
5. Train-Test Split
6. Model Training & Evaluation

## Models Tested
- Logistic Regression
- LinearSVC
- Decision Tree
- Multinomial Naive Bayes
- XGBoost
- MLPClassifier (Multi-layer Perceptron)

## Model Selection
โมเดลที่เลือกใช้คือ **MLPClassifier**  
เนื่องจากให้ผลลัพธ์ที่เหมาะสมที่สุด โดยพิจารณาจาก:
- Accuracy อยู่ในระดับดี
- ไม่เกิด Overfitting
- ค่า Log Loss ต่ำ
- ความแตกต่างของ Accuracy ระหว่าง Train และ Test ต่ำ (ประมาณ 0.03)

## Result
โมเดลสามารถทำนายแนวโน้มภาวะซึมเศร้าจากข้อความได้อย่างมีประสิทธิภาพ  
เหมาะสำหรับใช้เป็นเครื่องมือคัดกรองสุขภาพจิตเบื้องต้น

## Benefits
- สนับสนุนการวิจัยด้านสุขภาพจิต
- ช่วยในการตรวจคัดกรองภาวะซึมเศร้าเบื้องต้น
- สามารถนำไปต่อยอดในการพัฒนาเครื่องมือช่วยเหลือทางจิตใจ
- ใช้ในการวิเคราะห์อารมณ์ของผู้ใช้จากโซเชียลมีเดีย

## Team Members
- วริยาพร
- ฐิติชญา
- พิมพ์วรีย์
- พัชรี

## Presentation
- Google Drive: https://drive.google.com/file/d/1nxnddFqV4rAfXOuRf62AKU-wL4S19yYn/view?usp=drive_link




