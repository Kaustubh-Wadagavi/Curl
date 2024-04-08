# Understanding Curl

<h2>Introduction</h2>
Curl command is used to transfer the data with URLs. Curl supports various transfer protocols like http, https, ftp, sftp etc. Supported in the following Operating Systems: Microsoft, Linux, macOs and Solaris etc.

<h2>Why Use Curl Commands?</h2>
To speed up server requests for various cybersecurity functions. curl is especially helpful in penetration testing, such as simulating heavy attacks on a server to check its uploading and downloading speeds.

<h2>Difference between curl & wget</h2>

1. The curl & wget are both used for fetching the data over the web. Using curl we can send any type of requests to the URLs whereas the wget is used to download the files.

2. curl support all types of protocols whereas wget supports only https,http and ftp protocols.

3. curl serves the output in standard format whereas wget by default stores the output in a file.
   
4. curl supports custom headers, user authentication, proxy supports and file uploads.. Etc whereas wget is simpler and more straightforward for basic file downloads. It has options for resuming interrupted downloads, recursive downloads, and mirroring entire websites.

5. curl is mostly used for sending custom HTTP requests, interacting with APIs, or testing web services. wget is commonly used for downloading files from URLs, mirroring websites, or fetching files in non-interactive mode.
6. curl is also used for handling output formats, including saving to a file, printing to stdout, or piping to other commands. wget primarily saves files to disk, but it also offers options for displaying progress information and logging output to files.

<h2>Which details curl command gives about URL:</h2>

<h4>1. HTTP Response Headers:</h4>
When making HTTP or HTTPS requests, curl displays the response headers returned by the server. These headers include information such as the server type, content type, content length, date, and more.

<h4>2. Transfer Statistics:</h4>
Curl provides transfer statistics such as total transfer time, average download speed, average upload speed, size of data transferred... etc.

<h4>3. Error Messages:</h4>
In case of any errors during the transfer process, curl typically displays error messages along with error codes or descriptions to help diagnose the issue.

<h4>4. Verbose Output:</h4>
By using the -v or --verbose option, curl produces verbose output, providing more detailed information about the transfer process. This includes request and response headers, SSL/TLS handshake details, and more.

<h4>5. Progress Information:</h4>
During data transfer, curl can display progress information, showing the percentage of completion, current transfer speed, estimated time remaining, and other progress indicators.

<h4>6. SSL/TLS Certificate Details:</h4>
When accessing HTTPS URLs, curl can provide information about SSL/TLS certificates. This includes details such as the certificate issuer, validity period, subject, and other certificate details.

<h4>7. Redirect Information:</h4>
If the requested URL redirects to another location, curl can display information about the redirection. This includes the new URL and the number of redirects followed.

<h2>Some examples of Curl Commands:</h2>
<h4>Getting Header, Status Code, Content of a Webpage:</h4>
<code>curl -si https://test.example.com/</code>

<h4>Printing Detailed Information about a URL (Verbose):</h4>
<code>curl -v https://test.example.com/</code>

<h4>Getting Redirect Information:</h4>
<code>curl -iL https://test.openspecimen.org/</code>

<h4>Printing SSL/TLS Information:</h4>
<code>curl -vk https://test.openspecimen.org/</code>

<h4>Storing Packet Details:</h4>
<code>curl --trace packts_details.txt https://test.openspecimen.org</code>

<h4>Downloading URL in Silent Mode:</h4>
<code>curl -s https://test.openspecimen.org > test.txt</code>

<h4>Specifying Maximum Connection Time:</h4>
<code>curl -L "https://test.openspecimen.org/" --connect-timeout 0.1</code>

<h4>Checking Download Speed:</h4>
<code>curl -o /dev/null -w '%{speed_download}\n' https://test.openspecimen.org/</code>

<h2>Uploading Files:</h2>
<h4>Multiple Files Upload:</h4>
<code>curl -F "file1=@/path/to/file1" -F "file2=@/path/to/file2" <URL></code>

<h4>Single File Upload:</h4>
<code>curl -F "file=@/path/to/file" <URL></code>

<h4>Uploading File with Description:</h4>
<code>curl -F "file=@/path/to/file" -F "description=This is a description" <URL></code>

<h2>CRUD Operations:</h2>
<h4>Reading Data (GET):</h4>
<code>curl -X GET https://api.example.com/data</code>

<h4>Creating Data (POST):</h4>
<code>curl -X POST -d "param1=value1&param2=value2" https://api.example.com/data</code>

<h4>Updating Data (PUT):</h4>
<code>curl -X PUT -d "param1=value1&param2=value2" https://api.example.com/data/123</code>

<h4>Deleting Data (DELETE):</h4>
<code>curl -X DELETE https://api.example.com/data/123</code>
