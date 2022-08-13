## Uploading File/Folder in Google colab

1. By mounting the google drive on google colab, then access the google drive's file directly.<br>
```
from google.colab import drive 
drive.mount('/content/gdrive', force_remount=True)
```
