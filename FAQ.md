## Google Drive and Remote Machine

Often the need arises to transfer data between your local machine and remote machines (servers). On linux, this is usually handled by `scp` or `rsync`.  
*Try `rysnc` if `scp` is taking too much time*

However, depending on your workflow, there may arise a need to transfer between remote machines and cloud services like Google Drive, Dropbox, etc. The slow, inefficient way is to use your local machine as a middle man. 
That is, download data from remote(cloud) to local and upload from local to cloud(remote). TRY NOT TO DO THIS. 

With Google Drive, the aforementioned middle man, a.k.a your local machine, can be elimiated using [rclone](https://rclone.org/drive/). Its amazing. 

Few other resources exist to directly download from google drive to a server:  
* [gdown](https://github.com/wkentaro/gdown)