## Uploading File/Folder in Google colab

1. By mounting the google drive on Google colab, then access the google drive's file directly.<br>
```
from google.colab import drive 
drive.mount('/content/gdrive', force_remount=True)
```
2. If the folder is too large(for example, a folder which contains 40000 image files), you may upload the zip file to google drive first, mounting it(as above), then unzipped it in Google Colab. The metacode is:<br>
!unzip -u <source_path.zip> -d <destination_path> <br>
For example,
```
!unzip -u "/content/gdrive/MyDrive/roadcrack.zip" -d /content/gdrive/MyDrive/roadcrack
```
3. If you were just need to upload a single file, then you may use:
```
from google.colab import files
uploaded = files.upload()
```
4. If the file is a csv file, you may read the file by using pd.read_csv(), for example:
```
df_train = pd.read_csv("train.csv", sep=",", header=0) # If the data is separated by comma
df_train = pd.read_csv("train.csv", sep=" ", header=0) # If the data is separated by space
df_train = pd.read_csv("ttrain.csv", header=0) # If the data is placed inside the excel's cell properly.
```
