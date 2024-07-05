
# Steganography Project

## Introduction

This project focuses on steganography, the practice of concealing messages or information within other non-secret text or data. The goal of this project is to explore the methods and techniques used in steganography and to create a simple steganography tool using `stegseek` and the `rockyou.txt` wordlist.

## Features

- **Message Embedding:** Hide a secret message within an image.
- **Message Extraction:** Extract the hidden message from the image.
- **Brute-Force Password Cracking:** Use `stegseek` with the `rockyou.txt` wordlist to find passwords for hidden messages.
- **Supported Formats:** Works with common image formats like PNG and JPEG.
- **User-Friendly Interface:** Simple command-line interface for embedding and extracting messages.

## Getting Started

### Prerequisites

- `stegseek` tool
- `rockyou.txt` wordlist

### Installation

1. Clone the repository:
git clone https://github.com/your-username/steganography-project.git
cd steganography-project


2. Ensure you have `stegseek` installed. You can find installation instructions [here](https://github.com/RickdeJager/stegseek).

3. Download the `rockyou.txt` wordlist if you don't already have it. It's available [here](https://github.com/praetorian-inc/Hob0Rules/blob/master/wordlists/rockyou.txt.gz).

### Usage

#### Embedding a Message

To embed a message in an image using `steghide`, use the following command:
steghide embed -cf <input_image> -ef <message_file> -sf <output_image>

- `<input_image>`: The path to the image in which you want to hide the message.
- `<message_file>`: The path to the file containing the message you want to hide.
- `<output_image>`: The path to save the new image with the hidden message.

#### Extracting a Message

To extract a message from an image using `stegseek` with the `rockyou.txt` wordlist, use the following command:
stegseek <input_image> rockyou.txt

- `<input_image>`: The path to the image from which you want to extract the hidden message.
- `rockyou.txt`: The wordlist to use for brute-forcing the password.

## Example

Here is an example of how to embed and extract a message:

1. Embed the message:
steghide embed -cf example.png -ef message.txt -sf secret.png

2. Extract the message:
stegseek secret.png rockyou.txt

The output will display the hidden message and the password used (if any).

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by the fascinating world of steganography.
- Special thanks to the open-source community for their invaluable resources and support.
- Thanks to `stegseek` and `rockyou.txt` for making password recovery possible.


This version includes the specific tools you used (`stegseek` and `rockyou.txt`) and provides instructions for embedding and extracting messages with these tools. Let me know if you need any further adjustments!
