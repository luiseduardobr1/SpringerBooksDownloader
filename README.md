# SpringerBooksDownloader
Download all free books from Springer and upload to Google Drive automatically. 

## Requirements
* [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
* [PyPDF2](https://pythonhosted.org/PyPDF2/)
* [PyDrive](https://pythonhosted.org/PyDrive/)

## How to use it
1) Read this [tutorial](https://medium.com/@annissouames99/how-to-upload-files-automatically-to-drive-with-python-ee19bb13dda) to activate a Google Drive's API project.

2) Save the *string.pdf* in the same folder of *SpringerExtractorPDF.py*, because the complete list of the books are in a PDF file that will be read it to get all the links. 

3) The books will be saved in *livros* folder (it will be in the same directory). After the download, the book will be uploaded to your Google Drive's account, but it could take many hours to complete the task, so it's better to delete (or replace by a comment) all the final code lines if you **don't** want to save it **directly** in Google Drive:
```Python
# UPLOAD - VERY SLOW !
    path = r"livros"   
    for x in os.listdir(path): 
        f = drive.CreateFile({'title': x}) 
        f.SetContentFile(os.path.join(path, x)) 
        f.Upload() 
    print('Upload Completo!')
    os.remove('livros' + '//' + nome_livro + '.pdf')
 ```
