How to run code:(step by step procedure)
Step 1: Clone the Repository

Clone the repository to get the code and configuration files.

git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>

🔹 Step 2: Open in Google Colab

Go to Google Colab
.

Click File → Open Notebook → GitHub.

Paste the repo URL and open the main .ipynb notebook.

🔹 Step 3: Set Runtime

In Colab, go to Runtime → Change runtime type.

Select Python 3 and choose GPU if required.

🔹 Step 4: Install Dependencies

Run the following command in a notebook cell:

pip install -r requirements.txt

🔹 Step 5: Mount Google Drive

To save models and outputs persistently:

from google.colab import drive
drive.mount('/content/drive')

🔹 Step 6: Provide API Keys (if required)

Use secure input methods instead of hardcoding credentials:

from getpass import getpass
API_KEY = getpass("Enter API Key: ")

🔹 Step 7: Download & Prepare Dataset

Place datasets inside the data/ folder.

If using external datasets, download them via wget, gdown, or APIs as shown in the notebook.

🔹 Step 8: Run the Notebook

Execute cells sequentially for correct results.

Recommended: Runtime → Restart and run all for reproducibility.

🔹 Step 9: Save Checkpoints & Outputs

Save model weights and results for reuse:

torch.save(model.state_dict(), '/content/drive/MyDrive/project/checkpoint.pt')
