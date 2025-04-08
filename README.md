📝 Project Summary Report
📌 Approach
The goal of this project was to predict grammar scores from audio inputs. The core approach included converting audio to text using automatic speech recognition (ASR), extracting grammar-based features, and applying machine learning models for score prediction.

🧹 Preprocessing Steps
Audio Cleaning: Silence trimming and noise reduction for cleaner transcriptions.

Transcription: Used Whisper model for converting audio to text.

Feature Engineering:

Grammar-based features: num_errors, error_density, readability, etc.

BERT CLS token embeddings for deeper semantic understanding.

Missing Values: Handled with SimpleImputer using mean strategy.

Feature Scaling: Applied StandardScaler for normalized input to models.

⚙️ Pipeline Architecture
Extracted cleaned transcriptions from audio.

Extracted grammar-based and semantic (BERT) features.

Combined features into a single training dataset.

Trained various regressors: SVR, CatBoost, Random Forest.

Final model: StackingRegressor combining CatBoost + SVR, tuned for best performance.

📈 Evaluation Results
Mean Squared Error (MSE): 0.7395

R² Score: 0.4575

Predictions were rounded to the nearest 0.5 for alignment with the grading rubric.
