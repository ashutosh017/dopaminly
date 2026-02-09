# Dopaminly 📸

**Dopaminly** is a high-performance, full-stack social media platform designed for instant engagement. Built with a modern tech stack focusing on type safety, real-time interactivity, and scalable media handling, it mimics the core features of leading social networks with a "dopamine-driven" user experience.

---

## 🚀 Tech Stack

| Layer | Technology |
| :--- | :--- |
| **Framework** | [Next.js 14+](https://nextjs.org/) (App Router) |
| **Language** | [TypeScript](https://www.typescriptlang.org/) |
| **Database** | [PostgreSQL](https://www.postgresql.org/) |
| **ORM** | [Prisma](https://www.prisma.io/) |
| **Real-time** | [Pusher](https://pusher.com/) (WebSockets) |
| **Media Storage** | [Cloudinary](https://cloudinary.com/) |
| **Styling** | [Tailwind CSS](https://tailwindcss.com/) |

---

## ✨ Features

* **Authentication:** Secure user onboarding and session management.
* **Media Feed:** Create, view, and interact with image-based posts.
* **Real-time Notifications:** Instant alerts for likes, comments, follow requests, and mentions powered by Pusher.
* **Social Graph:** Follow/Unfollow system with support for private profiles and follow requests.
* **Interactions:** Like and comment on posts, with nested comment replies.
* **Direct Messaging:** Real-time private conversations between users.
* **Media Management:** Optimized image uploads and transformations via Cloudinary.
* **Search & Discovery:** Indexed search for users and profiles.

---

## 📊 Database Schema

The project utilizes a robust relational schema designed for high-integrity social data:



### Core Models:
* **User:** Profiles, credentials, and relationship mapping.
* **Post:** Media URLs, captions, and metadata.
* **Follow / FollowRequest:** Handles the "Social Graph" including pending requests for private accounts.
* **Notification:** A centralized system to track various engagement types (`LIKE`, `COMMENT`, `FOLLOW`, etc.).
* **Conversation / Message:** The backbone of the real-time chat system.

---

## 🛠️ Getting Started

### Prerequisites

* Node.js 18+
* PostgreSQL instance (Local or Hosted)
* Cloudinary Account
* Pusher Account

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/dopaminly.git](https://github.com/your-username/dopaminly.git)
    cd dopaminly
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Environment Variables:**
    Create a `.env` file in the root directory and add your credentials:
    ```env
    DATABASE_URL="postgresql://user:password@localhost:5432/dopaminly"
    NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME="your_cloud_name"
    CLOUDINARY_API_KEY="your_api_key"
    CLOUDINARY_API_SECRET="your_api_secret"
    NEXT_PUBLIC_PUSHER_APP_ID="your_app_id"
    NEXT_PUBLIC_PUSHER_KEY="your_key"
    PUSHER_SECRET="your_secret"
    ```

4.  **Database Migration:**
    ```bash
    npx prisma migrate dev
    npx prisma generate
    ```

5.  **Run the Development Server:**
    ```bash
    npm run dev
    ```

---

## 🏗️ Project Structure

text
├── app/                # Next.js App Router (Pages & API)
├── components/         # Reusable UI components
├── lib/
│   ├── generated/      # Prisma generated client
│   ├── pusher.ts       # Pusher configuration
│   └── prisma.ts       # Prisma singleton client
├── prisma/
│   └── schema.prisma   # Database source of truth
├── public/             # Static assets
└── styles/             # Global CSS and Tailwind config

## 🤝 Contributing
Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

1. Fork the Project

2. Create your Feature Branch (git checkout -b feature/AmazingFeature)

3. Commit your Changes (git commit -m 'Add some AmazingFeature')

4. Push to the Branch (git push origin feature/AmazingFeature)

5. Open a Pull Request
