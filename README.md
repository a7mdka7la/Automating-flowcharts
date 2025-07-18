# Storyboard to Flowchart Generator

A simple web application that uploads PDF storyboards and automatically generates flowcharts using Groq AI.

## Features

- Upload PDF storyboard files
- Automatically extract text from PDFs
- Generate process steps using Groq AI
- Create flowchart descriptions
- Generate Mermaid code for flowcharts
- Open flowcharts directly in Draw.io

## Setup

1. Clone this repository:
```bash
git clone https://github.com/a7mdka7la/Automating-flowcharts.git
cd Automating-flowcharts
```

2. Install Python dependencies:
```bash
pip install -r requirements.txt
```

3. Set up environment variables:
   - Copy `.env.example` to `.env`
   - Add your Groq API key to the `.env` file:
   ```
   GROQ_API_KEY=your_actual_groq_api_key_here
   ```

4. Run the application:
```bash
pip install -r requirements.txt
```

2. Run the application:
```bash
python app.py
```

3. Open your browser and go to `http://localhost:5000`

## Usage

1. Click "Choose PDF Storyboard File" and select your PDF storyboard
2. Click "Generate Flowchart" 
3. Wait for the AI to process your storyboard (this may take a few moments)
4. View the generated steps, flowchart description, and Mermaid code
5. Click "Open Flowchart in Draw.io" to view the final flowchart

## How it works

1. Extracts text from the uploaded PDF storyboard
2. Sends the text to Groq AI with the prompt: "For the provided storyboard generate steps to follow"
3. Takes the generated steps and asks Groq AI: "Please create a flowchart representing the process, incorporating the above steps. Ensure that related steps are placed side by side."
4. Finally asks Groq AI: "Give me the mermaid code for this"
5. Opens the generated Mermaid code in Draw.io for visualization

## Requirements

- Python 3.7+
- Groq AI API key (get one from https://console.groq.com)
- Internet connection for API calls

## Note

Make sure to add your Groq API key to the `.env` file to use the live Groq AI integration.
