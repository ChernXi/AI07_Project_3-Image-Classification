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
