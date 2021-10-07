# FAQs

## Computers and systems 

### Can we use Google Drive on remote machines? 

Often the need arises to transfer data between your local machine and remote machines (servers). On linux, this is usually handled by `scp` or `rsync`.  *Try `rysnc` if `scp` is taking too much time*

However, depending on your workflow, there may arise a need to transfer between remote machines and cloud services like Google Drive, Dropbox, etc. The slow, inefficient way is to use your local machine as a middle man. 
That is, download data from remote(cloud) to local and upload from local to cloud(remote). TRY NOT TO DO THIS. 

With Google Drive, the aforementioned middle man, a.k.a your local machine, can be elimiated using [rclone](https://rclone.org/drive/). Its amazing. 

Few other resources exist to directly download from google drive to a server:  
* [gdown](https://github.com/wkentaro/gdown)


## Methods

### How to use and train Sentence Transformer?

Sentence transfomers transform sentences to numerical vectors, which makes it easy to do various NLP tasks using simple vector operations.  
This [repository](https://github.com/skojaku/Practical-Guide-to-Sentence-Transformers) will walk you through how to use and train sentence transformer models using [sentence transformer library](https://www.sbert.net/index.html) and [Hugging Face Model Hub](https://huggingface.co/). [Here](https://iu.mediaspace.kaltura.com/media/t/1_e8qmpqe8) is a  video tutorial by Sadamori Kojaku.

### What is semantic role labeling and how to use it?

- https://iu.mediaspace.kaltura.com/media/t/1_4f4qkder 