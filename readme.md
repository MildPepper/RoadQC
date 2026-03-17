# RoadQC Distributor Portal (React Web App)

The Distributor Portal is a secure dashboard built with React and Vite. It is designed to be used by administrators and government auditors to monitor infrastructure quality, verify on-site visits, and manage road projects.

Login Credentials are

email: admin@roadqc.gov
password: nirma123

## Prerequisites

Before running this project, ensure you have the following installed on your machine:

- **Node.js** (v16.0.0 or higher recommended)
- **npm** (comes with Node.js) or **yarn**

## Getting Started

Follow these steps to set up and run the portal locally:

### 1. Install Dependencies

Open your terminal, navigate to the project directory, and install the required npm packages:

```bash
npm install
```

### 2. Environment Variables

Create a `.env` file in the root of the project directory (if it doesn't exist) and add your Supabase credentials:

```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

### 3. Start the Development Server

Start the local development server:

```bash
npm run dev
```

The application will typically be available at `http://localhost:5173`. Open this URL in your browser to view the dashboard.

## Building for Production

To create a production-ready build of the application:

```bash
npm run build
```

This will generate a `dist` folder containing the optimized static assets.










# RoadQC Field App (Flutter Application)
# Warning i wont recommend you to run this if you don't know flutter. It will be your waste of time, instead u can check out the pictures in pdf.
# U can run the other folder dashboard instead.

The Field App is a mobile application built with Flutter. It is designed to be used by on-site inspectors to view road projects, clock in/out of sites with geographical tracking, and upload verification selfies to the RoadQC platform.

## Prerequisites

Before running this project, ensure you have the following installed on your machine:

- **Flutter SDK** (Version 3.19.0 or higher recommended)
- **Android Studio** (for Android Emulator and SDK tools) or **Xcode** (for iOS Simulator)
- **Dart SDK** (comes bundled with Flutter)

Verify your installation by running:
```bash
flutter doctor
```

## Getting Started

Follow these steps to set up and run the app locally:

### 1. Install Dependencies

Open your terminal, navigate to the project directory, and fetch the required pub packages:

```bash
flutter pub get
```

### 2. Environment Variables

Create exactly two `.env` files in the flutter project to ensure compatibility across different build targets (like web). 

Create a `.env` file in the **root** of the project directory (`wetaran_ninja_v1/.env`), and a copy of the same file inside the **assets** directory (`wetaran_ninja_v1/assets/.env`). Both should look like this:

```env
SUPABASE_URL=your_supabase_project_url
SUPABASE_ANON_KEY=your_supabase_anon_key
GOOGLE_MAPS_API_KEY=your_google_maps_api_key
```

*Note: The Google Maps API key is required to reverse geocode the inspector's location when clocking in at a site.*

### 3. Run the Application

You can run the application on a connected device, emulator, or as a web app.

To run on an Android emulator or physical device:
```bash
flutter run
```

To run as a web app for testing (forces a mobile-width layout):
```bash
flutter run -d chrome
```

## Building for Production

To create an APK for Android deployment:

```bash
flutter build apk --release
```

This will generate an installable `app-release.apk` file in `build/app/outputs/flutter-apk/`.

## Technologies Used

- Flutter & Dart
- Supabase (Authentication, Database, & Storage for Selfies)
- Geolocator (GPS Tracking)
- Image Picker (Camera functionality)
- flutter_dotenv (Environment Configuration)
