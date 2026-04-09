# Accident-Detection-and-Alert-System

# File Structure : 

# ADS/
  ├── alert/                          # Logic for notification systems
  │   ├── alert_manager.py            # Coordinates all alert types
  │   ├── sms_alert.py                # SMS notification logic (e.g., Twilio)
  │   └── sound_alert.py              # Audio/Alarm alert logic
  ├── camera/                         # Video input management
  │   ├── dashcam_input.py            # Live dashcam feed handling
  │   └── video_file_input.py         # Processing stored video files
  ├── dataset/                        # Raw video data for training/testing
  │   ├── accident_videos/            # Positive samples (accidents)
  │   └── non_accident_videos/        # Negative samples (normal driving)
  ├── detection/                      # Core AI detection logic
  │   └── cnn_accident_detector.py    # CNN-based detection script
  ├── frames/                         # Extracted image frames from videos
  │   ├── accident/                   # Frames showing accidents
  │   └── non_accident/               # Frames showing normal traffic
  ├── gps/                            # Location tracking services
  │   └── location_fetcher.py         # Retrieves coordinates during accidents
  ├── gui/                            # Graphical User Interface files
  │   ├── dashboard_ui.py             # Main monitoring dashboard
  │   └── file_upload_ui.py           # Interface for uploading videos
  ├── model/                          # Saved AI models and weights
  │   ├── accident_model.h5           # Keras H5 model file
  │   ├── accident_model.keras        # Keras native model file
  │   ├── accident_model.tflite       # Optimized model for edge devices
  │   └── best_model.keras            # Highest accuracy model checkpoint
  ├── preprocessing/                  # Data cleaning and preparation
  │   ├── frame_resize.py             # Resizing images for model input
  │   └── normalize.py                # Pixel value normalization logic
  ├── recorder/                       # Video recording functionality
  │   └── event_video_recorder.py     # Saves clips when an event is detected
  ├── utils/                          # Helper functions and utilities
  ├── admin_data.json                 # Configuration/Admin credentials
  ├── extract_frames.py               # Script to convert videos into images
  ├── main.py                         # Application entry point
  ├── requirements.txt                # List of Python dependencies
  ├── test_camera.py                  # Script to test hardware camera
  ├── test_model.py                   # Script to evaluate model performance
  ├── test_twilio.py                  # Script to test SMS functionality
  └── train_model.py                  # Script to train the neural network
