# Book Recommendation System

A machine learning-based book recommendation system that suggests books to users based on their preferences. The system uses the K-Nearest Neighbors (KNN) algorithm to recommend similar books and provides book details like name and image through a user-friendly interface built with Streamlit.

## Features

- **Book Recommendations**: Recommends books based on user-selected input.
- **K-Nearest Neighbors (KNN)**: Uses KNN algorithm to find similar books based on content features.
- **Streamlit Interface**: Easy-to-use web interface for interacting with the recommender system.
- **Image Display**: Displays book covers alongside recommendations.

## Technologies Used

- **Python**: Primary programming language
- **K-Nearest Neighbors (KNN)**: Machine learning algorithm for book recommendations
- **Streamlit**: For building the interactive web interface
- **Numpy**: Data manipulation and numerical operations
- **Pandas**: Data handling and analysis
- **Pickle**: For saving and loading trained models and data
- **Scikit-learn**: For machine learning model implementation

## Setup & Installation

Follow the steps below to set up and run the Book Recommendation System on your local machine.

### Prerequisites

Before running the project, make sure you have the following installed:

- Python 3.x (preferably 3.7+)
- pip (Python package installer)

### Steps to Run the Project

1. **Clone the Repository**

   First, clone the repository to your local machine:
   bash
   git clone https://github.com/yourusername/Book-Recommendation-System.git
   cd Book-Recommendation-System
2. **Create a Virtual Environment (optional but recommended)**

To keep dependencies isolated, create a virtual environment:

bash
python -m venv venv
source venv/bin/activate   # For Linux/Mac
.\venv\Scripts\activate    # For Windows

3. **Install Dependencies**

Install the required Python libraries using the following command:
bash
pip install -r requirements.txt
If the requirements.txt file doesn't exist, you can manually install the dependencies with:
pip install numpy pandas scikit-learn streamlit

4. **Load Pretrained Models and Data**

The system requires trained models and data files for predictions. If they are not already available, you need to run the training pipeline to generate the models.

trained_model.pkl: Model trained using KNN for book recommendation.
book_pivot.pkl: Data file storing the pivot table for books.
final_rating.pkl: File containing the final ratings and book information.
If these files are missing, follow the next step to train the model.

5. **Run the Training Pipeline**

If you do not have the pre-trained models, you can train the system by running the train_engine() function:
Open the app.py file in the notebook/ directory.

Run the code to train the model:
python :
obj.train_engine()
This will train the KNN model using the dataset and generate the necessary .pkl files.

6. **Run the Streamlit Application**

After installing the dependencies and loading the models, you can start the Streamlit web interface by running:
bash
streamlit run app.py
This command will launch the application in your web browser.

7. **Interacting with the Application**

Book Selection: Use the dropdown to select a book.
Get Recommendations: Click the "Show Recommendation" button to view book suggestions.
Training: If you want to train the model again, click the "Train Recommender System" button.
Folder Structure

**Here’s a breakdown of the important files and folders in the project:**

bash
Book-Recommendation-System/
│                                                                                                                                                                  
├── notebook/                                                                                                                                                      
│   ├── app.py                    # Main Streamlit app                                                                                                             
│   ├── style.css                 # Custom styles for the app                                                                                                      
│   └── requirements.txt          # Project dependencies                                                                                                           
                                                                                                                                                                  
│                                                                                                                                                                  
├── books_recommender/            # Core logic for book recommendation                                                                                             
│   ├── components/               # Components of the recommendation pipeline                                                                                      
│   ├── logger/                   # Logging setup                                                                                                                  
│   └── config/                   # Configuration files                                                                                                            

│                                                                                                                                                                  
├── data/                         # Data folder for raw and processed data                                                                                         
│   ├── book_names.pkl            # Pickled book names for dropdown                                                                                                
│   └── final_rating.pkl          # Data with book ratings and URLs                                                                                                                                                                                                                                                                   
│                                                                                                                                                                  
├── artifacts/                    # Folder to store trained models and serialized data                                                                             
│   ├── trained_model.pkl         # Trained KNN model                                                                                                              
│   ├── book_pivot.pkl            # Pivoted book data                                                                                                              
│   └── final_rating.pkl          # Final ratings data                                                                                                             
└── README.md                     # Project documentation                                                                                                      

**Troubleshooting**
If you encounter any issues during setup or execution:

Missing Libraries: Ensure all dependencies are installed by running pip install -r requirements.txt.
Missing Data Files: Ensure the necessary .pkl files are present in the data/ folder. If not, you can retrain the model.
Web Interface Not Loading: If Streamlit fails to launch, ensure that streamlit is correctly installed and you’re running streamlit run app.py from the correct directory.
