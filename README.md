# Phân Tích Bìa Sách

This project is a web application that allows users to analyze book covers using a Flask server and a machine learning model. The application provides a user interface to upload book cover images and returns the title, author, and publisher of the book.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [API Endpoints](#api-endpoints)
- [License](#license)

## Installation

1. **Clone the repository:**
    ```sh
    git clone https://github.com/user020603/vqa-book-cover-analysis.git
    cd vqa-book-cover-analysis
    ```

2. **Install the required Python packages:**
    ```sh
    pip install flask-ngrok transformers pillow flask-cors pyngrok torch torchvision sentencepiece accelerate bitsandbytes
    ```

3. **Set up ngrok:**
    ```sh
    ngrok authtoken YOUR_NGROK_AUTH_TOKEN
    ```

## Usage

1. **Run the Flask server:**
#### Option 1: Local Execution
Open [`VQAFlaskServer.ipynb`](VQAFlaskServer.ipynb) in Jupyter Notebook or Jupyter Lab and run all cells to start the Flask server.

#### Option 2: Google Colab 
Click the link below to open and run the Flask server directly in Google Colab:

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lHWJptIK0ZcefrjXDOOesVO2YKuQdLvC?usp=sharing)


3. **Open the web application:**
    Open [`index.html`](index.html) in a web browser to access the user interface for uploading book cover images.

4. **Analyze a book cover:**
    - Click on the "Choose File" button to upload a book cover image.
    - Click on the "Analyze" button to send the image to the server for analysis.
    - The results (title, author, and publisher) will be displayed on the web page.

## Project Structure
- [`index.html`](index.html): The front-end of the application, providing a user interface for uploading book cover images and displaying the results.
- [`VQAFlaskServer.ipynb`](VQAFlaskServer.ipynb): The back-end of the application, containing the Flask server and the machine learning model for analyzing book covers.

## Dependencies

- Flask
- Flask-CORS
- Flask-Ngrok
- Transformers
- Pillow
- Pyngrok
- Torch
- Torchvision
- Sentencepiece
- Accelerate
- Bitsandbytes

## API Endpoints

### `POST /analyze-book-cover-v4`

Analyzes a book cover image and returns the title, author, and publisher.

- **Request:**
    - `file`: The book cover image file.

- **Response:**
    ```json
    {
        "title": "Book Title",
        "author": "Book Author",
        "publisher": "Book Publisher"
    }
    ```

## UI
![alt text](image.png)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
