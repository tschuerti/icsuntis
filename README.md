<p align="center">
  <img src="https://raw.githubusercontent.com/tschuerti/icsuntis/refs/heads/main/logo.png" />
</p>

ICSUntis is a simple JavaScript server that generates an ICS file from your WebUntis substitution plan. It is designed to be run on a server and can be accessed via a simple HTTP GET request.

## Usage

To use ICSUntis, you need to know the URL of your WebUntis server. You can find the server by logging into WebUntis and looking at the URL. It should look something like this:

```http
https://<server>.webuntis.com/
```

To get your school's short name, you can press on the RSS-Feed button in the WebUntis substitution plan. The URL should look something like this:
    
```http
https://<server>.webuntis.com/WebUntis/NewsFeed.do?school=<school>
```

To generate an ICS file, you need to make a GET request to the ICSUntis server with the following parameters:

- `server`: The full URL of your WebUntis server (including .webuntis.com if it isnt running on a custom domain)
- `school`: The short name of your school in WebUntis
- `username`: Your WebUntis username
- `password`: Your WebUntis password

Here is an example of a GET request:

```http
http://<your-server-adress>:3000?server=<server>.webuntis.com&school=<school>&username=<username>&password=<password>
```

<h3 align="center">Have fun using ICSUntis!🙂</p>