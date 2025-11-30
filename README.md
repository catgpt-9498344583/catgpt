# Cat GPT

This project contains a **Python Flask** backend and a **React + Vite** frontend, organized as Git submodules.

## 📦 Cloning the Project

This repo uses **Git submodules**, so clone it with:

```bash
git clone --recurse-submodules https://github.com/catgpt-9498344583/catgpt.git

or 

git clone --recurse-submodules git@github.com:catgpt-9498344583/catgpt.git

If you already cloned the repo without --recurse-submodules, initialize the submodules with:

git submodule update --init --recursive
```

## 🛠 Project Structure

```bash
/
├── backend/         # Python Flask backend (submodule)
├── frontend/        # React + Vite frontend (submodule)
├── docker-compose-dev.yml
├── docker-compose-prod.yml
├── run_dev.sh / .ps1
├── build_prod.sh / .ps1
```

## 🔧 Development Setup
* Supports Linux, Windows, and Mac
### Requirements
* Docker - 29.0.4
* Docker Compose - 2.40.3

Start the app with development mode for both frontend and backend.
Linux/macOS:
```bash
./run_dev.sh

or

docker compose -f docker-compose-dev.yml up --build
```
Windows PowerShell:

```ps1
.\run_dev.ps1

or 

docker compose -f docker-compose-dev.yml up --build
```
Then open:

Frontend: `http://localhost:5173`

Backend API Test: `http://localhost:5000/api/hello`
📦 Production Build & Run

🐳 Docker Compose Overview
File	Description
docker-compose-dev.yml	Dev setup 
docker-compose-prod.yml	Production setup
🧼 Clean Up

To stop and remove the containers:

docker compose -f docker-compose-dev.yml down
# or
docker compose -f docker-compose-prod.yml down
