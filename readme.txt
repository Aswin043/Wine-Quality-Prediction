# MLflow Experiments & Projects 🎛️

A hands-on repository showcasing both MLflow quickstarts and end-to-end ML projects, from simple demos to real-world regression and classification examples.

---

## 📚 Notebook Deep Dive

### 1. **dlmlflow/basics.ipynb**

* **Goal:** Predict white wine quality (regression) using a simple deep neural network.
* **Tools:** TensorFlow/Keras, Hyperopt, MLflow.
* **Highlights:**

  * Data loading & split via pandas & scikit-learn.
  * Hyperparameter search over learning rate & momentum with `fmin`/TPE.
  * Keras `Normalization` layer + Dense network.
  * Logging params, metrics, and serialized TensorFlow model with MLflow (including a JSON signature for serving).

### 2. **dlmlflow/housepricepredict.ipynb**

* **Goal:** Predict California housing prices (regression).
* **Tools:** scikit-learn, MLflow, GridSearchCV.
* **Highlights:**

  * Load **California housing** dataset from `sklearn.datasets`.
  * Prepare features + target in a DataFrame.
  * `RandomForestRegressor` hyperparameter tuning with `GridSearchCV`.
  * Log parameters, CV results, test metrics, and the final model to MLflow.

### 3. **ml-proj/basics.ipynb**

* **Goal:** Demo MLflow tracking for a classic classification task.
* **Tools:** scikit-learn, MLflow.
* **Highlights:**

  * **Iris dataset** loaded via `datasets.load_iris(return_X_y=True)`.
  * Train/test split.
  * `LogisticRegression` model with custom hyperparameters.
  * Log params, metrics (accuracy), and model artifact to MLflow.

### 4. **ml-proj/housepricepredict.ipynb**

* **Goal:** Another house price example, illustrating how to embed MLflow tracking in an ML pipeline.
* **Tools:** scikit-learn, MLflow.
* **Highlights:**

  * `RandomForestRegressor` on California housing.
  * Train/test split + `GridSearchCV` for hyperparameter search.
  * Logging of CV grid, metrics, and model through MLflow’s Python API.

---

## 🛠️ Setup & Run

1. **Clone & install**

   ```bash
   git clone https://github.com/yourusername/your-repo.git
   cd your-repo
   pip install -r requirements.txt
   ```

2. **Launch MLflow UI**

   ```bash
   mlflow ui
   ```

   Browse to [http://localhost:5000](http://localhost:5000).

3. **Run notebooks**

   * **Deep learning project:**

     ```bash
     jupyter notebook dlmlflow/basics.ipynb
     ```
   * **Classic ML demos:**

     ```bash
     jupyter notebook ml-proj/basics.ipynb
     ```

4. **Serve a model**

   ```bash
   mlflow models serve -m "runs:/<RUN_ID>/model" --port 1234
   ```

---

## 🎉 Enjoy & Experiment

Feel free to tweak hyperparameters, swap datasets, or integrate new algorithms. This repo is a sandbox for learning MLflow and end-to-end ML workflows—have fun!
