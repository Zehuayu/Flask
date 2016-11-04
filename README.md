# flask-exercises

exercise 2
I copy the Flask is Fun example from http://flask.pocoo.org/ to the file hello.hp. 
then type  python hello.py to get the URL: http://127.0.0.1:5000 .
from this URL ,I can see the content of hello.py .

exercise 3
I create the folder static, and download the Bootstrap basic template into index.html in it.
then change the location bar of my browser to http://127.0.0.1:5000/static/index.html to see the index.html.

exercise 4
I change the file hello.py , 
"@app.route('/user/<username>')
def show_user(username):
return 'Your name is %s' % username"
then run it ,and typed http://127.0.0.1:5000/user/TangqiFeng to the browser, it shows: Your name is TangqiFeng.

