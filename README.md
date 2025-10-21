
# YARAH AI

YARAH AI is a sophisticated web application designed for deep and insightful scriptural study. It combines a modern, user-friendly interface with the power of generative AI to allow users to ask context-rich questions about the Bible, other religious texts, and historical events.

![YARAH AI Screenshot](https://storage.googleapis.com/aistudio-marketplace-public/project_1720542308892/L2FwcC9hc3NldHMvU2NyZWVuc2hvdCAyMDI0LTA3LTA5IGF0IDUuNDQuNTIgUE0ucG5n_1720543501655_0)

## Features

- **AI-Powered Analysis**: Leverages Google's Gemini Pro model to provide comprehensive answers, relevant Bible verses, cross-references to other texts, and historical context.
- **User Authentication**: Secure signup and login system to save user data.
- **Guest Mode**: A "Try the Demo" option allows new users to experience the app's full functionality without mandatory registration.
- **Conversation History**: Registered users can save and revisit their previous study sessions.
- **Context-Aware Queries**: Users can provide optional context to their questions for more nuanced and accurate AI responses.
- **Modern UI/UX**: Clean, responsive, and mobile-first design.
- **Light & Dark Mode**: A theme toggle for comfortable viewing in any lighting condition.
- **Thematic Design**: Features a subtle "Tree of Life" background to create an immersive study environment.

## Tech Stack

- **Frontend**: React, TypeScript, Tailwind CSS
- **AI**: Google Gemini API (`@google/genai`)
- **Local Persistence**: Browser `localStorage` is used to simulate a database for users and conversations.

## Getting Started

Follow these instructions to set up and run the project locally for development and testing.

### Prerequisites

You will need a modern web browser and a local web server to run the project. You can use the `http-server` npm package or the "Live Server" extension in VS Code.

### Installation & Setup

1.  **Clone the repository (or download the source files):**
    ```bash
    git clone https://github.com/your-username/yarah-ai.git
    cd yarah-ai
    ```

2.  **Set up Environment Variables:**
    The application requires an API key from Google AI Studio to interact with the Gemini API.

    -   Create a new file named `.env.local` in the root of the project.
    -   Copy the contents of `.env.example` into `.env.local`.
    -   Open `.env.local` and add your Google Gemini API key:

    ```env
    # .env.local
    API_KEY="YOUR_GOOGLE_GEMINI_API_KEY"
    OPENAI_API_KEY="YOUR_OPENAI_API_KEY" # Currently unused, but placeholder is here
    ```

3.  **Run the application:**
    -   Start a local web server in the project's root directory.
    -   If you have Node.js installed, you can use `npx`:
        ```bash
        npx http-server
        ```
    -   Open your browser and navigate to the local address provided by the server (e.g., `http://localhost:8080`).

## Deployment

This project is configured for easy, zero-config deployment to [Vercel](https://vercel.com/).

### Deploying to Vercel

1.  **Push to GitHub/GitLab/Bitbucket:**
    Ensure your project is pushed to a Git repository.

2.  **Import Project on Vercel:**
    -   Log in to your Vercel account.
    -   Click "Add New..." -> "Project".
    -   Import the Git repository containing your project.

3.  **Configure Project:**
    -   Vercel will automatically detect that this is a static site. The included `vercel.json` file explicitly sets the configuration, so no build settings are needed.
    -   Navigate to the **Environment Variables** section in your Vercel project settings.
    -   Add your Google Gemini API key:
        -   **Name**: `API_KEY`
        -   **Value**: `YOUR_GOOGLE_GEMINI_API_KEY`

4.  **Deploy:**
    -   Click the "Deploy" button. Vercel will deploy your site, and it will be live at the provided domain.
