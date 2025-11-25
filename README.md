**🔧 AI Defect Advisor**

An interactive Python-based tool powered by OpenAI GPT models to analyze manufacturing, industrial, or material defects and recommend actions with confidence scoring.
This project enables operators, QA engineers, and technicians to quickly understand potential causes of defects such as cracks, corrosion, dents, discoloration, holes, bloating, and more — simply by describing the defect.

**🚀 Features**

AI-driven defect analysis using OpenAI GPT (supports gpt-4o-mini, etc.).
Structured JSON output containing:
likely_cause
recommended_action
confidence (0–1)
Interactive CLI mode
Automatic cleanup of Markdown/JSON fences
Lightweight, easy to extend

**🧠 How It Works**
You provide a defect description (e.g., crack, corrosion, black hole, bloating).
The model processes it using a system prompt and returns a structured JSON:
{
  "likely_cause": "Thermal stress during cooling or improper alloy composition.",
  "recommended_action": "Evaluate the cooling process and material specifications.",
  "confidence": 0.85
}


**This makes it suitable for:**
Manufacturing plants
Material science workflows
Defect triage tools
Automated QA assistants
Smart inspection systems

**📦 Installation**
1. Clone the repository
git clone https://github.com/your-username/ai-defect-advisor.git
cd ai-defect-advisor

2. Create a virtual environment (optional)
python3 -m venv venv
source venv/bin/activate

3. Install dependencies
pip install openai

**🔑 Setup Your API Key**
Set your OpenAI API key in your environment:
export OPENAI_API_KEY="your-openai-api-key"


Or replace it directly in the script (not recommended for production):
os.environ["OPENAI_API_KEY"] = "your-openai-api-key"

**▶️ Run the Application**
Start the interactive CLI:
python defect_advisor.py
You'll see:
🔧 Welcome to the AI Defect Advisor!
Type 'exit' to quit.
Example interaction:
Enter a defect type: green crack
Output:
{
  "likely_cause": "Thermal stress during cooling or improper alloy composition.",
  "recommended_action": "Evaluate the cooling process and material specifications.",
  "confidence": 0.85
}

**🧩 Code Overview**
analyze_defect(defect_type: str)
Sends the defect description to GPT
Uses a system prompt that enforces structured JSON
Cleans code fences & parses JSON safely
Returns the model's response as a Python dictionary

**Main Loop**
Provides an interactive CLI for entering defect types, with an exit command.

**📘 Example Defects & Responses**
Input Defect	Example Output
crack	Cause: thermal stress → Action: inspect cooling system
corrosion	Cause: moisture/chemical exposure → Apply protective coating
black hole	Material failure + discoloration → Structural inspection
bloated	Moisture expansion → Remove & seal
rotten	Fungal growth → Replace & improve ventilation

**🛠️ Folder Structure**
ai-defect-advisor/
│
├── defect_advisor.py     # Main script
├── README.md             # Documentation
└── requirements.txt      # (optional)

**🤖 Model Configuration**

Current model:
model="gpt-4o-mini"
temperature=0.2


You can upgrade anytime to models like:
gpt-4.1
gpt-4o
gpt-4.1-mini

**🧩 Future Enhancements (Optional Ideas)**
Add a FastAPI/Flask backend API
Build a web dashboard for defect entry
Integrate image-based defect detection
Add history tracking or logging
Create confidence-based automation workflows


**🙌 Contributions**
Pull requests are welcome!
If you have ideas for new defect categories or better analysis patterns, feel free to contribute.
