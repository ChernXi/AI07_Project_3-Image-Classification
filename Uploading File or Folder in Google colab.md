## Uploading File/Folder in Google colab

1. By mounting the google drive on Google colab, you can access the google drive's file directly.<br>
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

3. To read the folder that you have just uploaded, click the directory at the LHS of the Google Colab, and find your file there. <br>
![image](https://user-images.githubusercontent.com/108325848/184474011-3933d7da-57a5-40e2-bd62-89602636d30d.png)

you may copy the file path, <br>
![image](https://user-images.githubusercontent.com/108325848/184474141-448e2002-417a-4184-b0c2-3a2a741e7f2e.png)

then use keras.utils.image_dataset_from_directory() to read it:
```
file_path = r"/content/gdrive/MyDrive/roadcrack/road crack"
data_dir = pathlib.Path(file_path)

SEED = 12345
IMG_SIZE = (120,120)
BATCH_SIZE = 16

train_dataset = keras.utils.image_dataset_from_directory(data_dir,validation_split=0.2,subset='training',seed=SEED,shuffle=True,
                                                         image_size=IMG_SIZE,batch_size=BATCH_SIZE)
val_dataset = keras.utils.image_dataset_from_directory(data_dir,validation_split=0.2,subset='validation',seed=SEED,shuffle=True,
                                                         image_size=IMG_SIZE,batch_size=BATCH_SIZE)
``` 
The result will be something like:
![image](https://user-images.githubusercontent.com/108325848/184474514-5f09d3f3-aad1-44c6-90a8-35e11da6749d.png)

4. If you were just need to upload a single file, then you may use:
```
from google.colab import files
uploaded = files.upload()
```
5. If the file is a csv file, you may read the file by using pd.read_csv(), for example:
```
df_train = pd.read_csv("train.csv", sep=",", header=0) # If the data is separated by comma
df_train = pd.read_csv("train.csv", sep=" ", header=0) # If the data is separated by space
df_train = pd.read_csv("ttrain.csv", header=0) # If the data is placed inside the excel's cell properly.
```
