# 💰 Expense Tracker

A beautiful and intuitive expense tracking application built with React.js and Tailwind CSS. Track your spending, set budgets, and manage your finances with ease.

![Expense Tracker](https://img.shields.io/badge/React-18.3.1-blue.svg)
![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-3.4.1-38bdf8.svg)
![Vite](https://img.shields.io/badge/Vite-5.4.10-646cff.svg)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED.svg)
![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-2088FF.svg)

## ✨ Features

- 💵 **Budget Management** - Set and track your monthly budget
- 📝 **Add Expenses** - Quickly add expenses with amount, category, and description
- 🗑️ **Delete Expenses** - Remove expenses with a single click
- 📊 **Visual Progress** - Real-time budget usage tracking with progress bar
- 🎨 **Category Icons** - Color-coded categories for easy identification
  - 🍔 Food
  - 🚗 Transport
  - 🛍️ Shopping
  - 💡 Bills
  - 🎮 Entertainment
  - 📦 Other
- 💾 **Data Persistence** - Automatically saves your data using localStorage
- 📱 **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- 🎯 **User-Friendly Interface** - Clean, modern design with smooth animations

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone <repository-url>
cd ExpenseTracker
```

2. Install dependencies
```bash
npm install
```

3. Start the development server
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

## 🛠️ Built With

- **React.js** - JavaScript library for building user interfaces
- **Tailwind CSS** - Utility-first CSS framework for styling
- **Vite** - Next-generation frontend tooling for fast development
- **Lucide React** - Beautiful and consistent icon library

## 📦 Project Structure

```
ExpenseTracker/
├── .github/
│   └── workflows/
│       └── docker-publish.yml  # GitHub Actions CI/CD pipeline
├── src/
│   ├── App.jsx                 # Main application component
│   ├── main.jsx                # Application entry point
│   └── index.css               # Global styles and Tailwind imports
├── .dockerignore               # Docker ignore file
├── docker-compose.yml          # Docker Compose configuration
├── Dockerfile                  # Multi-stage Docker build
├── nginx.conf                  # Nginx server configuration
├── index.html                  # HTML template
├── package.json                # Project dependencies and scripts
├── vite.config.js              # Vite configuration
├── tailwind.config.js          # Tailwind CSS configuration
├── postcss.config.js           # PostCSS configuration
└── README.md                   # Project documentation
```

## 💡 Usage

1. **Set Your Budget**: Enter your monthly budget in the input field at the top
2. **Add Expenses**: 
   - Enter the expense amount
   - Select a category from the dropdown
   - Add a description (optional)
   - Click "Add Expense"
3. **Track Progress**: Watch the progress bar update as you add expenses
4. **Delete Expenses**: Click the trash icon next to any expense to remove it
5. **Your Data is Safe**: All data is automatically saved to your browser's localStorage

## 🎨 Color Scheme

- **Primary Gradient**: Purple to Pink (`from-purple-600 to-pink-600`)
- **Success**: Green (`text-green-600`)
- **Warning**: Yellow (`text-yellow-600`)
- **Danger**: Red (`text-red-600`)
- **Categories**: Color-coded for quick visual identification

## 📱 Responsive Design

The application is fully responsive and optimized for:
- 📱 Mobile devices (320px and up)
- 📱 Tablets (768px and up)
- 💻 Desktop (1024px and up)

## 🔧 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

## 🐳 Docker Deployment

### Using Docker Compose (Recommended)

1. Build and run the application:
```bash
docker-compose up -d
```

2. Access the application at `http://localhost:3000`

3. Stop the application:
```bash
docker-compose down
```

### Using Docker CLI

1. Build the Docker image:
```bash
docker build -t expense-tracker .
```

2. Run the container:
```bash
docker run -d -p 3000:80 --name expense-tracker-app expense-tracker
```

3. Stop and remove the container:
```bash
docker stop expense-tracker-app
docker rm expense-tracker-app
```

### Docker Hub

The Docker image is automatically built and pushed to Docker Hub via GitHub Actions on every push to the main branch.

Pull the latest image:
```bash
docker pull abhijeet14d/expense-tracker:latest
```

Run the pre-built image:
```bash
docker run -d -p 3000:80 abhijeet14d/expense-tracker:latest
```

## 🔄 CI/CD Pipeline

This project uses GitHub Actions to automatically:
- Build Docker images for multiple architectures (amd64, arm64)
- Push images to Docker Hub with proper tags
- Update Docker Hub description
- Support version tags and branch-based tags

### Setting up GitHub Actions

1. Go to your GitHub repository settings
2. Navigate to **Secrets and variables** → **Actions**
3. Add the following secrets:
   - `DOCKER_USERNAME` - Your Docker Hub username
   - `DOCKER_PASSWORD` - Your Docker Hub password or access token

### Workflow Triggers

The pipeline runs on:
- Push to `main` or `master` branch
- Pull requests to `main` or `master` branch
- Version tags (e.g., `v1.0.0`)
- Manual workflow dispatch

## 🌟 Future Enhancements

- [ ] Monthly/Yearly expense reports
- [ ] Export data to CSV
- [ ] Multiple budget categories
- [ ] Expense charts and analytics
- [ ] Dark mode support
- [ ] User authentication
- [ ] Cloud data sync
