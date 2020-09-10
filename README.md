# File Provider Web Server
Web server with two features
- text content upload using http post
- text content download using http get

## Build and run the web server
Web server is dockerized and can be easily build and run using the following way:
```
docker-compose build
docker-compose up
```

## Use the web server
The file content upload form is available on this link: [http://localhost:5080/fileprovider](http://localhost:5080/fileprovider)

### Upload the file content
File content can be uploaded by submitting the html form.
Another option is to use the `curl` command:
```
curl -s --location --request POST 'http://localhost:5080/fileprovider' \
--form 'fileContent={"key":"value"}'
```

### Get the file content
File content can be obtained by the following get request:
```
curl -s --location --request GET 'http://localhost:5080/fileprovider/fileContent'
```

## Shut down the web server
Run the following command to shut down the web server:
```
docker-compose down
```
