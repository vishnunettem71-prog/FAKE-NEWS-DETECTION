AI Fake News Detection Using NLP

An interactive web-based **Fake News Detection System** that analyzes news text and identifies whether it is **Likely Reliable, Suspicious, or Likely Fake News**.

The project combines **Natural Language Processing (NLP) concepts, keyword-based text analysis, Speech-to-Text, and Text-to-Speech** to provide an easy-to-use fake news analysis interface.

🚀 Features

* 📝 Enter news articles manually.
* 🎤 Convert speech into text using Speech-to-Text.
* 🔍 Analyze news content using text-based NLP rules.
* 🚨 Detect suspicious or fake-news indicators.
* 📊 Calculate a Fake News Probability Score.
* ⚠️ Display risk level:

  * LOW – Likely Reliable
  * MEDIUM – Suspicious / Verify
  * HIGH – Likely Fake News
* 📈 Display suspicion score with a progress bar.
* 🔎 Show detected suspicious signals.
* 🧠 Provide an explanation of the analysis.
* 🔊 Read the analysis result using Text-to-Speech.
* 🗑️ Clear the input and analysis results.
* 📱 Responsive design for smaller screens.

🛠️ Technologies Used

* HTML5 – Web page structure
* CSS3 – Styling and responsive design
* JavaScript – Application logic and analysis
* NLP Concepts – Text pattern and keyword analysis
* Web Speech API – Speech-to-Text and Text-to-Speech
* VS Code – Development environment
* Google Chrome – Recommended browser

The interface contains buttons for speaking news, analyzing the text, reading the result, and clearing the input.

🧠 How It Works

The system follows these steps:

text
User enters news
       ↓
Speech-to-Text (Optional)
       ↓
Text Preprocessing
       ↓
Keyword & Pattern Analysis
       ↓
Suspicious Signal Detection
       ↓
Fake News Score Calculation
       ↓
Classification
       ↓
Result + Explanation
       ↓
Text-to-Speech (Optional)

🔍 Detection Method

The application uses predefined textual patterns to calculate a suspicion score.

1. Explicit Fake News Indicators

The system checks for phrases such as:

* `fake news`
* `false information`
* `misinformation`
* `disinformation`
* `fabricated story`
* `false claim`
* `unverified claim`

2. Lack of Evidence

It checks for phrases indicating insufficient evidence, such as:

* `no reliable scientific evidence`
* `no evidence`
* `unsupported claim`
* `not supported by scientific evidence`

3. Lack of Official Sources

The system looks for indicators such as:

* `no official announcement`
* `no reliable source`
* `not officially announced`
* `not confirmed by scientists`

4. Extraordinary Claims

It identifies unusual claims such as:

* `live for more than 200 years`
* `stop aging`
* `live forever`
* `make humans immortal`
* `cure every disease`

5. Social Media Indicators

The system detects patterns such as:

* `viral on social media`
* `widely shared on social media`
* `shared without checking`
* `spread rapidly online`

### 6. Sensational Language

Words such as:

* `shocking`
* `unbelievable`
* `miracle`
* `amazing`
* `incredible`
* `secret`
* `revolutionary`
* `breaking`

are considered possible suspicious signals.

The JavaScript implementation contains separate rule groups for explicit fake-news phrases, missing evidence, missing sources, extraordinary claims, social-media sharing, source verification, sensational language, and absolute claims.

## 📊 Classification

The final score is limited to a range of 5%–98%.

  Score       Classification           Risk   

 70% – 98%   🚨 Likely Fake News      HIGH   
 40% – 69%   ⚠️ Suspicious / Verify   MEDIUM 
 5% – 39%    ✅ Likely Reliable        LOW    

These thresholds and classifications are implemented directly in the program.

Important:The system provides a pattern-based prediction. A "Likely Reliable" result does not prove that the news is actually true. News should always be verified using trustworthy and independent sources.

🎤 Speech-to-Text

The project uses the browser's **Web Speech API** to convert spoken news into text.

The application uses:

javascript
window.SpeechRecognition ||
window.webkitSpeechRecognition

and sets the recognition language to:
text
en-IN

Google Chrome is recommended because browser support for Speech Recognition can vary.

🔊 Text-to-Speech

After analysis, the system can read the prediction and fake-news probability aloud using the browser's Speech Synthesis API.

Example:

text
LIKELY FAKE NEWS.
Fake news probability is 85%.

The project uses `SpeechSynthesisUtterance` for this functionality.

🖥️ User Interface

The application provides:

* News input text area
* Speak News button
* Analyze News button
* Read Result button
* Clear button
* Prediction display
* Word count
* Risk level
* Suspicion score
* Fake probability
* Progress bar
* Analysis explanation
* Detected signals

These result components are defined in the HTML interface.

📂 Project Structure

text
AI-Fake-News-Detection/
│
├── index.html
└── README.md

Since the current project contains the HTML, CSS, and JavaScript together in one file, **no separate backend or database is required.

▶️ How to Run

Step 1: Download or Clone the Repository bash
git clone https://github.com/vishnunettem71-prog/AI-Fake-News-Detection.git

Step 2: Open the Project

Open the project folder in **VS Code**.

Step 3: Open `index.html`

You can either:

* Open `index.html` directly in a browser, or
* Use the **Live Server** extension in VS Code.

Step 4: Test the Application

Enter a news story into the text box.

For example:
text
A scientist claims to have invented a device that can make humans live for more than 200 years. There is no reliable scientific evidence supporting the claim.

Click:
text
🔍 Analyze News

The system will calculate the score and display the classification.

🧪 Example Output

text
🚨 LIKELY FAKE NEWS

Word Count: 28
Risk Level: HIGH
Suspicion Score: 80%
Fake Probability: 80%

Detected Signals:
• Extraordinary scientific claim detected
• Reliable scientific evidence is missing
• Suspicious claim detected

🎯 Project Objectives

1. To develop a simple fake-news detection web application.
2. To apply basic NLP concepts to news text.
3. To identify suspicious linguistic patterns.
4. To calculate a fake-news probability score.
5. To provide understandable explanations for predictions.
6. To integrate Speech-to-Text functionality.
7. To integrate Text-to-Speech functionality.
8. To create an interactive and responsive user interface.

🌟 Advantages

* Easy to use
* No installation of Python libraries required
* No database required
* Works directly in a web browser
* Supports voice input
* Supports voice output
* Provides an understandable explanation
* Suitable for educational NLP projects
* Can be easily modified and extended

⚠️ Limitations

This project is an **educational NLP project** and does not use a trained machine-learning model or live fact-checking database.

The detection is based mainly on predefined keywords and linguistic patterns. Therefore:

* It cannot verify news against real-time sources.
* It may produce false positives.
* It may produce false negatives.
* It cannot guarantee that a news article is factually true.
* Browser support for Speech Recognition may vary.

🔮 Future Enhancements

The project can be improved by adding:

* 🤖 Machine Learning-based fake news classification
* 🧠 Deep Learning models
* 📚 A real fake-news dataset
* 🔎 Real-time fact-checking
* 🌐 News API integration
* 🔗 Source credibility checking
* 📊 Visualization of NLP results
* 🌍 Multiple language support
* 🗄️ Database for storing analyzed articles
* 👤 User login and history
* 📈 Accuracy, precision, recall, and F1-score evaluation

📚 NLP Concepts Used

This project demonstrates basic concepts including:

* Text preprocessing
* Tokenization
* Keyword detection
* Pattern matching
* Sentiment/sensational language indicators
* Rule-based classification
* Feature scoring
* Risk classification

👨‍💻 Project Type

Mini Project / Academic Project

Domain: Artificial Intelligence & Natural Language Processing

Project: AI Fake News Detection

Input: Text or Speech

Output: Fake News Probability, Risk Level, Explanation, and Detected Signals

📄 License

This project is created for **educational purposes**. You are free to modify and improve the project for learning and academic use.

⭐ If You Like This Project

If you find this project useful, consider giving the repository a ⭐ on GitHub.

📌 Disclaimer

This application is designed for educational purposes and should not be treated as an authoritative fact-checking system. Always verify important news through reliable and independent sources.
