# The Smartest AI Nutrition Assistant

## 📌 Problem Statement
In an era where health awareness is growing, individuals increasingly seek personalized nutrition guidance. 
However, most existing tools provide **generic diet plans**, lack **real-time adaptability**, and fail to consider:
- Holistic lifestyle factors  
- Cultural & religious food preferences  
- Allergies & medical conditions  
- Dynamic adaptation to evolving health goals  

Dieticians and nutritionists also face **scaling limitations**, making personalization hard to achieve.

### 🎯 The Challenge
Build **The Smartest AI Nutrition Assistant** using **Generative AI** that:
- Understands user input via **text, voice, or images** (food photos, grocery labels)  
- Generates **personalized meal plans** (health goals, conditions, routines, preferences)  
- Provides **contextual explanations** (e.g., “Why is this food better?”)  
- Learns & adapts dynamically from **continuous feedback**  

This AI bridges the gap between one-size-fits-all diet apps and **real nutrition counselling**.

---

## ⚙️ Technology Stack (IBM Cloud Lite + Granite)
- **IBM watsonx.ai Granite** → Generative AI for reasoning & meal plan generation  
- **IBM Cloud App ID (Lite)** → Authentication  
- **IBM Cloud Object Storage (Lite)** → Storing images, food labels, PDFs  
- **IBM Cloudant (Lite)** → JSON DB for user profiles, preferences, logs  
- **IBM Code Engine (Lite)** → For OCR, food label parsing, ETL jobs  
- **FastAPI / Flask API Gateway** → Backend layer  
- **React Frontend** → Chat & planner UI (multimodal input support)  

---

## 📂 Repository Structure
```
Nutrition-Agent/
│── Nutrition Agent.ipynb   # Jupyter Notebook with prototype code
│── README.md               # Project documentation
│── requirements.txt        # Python dependencies (to be added)
│── /data                   # Food database, sample logs (optional)
```

---

## 🚀 Features Implemented in Notebook
- Data preprocessing for food & nutrition datasets  
- Basic integration with food APIs (e.g., USDA FoodData Central)  
- User profiling & JSON schema design (for Cloudant)  
- Prototype meal plan generation using **Granite LLM on watsonx.ai**  
- Example conversational flow (User ↔ Assistant)  

---

## 🛠️ Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Nutrition-Agent.git
   cd Nutrition-Agent
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Linux/Mac
   venv\Scripts\activate    # On Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the Jupyter notebook:
   ```bash
   jupyter notebook "Nutrition Agent.ipynb"
   ```

5. (Optional) Deploy backend API using **IBM Code Engine**.

---

## 📊 Example Use Case
**Input:**  
> I am a vegetarian, want to lose 5kg in 3 months. I don’t eat onion or garlic. Suggest a 1600 kcal plan.  

**Output (AI Generated):**  
- Breakfast: Vegetable upma with sprouts (350 kcal, 15g protein)  
- Lunch: Brown rice with dal, sautéed beans (550 kcal, 20g protein)  
- Snack: Roasted makhana + buttermilk (150 kcal, 6g protein)  
- Dinner: Paneer curry (no onion/garlic) + chapati + salad (500 kcal, 25g protein)  

Explanation: “Paneer provides high-quality protein. Whole grains keep you full. Garlic/onion excluded as per preference.”

---

## 📌 Future Improvements
- Full multimodal support (voice input + food photo recognition)  
- Continuous learning from wearable/sensor data  
- Export diet plans in **PDF/CSV** for doctors/nutritionists  
- Integration with **fitness trackers** & **blood sugar monitors**  

---

## ⚠️ Disclaimer
This project is for **educational and wellness purposes** only.  
It does **NOT replace professional medical advice**. Please consult a doctor/dietician for clinical guidance.
