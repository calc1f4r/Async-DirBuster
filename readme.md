### 🔥 Asynchronous Directory Buster

#### ⚡ Description

Asynchronous Directory Buster is a Python script that allows you to efficiently perform directory and file brute-forcing on a target website. The script leverages the power of asynchronous programming with aiohttp to perform multiple HTTP requests simultaneously, making the process faster and more efficient.

##### 💣 Key Features

- Asynchronous HTTP requests for improved speed.
- Customizable User-Agent and HTTP headers.
- Ability to follow redirects.
- Filter and match HTTP status codes.
- Filter and match response sizes.
- Output results to a file.
- Custom wordlist support.

##### 🧾 Requirements

```python
pip install aiohttp beautifulsoup4 termcolor
```

##### Usage

**📌 Basic one**

```python
python directory_buster.py -u <target_url> -w <path_to_wordlist>
```

**📌 Other examples**

_Custom Header_

```python
python directory_buster.py -u https://example.com -w wordlist.txt -H 'Authorization: Bearer token'
```

_Extensions_

```python
python directory_buster.py -u https://example.com -w wordlist.txt -x php asp
```

_Saving results to the file_

```python
python directory_buster.py -u https://example.com -w wordlist.txt -o output.txt
```

##### Supported flags

- -x <extensions>: Specify a list of file extensions to append to the directories in the wordlist (e.g., -x php asp).
- -r: Follow redirects. If this flag is set, the script will follow HTTP redirects (3xx status codes).
- -H <headers>: Specify custom HTTP headers in the format 'Header1: value1' 'Header2: value2'.
- -a <user_agent>: Set a custom User-Agent string. The default is directorybuster/1.0.
- -ht: Hide response title in output.
- -m c <status_codes>: Include status codes to match, separated by space (e.g., -m c 200 404).
- -ms <response_sizes>: Match response sizes, separated by space.
- -fc <status_codes>: Filter status codes, separated by space (default is filtering 404).
- -fs <response_sizes>: Filter response sizes, separated by space.
- -o <output_file>: Path to the output file to save the results

##### 🔴 Note

- Matching and Filtering Response Length together is not available at the moment. Choose one of them in the command-line arguments.
- Matching and Filtering Response Status Code together is not available at the moment. Choose one of them in the command-line arguments.

#### Contributions

Contributions are welcome! If you find a bug or have suggestions for improvements, feel free to open an issue or submit a pull request.

Happy directory busting🔥!
