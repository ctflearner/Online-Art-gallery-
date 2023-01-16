<h1>Online Art Gallery</h1>

<h3>Sensitive Cookie in HTTPS Session Without 'Secure' Attribute</h3>

<h4>Description</h4>
 The Secure attribute for sensitive cookies in HTTPS sessions is not set, which could cause the user agent to send those cookies in plaintext over an HTTP session.
 
 <h4>Proof Of Concept</h4>
 
 ````php
 POST /art/admin/ HTTP/1.1
Host: localhost
Content-Length: 46
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="109", "Not_A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
Origin: http://localhost
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/109.0.5414.75 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://localhost/art/admin/
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9
Cookie: PHPSESSID=8alf0rbfjmhm3ddra7si0cv7qc
Connection: close

uname=admin%40admin.com&password=12345&submit=
 ````
 
