# QuizWhiz

**Transform your lecture transcripts into interactive quizzes powered by AI!**

QuizWhiz is an intelligent quiz generation platform that converts your lecture transcripts into engaging multiple-choice questions. Upload your text files and let AI create personalized quizzes to test your understanding of the material.

## ✨ Features

- **Smart Question Generation**: AI-powered question creation from your lecture transcripts
- **Intelligent Answer Options**: Generates realistic distractors using advanced NLP models
- **Beautiful Dark Theme UI**: Modern Material-UI interface with purple and gold color scheme
- **Real-time Processing**: Fast question generation with loading indicators
- **Simple File Upload**: Just drag and drop your .txt files
- **Answer Verification**: Uses multiple AI models to ensure quality questions and answers

## 🚀 Quick Start

### Prerequisites

- Node.js (v14 or higher)
- Python 3.8+
- pip (Python package manager)

### Installation

#### Frontend Setup
```bash
# Clone the repository
git clone <your-repo-url>
cd QuizWhiz

# Install frontend dependencies
npm install

# Start the development server
npm run dev
```

#### Backend Setup
```bash
# Navigate to server directory
cd server

# Install Python dependencies
pip install -r requirements.txt

# Run Django migrations (if any)
python manage.py migrate

# Start the Django server
python manage.py runserver
```

### Usage

1. **Start both servers**: Make sure both frontend (Vite) and backend (Django) servers are running
2. **Upload your notes**: Click the upload button and select a .txt file containing your lecture transcript
3. **Wait for processing**: The AI models will analyze your text and generate questions
4. **Take the quiz**: Answer the generated multiple-choice questions to test your knowledge

## 🏗️ Architecture

### Frontend (React + Vite)
- **React 18+** with modern hooks and context API
- **Material-UI (MUI)** for consistent, accessible UI components
- **Axios** for API communication
- **Vite** for fast development and optimized builds

### Backend (Django + AI Models)
- **Django 5.1** REST API server
- **Hugging Face Transformers** for AI model integration
- **PyTorch** for deep learning model inference

## 🤖 AI Models Used

QuizWhiz leverages four specialized AI models for different aspects of quiz generation:

| Model | Purpose | Details |
|-------|---------|---------|
| `valhalla/t5-base-e2e-qg` | Question Generation | Creates relevant questions from text |
| `deepset/roberta-base-squad2` | Answer Extraction | Identifies correct answers from context |
| `google/flan-t5-base` | Distractor Generation | Creates plausible incorrect answer options |
| `microsoft/deberta-v3-large` | Answer Ranking | Ensures distractors are relevant but incorrect |

## 📁 Project Structure

```
QuizWhiz/
├── src/                          # React frontend source
│   ├── Components/
│   │   ├── Questions.jsx         # Quiz question display component
│   │   └── Options.jsx           # Multiple choice options component
│   ├── App.jsx                   # Main application component
│   ├── Context.jsx               # React context for state management
│   ├── UploadDesk.jsx           # File upload interface
│   ├── OutputDesk.jsx           # Quiz display interface
│   └── main.jsx                 # Application entry point
├── server/                       # Django backend
│   ├── quiz/                     # Main Django app
│   │   ├── views.py             # API endpoints
│   │   ├── pipelines.py         # AI model pipeline configuration
│   │   └── models.py            # Database models
│   ├── manage.py                # Django management script
│   └── requirements.txt         # Python dependencies
├── public/                       # Static assets
├── package.json                  # Node.js dependencies
└── vite.config.js               # Vite configuration
```

## 🛠️ Development

### Scripts

**Frontend:**
```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run lint     # Run ESLint
npm run preview  # Preview production build
```

**Backend:**
```bash
python manage.py runserver      # Start Django server
python manage.py migrate        # Apply database migrations
python manage.py test          # Run tests
```

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
