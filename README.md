![Untitled Diagram drawio](https://github.com/user-attachments/assets/ecc58d72-3c2d-432c-a172-34b127cb2f51)

# AI Electronics Sales Agent

An advanced AI-powered cold calling sales agent designed specifically for electronics sales. This application combines real-time voice interaction with customer data analysis to create personalized sales conversations. Built with Streamlit, it leverages speech-to-text, text-to-speech, and large language model capabilities to conduct natural sales conversations and track customer interactions.


## Features

- Automated cold calling for electronics sales
- Intelligent sales conversation management
- Customer purchase history tracking and analysis
- Personalized product recommendations
- Real-time voice interaction with AI
- Speech-to-text conversion using Deepgram
- Natural language processing using GPT models
- Text-to-speech synthesis with natural voice
- Live conversation display in Streamlit interface
- Support for custom sales functions and API integrations
- MongoDB integration for customer relationship management
- Detailed conversation history tracking
- Real-time audio streaming
- Sales performance analytics

## Demo Video
https://github.com/user-attachments/assets/13cf1a22-b8d3-4165-aa95-55834e6f105f

## Prerequisites

- Python 3.7+
- PyAudio
- Streamlit
- MongoDB instance

## Required API Keys

The following API keys need to be set as environment variables:

```bash
DEEPGRAM_API_KEY= 
OPENAI_API_KEY=
GEMINI_API_KEY=
```

## Installation

1. Clone the repository
2. Install the required packages:

```bash
pip install -r requirements.txt
```

## Configuration

The application uses several configuration settings that can be modified:

- Voice Agent URL: `wss://agent.deepgram.com/agent`
- Voice Model: "aura-luna-en"
- STT Model: "nova-2"
- LLM Model: "gpt-4o-mini"
- Audio Settings:
  - Sample Rate: 16000 Hz
  - Encoding: linear16
  - Chunk Size: 0.05 seconds

## Usage

1. Set up your customer database in MongoDB with electronics product catalog and customer information

2. Start the application:
```bash
streamlit run 1_Welcome.py
```
3. You will see two options : Customer ID :(Enter 9999 for testing, or insert a valid Customer entry in the database and enter their Customer ID)
4. Promt : You can enter the desired prompt for the LLM voice agent. Leaving it empty would default to the hard-coded prompt.
5. After entering the Customer ID and prompt(optional), click the VoiceAgent tab to chat with the agent.
6. You can also see and add entries in the MongoDB database.

### Sales Features

- Automatic customer profile loading
- Previous purchase history integration
- Product recommendation engine
- Customizable sales scripts and responses
- Real-time sales performance tracking
- Call outcome recording and analysis
- Follow-up scheduling automation

## Troubleshooting

- If experiencing audio issues, restart your computer, especially if you typically close your laptop instead of shutting down
- Use Postman to test API keys and endpoints
- Check if PortAudio is properly initialized
- Ensure all required environment variables are set
- Verify microphone permissions are granted to the application



## Error Handling

The application includes robust error handling for:
- WebSocket connections
- Audio stream management
- API calls
- Database operations
- Function execution





## Directory Structure


├── chroma.db
│   ├── chroma.cache
│   ├── 125ea723-8903-4ccd-905b-3ef652a4d5d1
│   ├── 3545ad7d-0c62-429a-8aed-80d6442a1b2e
│   ├── cbde1796-d7f9-4006-81ea-6b56acace068
│   └── chroma.sqlite3
├── env_name
│   └── Scripts
├── pyvenv.cfg
├── images
│   └── git_workflow.png
├── pages
│   ├── 2_VoiceAgent.py
│   ├── 3_MongoDB_Dashboard.py
│   └── 4_Data_Entry.py
├── templates
│   └── streams.xml
├── .gitignore
├── 1_Welcome.py
├── azure_test_code.py
├── BRANCH_AND_RELEASE_PROCESS.md
├── chromadb_agent.py
├── CODE_CONTRIBUTIONS_GUIDE.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── customer_id.txt
├── functions.py
├── GITHUB_WORKFLOW.md
├── LICENSE
├── model.py
├── mongo_forms_scheduler.py
├── mongodb.py
├── prompt.py
├── README.md
├── requirements.txt
├── sync_chroma_with_mongo.py
└── tempCodeRunnerFile.py


