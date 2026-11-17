# PlantCare – Plant Care Reminder Application 🌱🌿

> *"Your plants, your care, their happy growth."*

### 🌐 Live Demo & Web App
👉 **[Click Here to Open the Live Website](https://keshavm.pythonanywhere.com)**  
- **Live URL:** `https://keshavm.pythonanywhere.com`
- **Demo Account:** `demo@plantcare.com` / `password123`

---

PlantCare is a full-stack, responsive, and secure web application designed to help plant enthusiasts, students, home gardeners, and community farmers cultivate and maintain thriving plants through intelligent schedules, botanical records, and visual growth tracking.

---

## 🚀 Quick Step-by-Step Guide to Run Locally

### 1. Open PowerShell or Command Prompt
Open your terminal and navigate to the project directory:
```powershell
cd "c:\Users\Laptop adda manipal\Desktop\team s\plantcare"
```

### 2. Install Dependencies
```powershell
python -m pip install -r requirements.txt
```

### 3. Initialize Database & Seed Starter Plants
```powershell
python seed.py
```

### 4. Start the Application Server
```powershell
python run.py
```

### 5. Open in Your Browser
- On your laptop: **[http://localhost:5000](http://localhost:5000)** (or `http://127.0.0.1:5000`)
- On phone/tablet (same Wi-Fi): **`http://<your-ip-address>:5000`**

### 🔑 Demo Account Credentials:
- **Email:** `demo@plantcare.com`
- **Password:** `password123`
*(Or click **"Create Account"** to register a new user!)*

---

## 📤 Step-by-Step Guide to Push to GitHub

Follow these exact terminal commands to upload this entire project to your GitHub account:

### Step 1: Install Git
If you haven't installed Git yet, download and install it from [git-scm.com/download/win](https://git-scm.com/download/win).

### Step 2: Create a New GitHub Repository
1. Go to [github.com](https://github.com) and sign in.
2. Click **"+"** (top-right) -> **New repository**.
3. Name it `PlantCare` (do **not** check *"Add a README file"*).
4. Click **Create repository**.
5. Copy your repository link (e.g. `https://github.com/YOUR_USERNAME/PlantCare.git`).

### Step 3: Run Git Commands in Terminal
Open PowerShell in this folder and run:

```powershell
# 1. Navigate to project folder
cd "c:\Users\Laptop adda manipal\Desktop\team s\plantcare"

# 2. Configure your identity (one-time)
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"

# 3. Initialize Git repository
git init

# 4. Stage and commit all files
git add .
git commit -m "Initial commit: Complete PlantCare Full-Stack Web Application"

# 5. Set main branch
git branch -M main

# 6. Link to your GitHub repo
git remote add origin https://github.com/NextGen-Thinkers/plantcare-.git

# 7. Push all code to GitHub
git push -u origin main
```

---

## 🌟 Key Application Features

### Core Management & Schedules
1. **User Authentication & Profiles**: Secure user registration, password hashing (Werkzeug), session handling (Flask-Login), profile avatar uploads, and password reset flows.
2. **Interactive Botanical Dashboard**: Real-time statistics calculated from SQLite (Total Plants, Plants Needing Water, Upcoming Tasks, Healthy Plants), today's care checklist, and immediate quick-actions.
3. **Plant Inventory (My Plants)**: Grid and list view modes, category filters, name/date/watering sorting, and comprehensive plant profiles.
4. **Plant Registration Form**: Upload photos with real-time preview, configure custom watering and fertilizing frequencies, sunlight, and soil profiles.
5. **Plant Library & Encyclopedia**: Pre-seeded collection of common plants (*Tulsi, Monstera, Aloe Vera, Money Plant, Snake Plant, Peace Lily, Rose, Hibiscus*) with one-click adoption into personal gardens.
6. **Watering Reminder & Management**: Automatic recalculation of next due dates upon completion, overdue warning banners, completed activity logs, and interval adjustments.
7. **Fertilizer Scheduling**: Track fertilization cycles, organic liquid food applications, and nutritional reminders.
8. **Interactive Care Calendar**: FullCalendar (Month/Week/List views) dynamically rendering scheduled care tasks and completed milestones.
9. **In-App Notification Centre**: Instant alerts for overdue care, watering deadlines, health alerts, and growth updates with desktop notification support.
10. **Care History Audit Log**: Chronological history filterable by plant, activity type, and date range.

### Advanced Botanical Tools
11. **Plant Health Checker**: Upload photos of stressed foliage, record symptoms (e.g., chlorosis, leaf burn, drooping, powdery mildew), and receive instant diagnosis, cause analysis, care solutions, and prevention tips via a modular rule-based engine (with optional external AI Vision API hook).
12. **Smart Watering Decision**: A scientific guide where users manually assess soil moisture (Dry, Slightly Moist, Wet) and receive tailored watering recommendations based on species and watering intervals without relying on sensors.
13. **Plant Growth Tracker**: Log periodic plant heights (cm), condition evaluations, notes, and visual photos. Generates side-by-side photo progression comparisons and interactive **Chart.js** growth curves.
14. **User Preferences & Settings**: Customizable daily reminder times, theme selection, and notification switches.

---

## 🎨 Visual Design System

- **Forest Green**: `#174C35`
- **Deep Green**: `#123D2B`
- **Sage Green**: `#A8BFA3`
- **Soft Cream**: `#F7F8F2`
- **White**: `#FFFFFF`
- **Light Olive**: `#DCE8D5`
- **Dark Text**: `#26332B`
- **Muted Text**: `#778078`

Featuring Lucide icons, smooth responsive layouts, desktop sidebar navigation, and a mobile-friendly bottom app navigation bar.

---

## 🛠️ Technology Stack

- **Backend**: Python 3, Flask, Flask-SQLAlchemy, Flask-Login, Flask-WTF, WTForms, Werkzeug
- **Database**: SQLite
- **Frontend**: HTML5, CSS3, Vanilla JavaScript, Jinja2 Templates, Bootstrap 5, Lucide Icons, FullCalendar, Chart.js
- **Testing**: Python `unittest` suite

---

## 📁 Project Directory Structure

```text
plantcare/
│
├── app/
│   ├── __init__.py            # Flask App Factory & Blueprint registration
│   ├── extensions.py          # SQLAlchemy, LoginManager, CSRF extensions
│   ├── models.py              # Database models (User, Plant, CareActivity, etc.)
│   ├── services.py            # Date calculations, file uploads, notifications
│   │
│   ├── auth/                  # Authentication routes and WTForms
│   ├── dashboard/             # Dashboard analytics and tasks
│   ├── plants/                # Plant CRUD and collection views
│   ├── library/               # Botanical encyclopedia & adoption
│   ├── watering/              # Watering reminder schedules
│   ├── fertilizer/            # Nutrient scheduling and tracking
│   ├── calendar/              # FullCalendar JSON event feeds
│   ├── notifications/         # Notification centre
│   ├── history/               # Activity audit logs
│   ├── health/                # Plant Health Checker & diagnosis
│   ├── smart_watering/        # Soil-based decision assistant
│   ├── growth/                # Height charts & photo progression
│   ├── profile/               # User profile management
│   ├── settings/              # System and reminder preferences
│   │
│   ├── templates/             # Jinja2 HTML templates
│   │   ├── base.html          # Global layout & sidebar
│   │   ├── auth/
│   │   ├── dashboard/
│   │   ├── plants/
│   │   ├── library/
│   │   ├── watering/
│   │   ├── fertilizer/
│   │   ├── calendar/
│   │   ├── notifications/
│   │   ├── history/
│   │   ├── health/
│   │   ├── smart_watering/
│   │   ├── growth/
│   │   ├── profile/
│   │   ├── settings/
│   │   └── errors/
│   │
│   └── static/
│       ├── css/style.css      # Botanical stylesheet
│       ├── js/main.js         # Client-side scripts & icons
│       └── uploads/           # User plant images and avatars
│
├── instance/                  # SQLite database location (plantcare.db)
├── tests/
│   └── test_plantcare.py      # Automated unit & integration tests
├── config.py                  # Environment and Flask configuration
├── requirements.txt           # Python dependencies
├── run.py                     # Development server entry point
├── seed.py                    # Database seeding script
├── .env.example               # Environment variables template
└── README.md                  # Documentation
```

---

## 🧪 Running Automated Tests

Run the complete test suite:
```powershell
python -m unittest tests/test_plantcare.py
```

---

## 📄 College Demonstration Highlights

For college project presentation or evaluation:
1. Log in using `demo@plantcare.com` / `password123`.
2. Inspect the **Dashboard** to show dynamic metrics calculated from database records.
3. Show the **Care Calendar** to demonstrate FullCalendar synchronization.
4. Open the **Plant Health Checker** and submit sample symptoms (e.g. *yellow leaves*) to review the diagnostic recommendations.
5. Demonstrate the **Smart Watering Decision** system using physical soil condition choices.
6. Open **Plant Growth Tracker** to show side-by-side photos and Chart.js height progression graphs.

