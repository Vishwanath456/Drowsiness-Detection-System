# Drowsiness Detection System

This is a web-based application that uses your webcam to monitor your eyes and detect signs of drowsiness in real-time. If it detects that your eyes have been closed for an extended period, it will play an alert sound.

## Features

-   **Real-time Eye Tracking:** Uses MediaPipe to accurately track facial landmarks, specifically around the eyes.
-   **Drowsiness Detection:** Calculates the Eye Aspect Ratio (EAR) to determine if your eyes are closed.
-   **Sound Alert:** Plays a `.wav` file to alert you when drowsiness is detected.
-   **Web Interface:** A simple Flask-based web interface to display the video feed and detection status.

## Requirements

-   Python 3.x
-   A webcam

## Installation

1.  **Clone the repository or download the files:**
    Make sure you have all the project files (`app.py`, `requirements.txt`, `Alert.wav`, and the `templates` directory) in a single project folder.

2.  **Create and activate a virtual environment:**
    Open your terminal in the project directory and run the following commands:

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```
    *On Windows, use `venv\Scripts\activate`*

3.  **Install the dependencies:**
    With your virtual environment activated, install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

4.  **Alert Sound:**
    This project uses an `Alert.wav` file for the sound alert. Make sure this file is present in the root directory of the project. You can replace it with your own `.wav` file, but be sure to update the filename in `app.py` if you do.

## Usage

1.  **Run the application:**
    Execute the following command in your terminal from the project's root directory:

    ```bash
    python app.py
    ```

2.  **Access the web interface:**
    Open your web browser and navigate to the following URL:

    [http://127.0.0.1:5000](http://127.0.0.1:5000)

    You should see the video feed from your webcam with the drowsiness detection overlay.

3.  **Stopping the application:**
    To stop the Flask server, go back to your terminal and press `CTRL+C`.

## How It Works

-   **Flask:** Serves as the web framework to stream the video feed to the web interface.
-   **OpenCV:** Captures the video from the webcam and handles image processing.
-   **MediaPipe:** Provides the machine learning model for real-time face mesh and landmark detection.
-   **Pygame:** Used to play the audio alert. 