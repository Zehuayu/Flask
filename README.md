# curl-exercises

exercise 2
   curl -o http-sasy.html  http://www.jmarshall.com/easy/http/
 
 frame:
 -o is get a web page and store in a local file with a specific name
 I save source of URL at  http://www.jmarshall.com/easy/http/
 to a file http-sasy.html
 the differents between open the URL in a browser and open the file http- sasy.html
 1)the file http-easy.html doesn't have images like the URL opened in the  browser.
 2)the browser’s location bar is different, one is from local, the other  is from www.jmarshall.com
 
 
exercise 3
   curl -o duckduckgo.html http://www.duckduckgo.com
 I saved the content from URL at http://www.duckduckgo.com in  duckduckgo.html, but it shows the error 301
 Then I find the solution from https://curl.haxx.se/docs/manual.html
 with -L ,can make curl follow a location
 I typed:
   curl -L duckduckgo.txt http://www.duckduckgo.com > duckduckgo.html
 from google.com,I find "A > B" means output A into file B 
 And I use ">" to save the contents of URL at http://www.duckduckgo.com in   the file duckduckgo.html
 then duckduckdo.html works

 Investigate the HTTP transaction using curl’s verbose mode
 I searches in https://curl.haxx.se/docs/manual.html
 use the -v flag to get verbosefetching. Curl will output lots of info and  what it sends and receives in order to let the user see all client-server  interaction (but it won't show you the actual data).
 I typed: 
   curl -v http://www.duckduckgo.com > duckduckgo.txt
 I find that the duckduckgo.txt doesn't show the full contents,just the html body
 after searching in https://curl.haxx.se/mail/archive-2005-06/0090.html#start. I get the solition:
 (1) curl -v http://www.duckduckgo.com  ... --stderr duckduckgo.txt
 (2) curl -v http://www.duckduckgo.com ... 2> duckduckgo.txt
 (3) curl -v http://www.duckduckgo.com ... > duckduckgo.txt 2>&1
    (1)and(2)show the same(without html body)
    (3)output all the contents
 And the file duckduckgo.txt here is got from the command (3)


exercise 4
 In my browser, search for the term GMIT using DuckDuckGo, the URL in the
browser’s location bar:
   https://duckduckgo.com/?q=GMIT&t=h_&ia=about
 I adapt it to search "science" :
   https://duckduckgo.com/?q=science&t=h_&ia=about
 then typed in cmder:
   curl -o science.txt https://duckduckgo.com/?q=science&t=h_&ia=about
 save the response to the file science.txt
 
 By the same way:
 type in cmder:
   curl -o computer-science.txt https://duckduckgo.com/?q=computer-science&t=h_&ia=about
 to save the response to the file science.txt


exercise 5
   curl -o response.html -L http://duckduckgo.com/?q=gmit&format=json
 I save the content into the file response.html
 I use -L because with out it just like exercise 3, display the error 301
 And I used the software brackets to re-format response.html to make it easier to read.



exercise 6
   mkdir www
 to create the folder "www"
   I copy the Basic template from http://getbootstrap.com/getting-started/
   and save as index.html
   then type "python -m http.server" to run a Python SimpleHTTPServer in www
   I get the port 8000
   the URL of my browther location bar is http://10.211.55.7:8000/curl-exercises/www/
   I copy the Bootstrap CDN to the file index.html
   











 
 
 
 
