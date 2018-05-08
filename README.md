INTRODUCTION:
=============

* This tool basically helps you to get information about selected text in web-browser.
* It provides you with:
    1. URl of current window.
    2. X-path of selected DOM object.
    3. Selected text.
* Also batch updates are now available for bookmarklet, so just keep on adding all the information you need and add it all at once.

**It is available as:**

CHROME PLUGIN:
==============

Pros:
-----
1. You need not load the tool again and again. Load it once and you are good to go!
2. It is now a feature of your browser!

Cons:
-----
1. Browser Dependent.
2. Not easy to load for non-techno-savvy people.

How to use:
-----------
1. Download/Clone current repo.
2. Open chrome browser.
3. Go to this [link](chrome://extensions) or from menu(thrre dots) go to more tools->extension
4. Tick on Developer mode.
5. Select load unpacked extension.
6. Now just click on icon of tool whenever you want to use it.

BOOKMARKLET:
============

Pros:
-----
1. It is browser independent.
2. Easy to load.
3. Batch updates available.

Cons:
-----
1. Need to load it for every webpage.

Features:
---------
1. Selected text gets highlighted.
2. All information is stored on local server.
3. On visiting website again and loading the tool, the previous selections get highlighted.

How to use:
-----------
1. BACKEND
	1. cd ./backend
	2. sudo -H pip3 install requirements.txt -r
	3. python3 dbFlask.py 

2. FRONTEND
	1. Open the [bookmarklet.html](./Bookmarklet/frontend/bookmarklet.html)
	2. Enable bookmark bar from settings.
	3. Drag & Drop the link to bookmark bar.
	4. Click on the button in bookmark bar to use it on any page(Only if scripting is not blocked).

Routes:
-------

1. [data](http://127.0.0.1:5000/data)
	1. Url: http://127.0.0.1:5000/data
	2. Method: GET
	3. Paramreters: url
	4. Description: To get the json object of all data of this url.

2. [getdata](http://127.0.0.1:5000/getdata)
	1. Url: http://127.0.0.1:5000/getdata
	2. Method: GET
	3. Parameters: None
	4. Description: To get the json object of all data.	


3. [store](http://127.0.0.1:5000/store)
	1. Url: http://127.0.0.1:5000/store
	2. Method: POST
	3. Parameters: url,xpath,text,startPoint,endPoint,tag
	4. Description: To store the data (of selected text) at backend.

4. [texts](http://127.0.0.1:5000/texts)
	1. Url: http://127.0.0.1:5000/texts
	2. Method: GET
	3. Parameters: None
	4. Description: To get all the text stored in DB.
