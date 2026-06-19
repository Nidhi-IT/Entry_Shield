# Entry Shield: Smart Campus Security System 🛡️

Entry Shield is a full-stack, automated security and visitor management system designed to secure campus entry points. By integrating live facial recognition and Automated License Plate Recognition (ALPR), the system replaces manual logbooks with a seamless, digital verification process. 

## 🚀 Key Features

* **Role-Based Access Control:** Secure, customized dashboards for Admins, Guards (Sub-Admins), and Members/Students, powered by Clerk Authentication.
* **Live Automated License Plate Recognition (ALPR):** Real-time vehicle plate scanning using YOLO object detection combined with EasyOCR/PaddleOCR to match arriving vehicles against registered databases.
* **Facial Verification:** Automated live facial scanning using DeepFace and RetinaFace to instantly verify authorized students, parents, and visitors.
* **Visitor & Student Portals:** Secure forms for students to register their details and host visitors, with automated data sanitization and strict ID validation constraints.
* **Digital Passes:** Automated generation and state-tracking of entry receipts and passes (pending, approved, denied).

## 💻 Tech Stack

**Frontend:**
* **Framework:** React (Vite)
* **Routing:** React Router DOM
* **Styling:** Tailwind CSS, Framer Motion (Animations), Lucide React (Icons)
* **Authentication:** Clerk React
* **Forms & Validation:** React Hook Form, Zod

**Backend:**
* **Framework:** Python / Flask
* **Database:** MongoDB (PyMongo)
* **Computer Vision & OCR:** OpenCV, Ultralytics (YOLO), DeepFace, RetinaFace, EasyOCR, PaddleOCR
* **Data Processing:** NumPy, Pandas

## ⚙️ Installation & Setup

### Prerequisites
* Node.js (v18+)
* Python 3.11+
* MongoDB URI
* Clerk API Keys

### 1. Clone the Repository
\`\`\`bash
git clone https://github.com/your-username/entry-shield.git
cd entry-shield
\`\`\`

### 2. Backend Setup
Navigate to the backend directory and install the required Python packages:
\`\`\`bash
cd backend
pip install -r requirements.txt
\`\`\`
Create a `.env` file in the backend folder and add your environment variables (e.g., MongoDB URI).
Run the Flask server:
\`\`\`bash
python app.py
\`\`\`

### 3. Frontend Setup
Open a new terminal, navigate to the client directory, and install the Node dependencies:
\`\`\`bash
cd client
npm install
\`\`\`
Create a `.env` file in the `client` directory and add your Clerk publishable key:
\`\`\`env
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_key
\`\`\`
Start the Vite development server:
\`\`\`bash
npm run dev
\`\`\`

