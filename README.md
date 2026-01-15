# **AI-Powered Wellness Platform (Flutter • Firebase • TensorFlow Lite)**

## **Overview**

Liora is a private, enterprise-grade mobile application designed to deliver a comprehensive wellness experience. The platform integrates advanced menstrual health tracking with a curated wellness marketplace, offering users a secure, intelligent, and personalized environment.

Built with Flutter and Dart, Liora combines scalable architecture, cloud-backed services, and on-device machine learning to ensure high performance, privacy, and reliability.

---

## **Core Features**

### **AI-Powered Health Tracking**

* Intelligent menstrual cycle predictions using on-device machine learning models
* Personalized insights based on historical data patterns
* Offline-capable inference with no dependency on external servers

### **Privacy-First Architecture**

* All sensitive health computations are performed locally on-device
* No transmission of personal health prediction data
* Secure storage and handling of user information

### **Wellness Marketplace**

* Integrated product catalog for health and wellness items
* Cart management and order processing
* Optimized media loading for performance

### **Personalized Recommendations**

* Dynamic wellness and dietary suggestions
* Recommendations aligned with user cycle phases

### **Administrative Capabilities**

* User and inventory management tools
* Order monitoring and system-level oversight

---

## **Platform Support**

| Platform    | Status    | Notes                              |
| ----------- | --------- | ---------------------------------- |
| Android     | Supported | Optimized for Android 10 and above |
| iOS         | Planned   | Future App Store deployment        |
| Web/Desktop | Planned   | Cross-platform expansion roadmap   |

---

## **Technology Stack**

### **Core Technologies**

* **Framework:** Flutter (SDK ^3.19.x)
* **Language:** Dart
* **Machine Learning:** TensorFlow Lite (on-device inference)
* **Backend Services:** Firebase

### **Firebase Services**

* Authentication for secure user identity management
* Cloud Firestore for real-time NoSQL data storage
* Cloud Storage for media and user assets

### **State Management**

* Provider

### **Key Dependencies**

* `tflite_flutter` – ML model execution
* `table_calendar` – Cycle visualization
* `cached_network_image` – Optimized image loading
* `google_fonts` – Typography
* `shared_preferences` – Local data persistence

---

## **Architecture**

The application follows a **modular layered architecture**, ensuring clear separation of concerns, scalability, and maintainability.

### **Layers**

* **Presentation Layer:** UI components and state-aware widgets
* **Business Logic Layer:** Services, providers, and ML processing
* **Data Layer:** Strongly typed models for structured data handling
* **Core Layer:** Shared utilities, theming, and global configurations

---

## **Project Structure**

```
lib/
├── admin/          # Administrative dashboards and tools
├── core/           # Global configurations, themes, utilities
├── home/           # Dashboard and core logic
├── models/         # Data models (e.g., products, orders, ML data)
├── onboarding/     # User onboarding flow
├── screens/        # UI screens (auth, insights, settings)
├── services/       # Business logic and ML services
└── shop/           # Marketplace features
```

---

## **Module Overview**

| Module     | Description                                  |
| ---------- | -------------------------------------------- |
| Admin      | System management, users, and inventory      |
| Core       | Global state, themes, shared utilities       |
| Home       | Main dashboard and core application logic    |
| Models     | Data structures and schema definitions       |
| Onboarding | Initial user flow and setup                  |
| Screens    | UI components and application views          |
| Services   | Business logic, ML processing, and providers |
| Shop       | Product browsing and commerce functionality  |

---

## **Setup & Installation**

### **Prerequisites**

* Flutter SDK (^3.19.x)
* Dart SDK (compatible with Flutter version)
* Android Studio or Visual Studio Code with Flutter plugins
* Python (optional, for ML model training)

---

### **Installation Steps**

1. **Clone the Repository**

   ```bash
   git clone <repository-url>
   cd liora
   ```

2. **Install Dependencies**

   ```bash
   flutter pub get
   ```

3. **Prepare Machine Learning Model**

   * Run:

     ```bash
     python train_cycle_model.py
     ```
   * Place the generated `.tflite` file inside the `assets/` directory

4. **Configure Firebase**

   * Add your own `google-services.json` (Android)
   * Update Firebase configuration files as required

---

## **Running the Application**

```bash
flutter run
```

---

## **Build Instructions (Android)**

```bash
flutter build apk --release
```

---

## **Development Guidelines**

### **Code Organization**

* Keep business logic within `lib/services/`
* Avoid placing complex logic directly in UI widgets
* Use modular, reusable components

### **State Management**

* Access state using `Provider` or `Consumer` patterns

### **Extensibility**

* Follow existing folder structure for new features
* Maintain consistency with shared themes and models
* Ensure type safety using defined data models

---

## **Security & Privacy**

* Sensitive health computations are processed locally
* User data is securely stored and managed
* Access to the project is restricted to authorized environments
* External configuration (e.g., Firebase keys) must not be committed

---

## **Roadmap**

* Enhanced AI-based cycle prediction
* Advanced dietary and wellness recommendations
* iOS platform support
* Push notification system
* Production deployment to mobile app stores