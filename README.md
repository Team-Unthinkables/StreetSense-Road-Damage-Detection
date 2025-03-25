# StreetSense - Road Damage Detection App

StreetSense is a Flutter-based mobile application designed to capture images of road surfaces and analyze them for damage such as potholes and cracks. Using a powerful cloud-based detection API, the app provides detailed analysis and risk assessment metrics to help users identify and evaluate road damage.

## 📱 Demo

<!-- Add your app demo video here -->
[Insert app demonstration video]

## ✨ Features

- **Intuitive Camera Interface**: Capture road images with a user-friendly camera UI
- **Gallery Integration**: Select existing images from device gallery
- **Real-time Damage Detection**: Analyze road images using cloud-based AI detection
- **Visual Results**: View detected damage with highlighted bounding boxes
- **Damage Classification**: Differentiate between potholes and cracks
- **Risk Assessment Metrics**:
  - Overall Damage Percentage
  - Hazard Level
  - Accident Risk
  - Comprehensive Risk Assessment
- **Damage Distribution**: Visual representation of damage types
- **Contact Form**: Submit user information for follow-up
- **Responsive Design**: Works across different device sizes

## 🛠️ Technical Architecture

### App Modules

1. **App Entry Point (`main.dart`)**
   - Initializes the Flutter environment
   - Sets up the available camera(s)
   - Runs the app with the CameraScreen as the home screen

2. **Camera Module (`camera_screen.dart`)**
   - Provides live camera preview
   - Allows image capture or gallery selection
   - Includes UI controls (flash toggle, mode selection)
   - Handles navigation to the Display Picture Screen

3. **Image Analysis Module (`display_picture_screen.dart`)**
   - Displays the captured/selected image
   - Processes the image (resizing, compression, encoding)
   - Sends the image to the detection API
   - Handles API response and navigation to analysis screen

4. **Damage Analysis and Display Module (`damage_analysis_screen.dart`)**
   - Shows the image with overlaid detection boxes
   - Calculates damage metrics
   - Displays risk assessment and damage distribution
   - Includes contact information form

### App Workflow

1. App starts and initializes the camera
2. User captures an image or selects from gallery
3. Image is processed and sent to the cloud detection API
4. API returns detection results
5. Results are displayed with visual overlays and metrics
6. User can submit contact information or take another image

## 📊 Damage Analysis Metrics

The app provides comprehensive damage analysis through multiple metrics:

- **Damage Overview**: A pie chart showing the overall damage percentage
- **Hazard Level**: Calculated based on damage type, size, and confidence
- **Accident Risk**: Evaluates potential for accidents based on damage characteristics
- **Risk Assessment**: A weighted combination of hazard level and accident risk
- **Damage Distribution**: Visual meters showing potholes vs. cracks distribution

## 🔧 Installation

### Prerequisites

- Flutter SDK (^3.5.4)
- Dart SDK
- Android Studio or Visual Studio Code with Flutter extensions
- Android SDK or iOS development setup

### Steps

1. Clone the repository:
   ```
   git clone https://github.com/Team-Unthinkables/StreetSense-Road-Damage-Detection.git
   git clone https://github.com/Kanishk1420/StreetSense-Road-Damage-Detection.git
   ```

2. Navigate to the project directory:
   ```
   cd streetsense
   ```

3. Install dependencies:
   ```
   flutter pub get
   ```

4. Run the app:
   ```
   flutter run
   ```

## 📦 Dependencies

The app relies on the following key dependencies:

| Package | Version | Purpose |
|---------|---------|---------|
| camera | 0.10.5+9 | Camera access and control |
| image_picker | 1.0.7 | Accessing the device gallery |
| http | 1.1.0 | Making API requests |
| image | 4.0.15 | Image processing |
| fl_chart | 0.66.0 | Rendering charts and graphs |
| path_provider | 2.1.2 | File system access |
| sensors_plus | 6.1.1 | Device sensor access |

See `pubspec.yaml` for a complete list of dependencies.

## 🔑 API Integration

The app uses the Roboflow API for road damage detection:

- **API Endpoint**: `https://detect.roboflow.com/road-damage-detection-apxtk/5`
- **Model**: Road damage detection model
- **Detection Classes**: Potholes, Cracks (Longitudinal and Alligator)
- **Confidence Threshold**: Dynamically adjusted based on image and damage area
- **Overlap Parameter**: 20%

To use your own API key:
1. Replace the API_KEY constant in `display_picture_screen.dart`
2. Ensure your endpoint URL is correct for your model

## 🔜 Upcoming Features

- **Google Maps Integration**: Adding location tracking and mapping features to plot damage locations and create heatmaps of problematic areas
- **Enhanced Registration System**: Improved user registration page with profile management and historical analysis tracking
- **Model Improvements**: 
  - Higher accuracy detection for various types of potholes
  - Better classification of different crack patterns (longitudinal, alligator, etc.)
  - Improved detection in various lighting and weather conditions
- **UI/UX Enhancements**:
  - Redesigned dashboard with intuitive navigation
  - Dark/light theme options
  - Accessibility improvements
  - Animated transitions between screens
- **Additional Planned Features**:
  - Offline detection capabilities
  - Historical data analysis and trends
  - Direct reporting to local authorities
  - Severity classification system
  - Support for video analysis
  - Damage progression tracking over time

## 👨‍💻 Team Members

### Developers
- **Kanishk** - *Lead Developer*
  - Email: kanishkgupta2003@outlook.com
  
- **Kingshuk Chatterjee** - *UI/UX Designer*
  - Email: kingshuk.chatterjee770@gmail.com
  
- **Md Azlan** - *Idea Interpreter*
  - Email: p038434azlannbpjc2@gmail.com

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

Developed with ❤️ using Flutter