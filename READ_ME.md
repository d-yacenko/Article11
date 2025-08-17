Here’s a clear English version of your text:

---

In this project, you will find the code and pretrained model that allow you to reproduce the results presented in the paper.

The content consists of a set of notebooks and serialization files:

* **1\_rcnn.ipynb** – Model Training
* **2\_rcnn.ipynb** – Resuming Training
* **3\_rcnn.ipynb** – Model Evaluation
* **4\_rcnn\_report.ipynb** – Training Visualization
* **5\_baseline\_alexnet.ipynb** – Baseline AlexNet for comparison
* **5\_baseline\_densenet.ipynb** – Baseline DenseNet
* **5\_baseline\_efficientnet.ipynb** – Baseline EfficientNet
* **rnn\_conv\_12.31.18.pth, rnn\_conv\_10.32.43.pth, rnn\_conv\_11.26.30.pth** – model weight files obtained during training. Since training lasted about two days, it was completed in three sessions, resulting in three checkpoint files (in chronological order). The final model is **rnn\_conv\_11.26.30.pth**.
* **rnn\_conv\_ds\_08.12.54.pkl** – file with the status of the train/val/gold dataset splits used in our study, which can be reused for idempotent reproduction of the experiments.
* **rnn\_conv\_report\_12.31.18.pkl, rnn\_conv\_report\_10.32.43.pkl, rnn\_conv\_11.26.30.pkl** – log files with model metrics collected during training (also in chronological order).

**Note:** The code is designed to work with a random subset of the ImageNet dataset. The dataset itself is not included in the repository due to its large size. However, you can reconstruct it yourself by following these steps:

1. Visit the [ImageNet website](https://www.image-net.org/) and select **Download**.
2. Register on the site (an academic or corporate email is required).
3. Once your request is approved, log back in and go to the **Download** section under your account.
4. Download the main archive: **ILSVRC2012\_img\_train.tar** (\~138 GB).
5. From the extracted folder, copy the following class subfolders into a directory named `/MAIN/files20/`:

   ```
   n01675722  n01755581  n01798484  n02087046  n02091467  n02106030  
   n02110185  n02113624  n02125311  n02361337  n02442845  n02493509  
   n02793495  n02802426  n02843684  n02977058  n03223299  n03457902  
   n03825788  n04147183
   ```

   This `/MAIN/files20/` directory will be used for training.
