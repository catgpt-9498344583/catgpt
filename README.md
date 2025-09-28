# Cat GPT

This project contains a **Python Flask** backend and a **Bun + Vite** frontend, organized as Git submodules.

## 📦 Cloning the Project

This repo uses **Git submodules**, so clone it with:

```bash
git clone --recurse-submodules https://github.com/catgpt-9498344583/catgpt.git

or 

git clone --recurse-submodules git@github.com:catgpt-9498344583/catgpt.git

If you already cloned the repo without --recurse-submodules, initialize the submodules with:

git submodule update --init --recursive

🛠 Project Structure

/
├── backend/         # Python Flask backend (submodule)
├── frontend/        # Bun + Vite frontend (submodule)
├── docker-compose-dev.yml
├── docker-compose-prod.yml
├── run_dev.sh / .ps1
├── build_prod.sh / .ps1

🔧 Development Setup

Start the app with hot reload in both frontend and backend.
Linux/macOS:

./run_dev.sh

Windows PowerShell:

.\run_dev.ps1

Then open:

Frontend: http://localhost:5173

Backend API: http://localhost:5000/api/hello
📦 Production Build & Run

Build and start the production containers with:
Linux/macOS:

./build_prod.sh

Windows PowerShell:

.\build_prod.ps1

Once started, Flask will serve the built frontend from /static.

Visit:

http://localhost:5000

🐳 Docker Compose Overview
File	Description
docker-compose-dev.yml	Dev setup with live reload
docker-compose-prod.yml	Production setup with static build
🧼 Clean Up

To stop and remove the containers:

docker compose -f docker-compose-dev.yml down
# or
docker compose -f docker-compose-prod.yml down
