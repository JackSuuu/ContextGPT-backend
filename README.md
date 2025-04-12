# ContextGPT Backend

This repository contains the FastAPI backend for the ContextGPT project, an AI-powered assistant designed to enhance personal learning by leveraging user-provided context.

## Features

- **Contextual File Upload**: Users can upload various educational materials (e.g., textbooks, tutorial sheets, course slides) to provide context for the AI assistant.

- **Dedicated Summaries**: The system generates concise summaries for the uploaded context files, aiding in quick revision.

- **Contextual Chat**: Engage in conversations strictly within the bounds of the provided context, ensuring relevant and accurate responses.

## Why a Specialized AI Agent?

While general-purpose LLMs like ChatGPT and DeepSeek are powerful, a specialized AI agent offers:

1. **Customization for Specific Use Cases**: Tailored to handle academic materials, providing more relevant assistance for students.

2. **Efficiency & Cost Savings**: Focused processing on pertinent inputs reduces computational overhead.

3. **Enhanced Context Management**: Maintains a clear boundary of context, preventing the dilution of responses with unrelated information.

## Getting Started

### Prerequisites

- Python 3.8 or higher

- [FastAPI](https://fastapi.tiangolo.com/)

- [Docker](https://www.docker.com/) (optional, for containerized deployment)

### Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/JackSuuu/contextGPT-backend.git
   cd contextGPT-backend
   ```


2. **Create a Virtual Environment**:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```


3. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```


4. **Run the Application**:

   ```bash
   uvicorn api:app --reload
   ```


   The API will be accessible at `http://127.0.0.1:8000`.

## Deployment

For production deployment, consider using Docker:

1. **Build the Docker Image**:

   ```bash
   docker build -t contextgpt-backend .
   ```


2. **Run the Docker Container**:

   ```bash
   docker run -d -p 8000:8000 contextgpt-backend
   ```


## Project Structure

- `api.py`: Main FastAPI application.

- `pdf_parsing.py`: Handles parsing of uploaded PDF files.

- `utils.py`: Utility functions used across the application.

- `requirements.txt`: Python dependencies.

- `Dockerfile`: Docker configuration for containerization.

- `deployment.yaml` & `service.yaml`: Kubernetes deployment configurations.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any enhancements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
