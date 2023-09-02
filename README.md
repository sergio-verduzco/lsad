# LogSeq Assets Downloader

This could be useful when [migrating from Roam Research to Logseq](https://hub.logseq.com/getting-started/uQdEHALJo7RWnDLLLP7uux/how-to-switch-from-roam-research-to-logseq/epbNMUYPWBSjxfrog8v2sH). In particular, I had uploaded a large number of
images and PDF files into my Roam graph. When I exported the graph from Roam and imported it to Logseq
all those files were still in some remote server.

Here's a script to go through all the pages in a Logseq graph exported from
Roam Research, download all external PDF and image files to the `assets` folder, and
change the links accordingly.

Each page should be a separate `.md` file in the `pages` folder.

Typical image link: `![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fmorawa%2FGhQGPfOOrV.png?alt=media&token=4abeaf62-63c5-4859-97a5-91ace19e5dd7)`  
Should be changed to `![](<../assets/<page name>_img<image number>.png)`  

Typical pdf link: `{{pdf(https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fmorawa%2FgAFZMChTVX.%20Standard%20notations%20for%20Deep%20Learning.pdf?alt=media&token=3ce4577b-bc6a-431c-9988-a40c20104af2)}}`  
Should be changed to `![pdf](../assets/<page name>_pdf<pdf number>.pdf)`

See more instructions in the `lsad.ipynb` file.