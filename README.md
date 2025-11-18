# Pinpoint Digital - Digital Marketing Agency Landing Page

This is a fully responsive, single-page landing website for **Pinpoint Digital**, a digital marketing agency specializing in Google Business Profile optimization for local businesses in Pune. The site is designed to attract clients and generate leads through a "Free Audit" offer, with form data captured using a serverless Google Apps Script backend.

[![Netlify Status](https://api.netlify.com/api/v1/badges/YOUR_NETLIFY_BADGE_ID/deploy-status)](https://app.netlify.com/sites/pinpointdigital/deploys)

**Live Demo:** [**pinpointdigital.netlify.app**](https://pinpointdigital.netlify.app)

---

## ✨ Features

-   **Modern & Responsive Design**: A clean layout that looks great on all devices, from mobile phones to desktops.
-   **Interactive UI/UX**:
    -   **Sticky Navigation**: An always-accessible navigation bar that sticks to the top on scroll.
    -   **Smooth Scrolling**: Clicking on nav links smoothly scrolls the user to the corresponding section.
    -   **Scroll-Reveal Animations**: Content sections elegantly fade in as the user scrolls down the page.
-   **Lead Generation Form**: A comprehensive contact form for users to request a free business audit.
-   **Serverless Backend Integration**: The contact form is fully functional and sends data to a **Google Apps Script** endpoint, which can be easily configured to save leads directly into a Google Sheet.
-   **SEO Optimized**: Includes meta tags for description, keywords, and a local business schema to improve search engine visibility.

---

## 🛠️ Technologies Used

-   **Frontend**:
    -   `HTML5`
    -   `Tailwind CSS` (for styling and layout)
    -   `Vanilla JavaScript` (for DOM manipulation and interactivity)
-   **Backend**:
    -   `Google Apps Script` (to handle form submissions without a dedicated server)

---

## 🚀 Setup and Installation

This project is built with static files and requires no complex setup.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/pinpoint_digital.git](https://github.com/your-username/pinpoint_digital.git)
    ```

2.  **Navigate to the project directory:**
    ```bash
    cd pinpoint_digital
    ```

3.  **Open the `index.html` file:**
    -   Simply open the `index.html` file in your favorite web browser to view the site locally.

---

## 📝 Form Integration with Google Apps Script

The contact form is configured to send submission data to a Google Apps Script URL. This allows you to collect leads in a Google Sheet for free.

### How It Works:
1.  A user fills out and submits the form.
2.  The JavaScript `fetch()` API sends the form data via a `POST` request to the specified `scriptURL`.
3.  The Google Apps Script receives the data, processes it, and appends it as a new row in a connected Google Sheet.
4.  The script returns a JSON response (`{result: 'success'}` or an error message).
5.  The JavaScript on the frontend displays a success or error message to the user based on the response.

### How to Set Up Your Own Form Backend:
1.  **Create a Google Sheet** to store the form responses.
2.  Go to `Extensions > Apps Script` to open the script editor.
3.  Paste the Google Apps Script code for handling POST requests (you can find many templates online for this).
4.  **Deploy** the script as a **Web App**.
5.  **Copy the Web App URL** provided after deployment.
6.  In the `index.html` file, find the following JavaScript block and replace the placeholder `scriptURL` with your own URL:

    ```javascript
    // ... inside the <script> tag at the bottom of the HTML file
    
    const scriptURL = 'YOUR_GOOGLE_APPS_SCRIPT_URL_HERE';
    
    form.addEventListener('submit', e => {
      // ... rest of the submission logic
    });
    ```

--

## 🖼️ Screenshots
 
_You can add screenshots of the website's sections here to showcase the design._

| Hero Section                                   | Services Section                            |
| ---------------------------------------------- | ------------------------------------------- |
| ![Hero Section Screenshot](<img src="https://i.ibb.co/N626G0bc/Screenshot-2025-09-29-021258.png" alt="Screenshot-2025-09-29-021258" border="0">)      | ![Services Section Screenshot](<img src="https://i.ibb.co/S767ryGQ/Screenshot-2025-09-29-021320.png" alt="Screenshot-2025-09-29-021320" border="0">) |
| **Contact Form** | **Mobile View** |
| ![Contact Form Screenshot](<img src="https://i.ibb.co/W4KTR21n/Screenshot-2025-09-29-021336.png" alt="Screenshot-2025-09-29-021336" border="0">)      | ![Mobile View Screenshot](<img src="https://i.ibb.co/P0q4gdz/Screenshot-2025-09-29-021409.png" alt="Screenshot-2025-09-29-021409" border="0">)    |

---
