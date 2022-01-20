# FAQs

## Computers and systems 

### Which editor should I use?

[Visual Studio Code](https://code.visualstudio.com) will be the best editor for most. It can handle pretty much all languages and formats. It can natively handle Jupyter notebooks. The remote SSH plugin lets you work in the exactly same environment even when your programs are running on a server. 

For a lightweight editor, it may be worthwhile to learn vim. Use [NeoVim](https://neovim.io). 

### Why should I keep typing my password when I ssh into a server? Can I avoid doing that?

If you don't have your ssh key generated, generate your key by following https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent 

```sh
ssh-copy-id -i ~/.ssh/id_ed25519.pub user@host
```

`id_ed25519.pub` can be different depending on how you generated your ssh key. 


### It is annoying to setup a new server or new computing environments. Any solution? 

Create a [dotfile](https://dotfiles.github.io) repo. A dotfile repo efers to a repo that contains all the settings (e.g., git, vim, shell, python, etc.) as well as a script to install them into a new environment. For each new computer to set up, you can simply clone & install it and you're done with the setup. 


### Can I avoid typing the full hostname whenever I ssh into a server?

Yes! You should use ssh confg. You can store all kinds of pre-configured settings for each server by using ssh config. 


### How can I easily ssh into the computing servers that are not open to the world?

You can add the following to your `~/.ssh/config` (explanation: https://backdrift.org/transparent-proxy-with-ssh).

```
# Bastion server
Host sharks
    HostName sharks.rest.of.domain.name
    User yourusername

# computing server
Host ember
    HostName ember.rest.of.domain.name
    User yourusername
    ForwardAgent yes
    ProxyCommand ssh yourusername@sharks.rest.of.domain.name nc %h %p
```

Once you copy your public key to `sharks`, you can simply run `ssh ember` to connect to `ember`. 

### How can I effectively use IU's supercomputers?

- [Recording](https://iu.mediaspace.kaltura.com/media/t/1_dr5mq1ek)
- [Demo repo](https://github.com/yangkcatiu/workflowdemo)

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

## Figures

### What should I use for diagrams or other custom figures?

For plots, try to make it as complete as possible to minimize manual post-processing. Usually there will be many iterations on the figure, so more you automate, the better. 

For simple figures, you can consider using [TikZ/PGF](https://texample.net/tikz/examples/all/). It allows you to _script_ diagrams. It is built on the graph structure (everything in the figure is more or less node or edge) and quite nice to draw network/graph figures, although there is a pretty _huge_ learning curve. You can do incredible drawings with TikZ/PGF. 

Adobe illustrator is probably the most powerful tool to draw all kinds of diagrams and figures. However, it is like a big chain saw. Consider [OmniGraffle](https://www.omnigroup.com/omnigraffle) (Mac) or [Keynote](https://www.apple.com/keynote/) (or Powerpoint) as a tool for quickly sketching the figure. Illustrator can be used for polishing and composing the figures created in these apps. 

## Jobs

### Internship

You can find many possible internship positions on LinkedIn. You can also talk to professors because they can recommend you to certain positions/people. The best time to apply for a summer internship is usually October-December. It is very helpful to have technical CS conference publications and presence on GitHub. Many positions will require coding interview so you will need to prepare for that. For research internships, use keyword "Research Intern" and for Data Science Internship use "Data Science Intern".






