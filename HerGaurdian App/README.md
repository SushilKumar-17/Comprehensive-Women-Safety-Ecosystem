# APP: HerGuardian 

**HerGuardian** is a mobile safety application as a part of this women safety ecosystem designed to enhance women’s security by providing real-time SOS alerts, AI-integrated surveillance, and seamless connectivity with guardians. This project was built as part of a hackathon initiative and integrates smart technology with user-focused design to ensure emergency responsiveness.
<p align="center">
  <img src="https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"/>
  <img src="https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white"/>
  <img src="https://img.shields.io/badge/Google_Maps_API-4285F4?style=for-the-badge&logo=googlemaps&logoColor=white"/>
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=white"/>
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white"/>
</p>

## Features

-  One-tap SOS alerts with location
-  Real-time location tracking
-  Integration with AI-based CCTV for monitoring
-  Heat map visualization for risky zones
-  Emergency contact auto-calling
-  Smartwatch pairing support
-  Backend API integration for real-time communication

---

> ⚠️ **Under Maintenance:**  
> While the **Heatmap** feature works as expected on **Expo Go**, it is still **buggy on the APK version** and currently **under active development**.  
> You can test the latest APK version here:  
> 👉 [Download APK](https://expo.dev/accounts/udai1273/projects/herGuardian/builds/e2d51141-7c91-4b7e-b6eb-70afcdf5df75) 

---

##  Technologies Used

- **Frontend**: React Native (with or without Expo)
- **Backend**: Your own API (integrate manually)
- **AI & Surveillance**: Python, OpenCV (optional if you plan to build the surveillance system)
- **Database**: MongoDB / Firebase / your own choice
- **Maps & Location**: Google Maps API

---

##  Installation Setup

### 1. Clone the repository

### 2. Install dependencies

If using **Expo**:

```bash
npm install -g expo-cli
npm install
```

If using **React Native CLI**:

```bash
npm install
npx react-native link
```

---

##  Environment Setup

Create a `.env` file in the root directory and configure the following:

```
MONGODB_URI=https://your-api-url.com
API_KEY=your_google_maps_key
```

> **Note**: Do **not** commit your `.env` file.

---

## ▶ Running the App

If you're using **Expo**:

```bash
npx expo start
```

---

##  Backend/API Integration

This project is front-end focused. To enable full functionality:

1. Plug in your backend API in `.env` (`API_URL`)
2. Ensure your API supports:
   - Sending and receiving SOS data
   - Location updates
   - Heat map data (optional)
3. Host your backend (e.g., Render, Railway, or AWS)

---

##  Project Structure

```
herGuardian/
├── assets/
├── components/
├── screens/
├── services/
├── App.js
├── .env
└── package.json
```

---

##  Disclaimer

This project was built for educational and hackathon purposes. While it uses real-time features and attempts to provide genuine help in emergencies, **please do not rely on it in real-world life-threatening situations without thorough testing and validation.**

---

## App Interface (Figma Prototype)

<div align="center">
  <img src="assets/img (5).png" alt="App UI with Map & SOS" width="750"/>
</div>

## App in Work (Live working)
<dib align="centre">
<img src="https://github.com/user-attachments/assets/18b9d3f9-4aaf-4b4d-8d9a-a5f643a7ed21" width="200"/>
<img src="https://github.com/user-attachments/assets/d7133b87-81ad-4536-89ce-25125ae0883f" width="200" />
<img src="https://github.com/user-attachments/assets/a9f06c1b-4efb-48d4-85f2-fc4c6c8d6144" width="200" />
<img src="https://github.com/user-attachments/assets/a9b3af37-0191-4bd1-b8c4-8edddab9bc4f" width="200" />
<img src="https://github.com/user-attachments/assets/fa671a47-c8ce-4fdb-8cff-67edb0898ee5" width="200"/>
<img src="https://github.com/user-attachments/assets/185a0a71-356d-4e5b-99ff-2df0172753b5" width="200" />
<img src="https://github.com/user-attachments/assets/c0d1aaea-ac4b-4811-a96b-60bef33d694b" width="200" />
</div>
---

## # Future Work

- Add background tracking service
- Integrate secure login via OAuth
- Add panic voice command
- Smartwatch SOS gestures
- Geo-fencing alerts

---
##  Contributors

This project is a result of a team effort combining AI, IoT, and mobile development to address real-world safety challenges.



