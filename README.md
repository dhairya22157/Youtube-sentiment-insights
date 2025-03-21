# YouTube Sentiment Insights

 Overview
YouTube Sentiment Insights is a **Chrome extension** and **Flask-based API** that analyzes YouTube comments to provide sentiment insights. It classifies comments into **positive, neutral, and negative** categories, helping users quickly understand audience reactions to a video. The project is deployed on **AWS** and uses **DVC** for managing data workflows.

 Features
- Fetches and analyzes YouTube comments using **YouTube API**.
- **Sentiment classification** using NLP models.
- Chrome extension for seamless integration.
- Backend powered by **Flask** and deployed on **AWS**.
- Uses **DVC** for data version control.
- **Insightful Visualizations**:
  - **Comment Analysis Summary**: Displays total comments, unique commenters, average comment length, and sentiment score.
  - **Sentiment Analysis Results**: Pie chart visualization of sentiment distribution (Positive, Neutral, Negative).
  - **Sentiment Trend Over Time**: Line chart showing sentiment trends over time.
  - **Comment Word Cloud**: Highlights frequently used words in comments.
  - **Top Comments with Sentiments**: Lists top comments with associated sentiment labels.

---

 Installation & Setup
# 1. Clone the Repository
```bash
git clone https://github.com/your-repo/youtube-sentiment-insights.git
cd youtube-sentiment-insights
```

# 2. Create and Activate Virtual Environment
```bash
conda create -n youtube python=3.11 -y
conda activate youtube
```

# 3. Install Dependencies
```bash
pip install -r requirements.txt
```

# 4. Initialize DVC
```bash
dvc init
dvc repro
dvc dag
```

# 5. Configure AWS (if deploying)
```bash
aws configure
```

# 6. Run the Application Locally
```bash
python app.py
```
By default, the server runs on `http://localhost:5000/`.

---

 Running the Project
# 1. Test API using Postman
You can send a **POST** request to the following endpoint to analyze sentiment:
```bash
http://localhost:5000/predict
```
 Example JSON Request:
```json
{
    "comments": ["This video is awesome! I loved it a lot", "Very bad explanation. Poor video"]
}
```
 Expected JSON Response:
```json
{
    "sentiments": ["positive", "negative"]
}
```

# 2. Load Chrome Extension
```bash
chrome://extensions/
```
1. Open `chrome://extensions/` in your browser.
2. Enable **Developer mode** (toggle at the top-right corner).
3. Click **Load unpacked** and select the `extension` folder from this project.
4. The extension will now be available in your browser.

---

 How to Get YouTube API Key
To fetch YouTube comments, you need an API key from **Google Cloud Platform (GCP)**. Follow this tutorial:
[How to get a YouTube API key](https://www.youtube.com/watch?v=i_FdiQMwKiw)

---

 Deployment
# Deploying to AWS
```bash
aws configure
```
1. Ensure AWS CLI is configured.
2. Deploy using a cloud service (EC2, Lambda, or Elastic Beanstalk).

---
Contributing
Pull requests are welcome! If you find any issues or improvements, feel free to open an issue or submit a PR.


