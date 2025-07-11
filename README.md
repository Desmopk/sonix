🎵 Sonix — Full Stack Music Streaming App

Sonix is a sleek, Spotify-style music streaming platform built with a clean MVVM architecture. It combines a **Flutter** frontend with a **FastAPI** backend, backed by **PostgreSQL**, local caching via **Hive**, and managed state through **Riverpod Generators**.

🧰 Tech Stack

🔙 Backend  
- FastAPI (Python)  
- PostgreSQL (Database)  
- SQLAlchemy or Tortoise ORM (DB modeling)  
- Docker + Docker Compose  

📱 Frontend  
- Flutter (Cross-platform: Android, iOS, Web, Desktop)  
- MVVM Design Pattern  
- Riverpod with Generator-based Providers  
- Hive (Local Storage / Cache)  
- Audio Playback Packages (e.g., `just_audio`, `audio_service`)

🔥 Key Features

- 🎼 Browse & search songs, albums, artists  
- ▶️ Play audio tracks with playback controls  
- 🔁 Playlist creation & management  
- 💾 Offline playback with local caching (Hive)  
- 🔄 MVVM state management through Riverpod generators  
- 🐳 Dockerized backend for easy deployment

🚀 Getting Started

📦 Prerequisites  
- Flutter SDK  
- Dart SDK ≥ 3.7.0  
- Python 3.9+  
- PostgreSQL  
- Docker & Docker Compose  

🐳 Backend Setup

```bash
# Clone the repo
git clone https://github.com/Desmopk/sonix.git
cd sonix/backend

# Copy example env and configure DB credentials
cp .env.example .env

# Start backend
docker-compose up -d

# Or run directly
pip install -r requirements.txt
uvicorn main:app --reload
```
📱 Frontend Setup
```bash
cd ../frontend
# Install dependencies
flutter pub get
# Run app on emulator or device
flutter run
```
🎵 Architecture Overview

User Interaction →
- Flutter ViewModel (Riverpod)
- API calls to FastAPI
- PostgreSQL for data persistence
- Hive for local caching & offline playback
- Streaming playback via audio packages

🛡️ State Management

- MVVM with Riverpod Generators
- ViewModels handle API calls, caching logic, playback state
- UI watches observable state from providers

📦 Deployment

- Backend: Deploy via Docker Compose or Kubernetes
- Frontend: Build for web or native platforms
- Future Enhancements:
- Authentication (JWT/OAuth)
- Social features (likes, follows)
- Recommendations using ML / collaborative filtering
