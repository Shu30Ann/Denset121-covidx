# Datasets

This project uses chest X-ray datasets from Kaggle:

1. [Chest X-Ray Pneumonia](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)  
2. [COVID-19 Radiography Database](https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database)  
3. [COVID-QU Dataset](https://www.kaggle.com/datasets/anasmohammedtahir/covidqu) *(COVID images only)*  

---

## Dataset Combination and Balancing

To create a balanced dataset for **three classes (Pneumonia, COVID, Normal)**, images from the above sources were combined as follows:

- **Pneumonia**: collected from **Dataset 1** and **Dataset 2**  
- **COVID-19**: merged from **Dataset 2** and **Dataset 3**  
- **Normal**: collected from **Dataset 1** and **Dataset 2**  

After merging, the final dataset was balanced across classes with the following distribution:

| Class      | Number of Images |
|------------|------------------|
| Pneumonia  | 15,903           |
| COVID-19   | 15,565           |
| Normal     | 13,358           |

This ensures that no class heavily outweighs the others, improving model training stability and evaluation fairness.
