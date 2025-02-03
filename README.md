# gmgn.ai-api
API information about gmgn.ai
<br></br>

# General Information
[gmgn.ai](https://gmgn.ai) has cloudflare protection, for python projects you can use [cloudscraper](https://github.com/VeNoMouS/cloudscraper)

For other languages, check out my own project [cloudscraper-server](https://github.com/GhostTypes/cloudscraper-server) which is a local proxy server for easy use in other projects.

<br></br>
# Required Headers
```
def get_headers(address: str = "None"):
    headers = {
        'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/120.0.0.0 Safari/537.36',
        'Accept': 'application/json, text/plain, */*',
        'Accept-Language': 'en-US,en;q=0.9',
        'Accept-Encoding': 'gzip, deflate, br',
        'Origin': 'https://gmgn.ai',
        'Referer': f'https://gmgn.ai/sol/token/{address}',
        'Sec-Ch-Ua': '"Not_A Brand";v="8", "Chromium";v="120", "Google Chrome";v="120"',
        'Sec-Ch-Ua-Mobile': '?0',
        'Sec-Ch-Ua-Platform': '"Windows"',
        'Sec-Fetch-Dest': 'empty',
        'Sec-Fetch-Mode': 'cors',
        'Sec-Fetch-Site': 'same-origin',
        'Connection': 'keep-alive'
    }
    if address == "None":
        headers['Referer'] = "https://gmgn.ai"
    return headers
```