# online-book-recommendation-using-collaborative-filtering-website


### Introduction
This is an **Online Book Recommendation System** that provides personalized book suggestions to users based on collaborative filtering techniques. The application predicts book recommendations by analyzing user preferences and book ratings. It is built using Flask, Python, and several data science libraries.

---

### Features
1. **Popular Books Display:**
   - Shows a list of trending books with details like the title, author, rating, and number of votes.

2. **Book Recommendation:**
   - Users can input a book title to get similar book recommendations based on collaborative filtering.

3. **Interactive UI:**
   - A user-friendly interface created using HTML templates for input and displaying results.

---

### Workflow
1. **Homepage (`/`):**
   - Displays a list of popular books with their details (title, author, ratings, and images).

2. **Recommendation Page (`/recommend`):**
   - Users can input the name of a book to get recommendations.

3. **Backend Recommendation Logic:**
   - When the user submits a query, the application:
     - Retrieves the book title input.
     - Identifies similar books based on pre-computed similarity scores.
     - Displays the recommendations, including book details like title, author, and cover image.

---

### Files and Structure
1. **`apps.py`:**
   - Main Flask application file to handle routes, request processing, and rendering templates.
   - Uses pre-trained data and models stored in `.pkl` files.

2. **Pretrained Data Files:**
   - **`popular.pkl`:** Contains data on popular books.
   - **`pt.pkl`:** Pivot table data for collaborative filtering.
   - **`books.pkl`:** Details about all available books (title, author, cover image).
   - **`similarity_scores.pkl`:** Pre-computed similarity matrix for collaborative filtering.

3. **HTML Templates:**
   - **`index.html`:** Template for the homepage showing popular books.
   - **`recommend.html`:** Template for displaying recommendations.

---

### How It Works
1. **Preprocessing:**
   - Books are analyzed, and a similarity matrix is generated using collaborative filtering techniques. 
   - Popular books are identified based on user ratings.

2. **Recommendation Logic:**
   - When a user inputs a book title:
     - The index of the book in the pivot table is identified.
     - The similarity matrix is used to find the most similar books.
     - The details of these similar books are retrieved and displayed.

3. **Frontend Integration:**
   - Flask renders the data dynamically using templates to provide an interactive experience.

---

### Installation and Setup
1. **Prerequisites:**
   - Python (>=3.7)
   - Flask
   - Libraries: `numpy`, `pickle`, `pandas`

2. **Steps:**
   - Clone the repository and navigate to the project directory.
   - Ensure the `.pkl` files are present in the directory.
   - Install dependencies:
     ```bash
     pip install -r requirements.txt
     ```
   - Run the Flask application:
     ```bash
     python apps.py
     ```
   - Access the application at `http://127.0.0.1:5000`.

---

### Usage
1. **Homepage:**
   - Explore the trending books and their details.
2. **Recommendation Page:**
   - Input a book title and get personalized recommendations.

---

