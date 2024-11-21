Here’s the updated `README.md` to reflect the tool's name `image_encdec.py`:

```markdown
# Image EncDec Tool

This project is a simple **Image Encryption and Decryption Tool** built with Python. It allows users to encrypt and decrypt images using a random seed value. The encryption and decryption are performed by scrambling pixel values based on a user-provided seed.

## Features

- **Encrypt Images**: Scramble the pixels of an image using a random seed to create an encrypted version.
- **Decrypt Images**: Restore the original image using the same seed that was used for encryption.
- **GUI Interface**: Built with `Tkinter`, providing a simple and intuitive user interface.
- **Seed-based Encryption**: The use of a seed allows for reproducible encryption and decryption.

## Installation

### Requirements

- **Python 3.6+**
- **Pillow**: A Python Imaging Library (PIL) fork.
- **Tkinter**: A standard Python library for creating GUI applications (usually included with Python).
  
### Install Dependencies

Make sure you have `Pillow` installed:

```bash
pip install Pillow
```

### Clone the Repository

```bash
git clone https://github.com/Adityannn/PRODIGY_CS_02.git
cd PRODIGY_CS_02
```

## Usage

### Running the Tool

To run the image encryption tool, simply execute the script:

```bash
python image_encdec.py
```

### How to Use

1. **Open the Application**.
2. **Select an Image**: Click "Browse" to choose an image for encryption or decryption.
3. **Choose Output Path**: Click "Save As" to select where the processed image will be saved.
4. **Enter a Seed Key**: This key is used for encryption/decryption. Remember the seed used for encryption, as it is required to decrypt the image.
5. **Encrypt or Decrypt**: Click the respective button to perform the operation.

## Project Structure

```plaintext
image-encdec-tool/
├── image_encdec.py           # Main script for the Image Encryption and Decryption Tool
├── README.md                 # Project documentation
└── requirements.txt          # Dependencies (if any)
```

## Code Explanation

The code leverages a seeded random number generator to shuffle the pixel indices of an image during encryption. The same seed can be used to reverse the process during decryption.

### Key Functions

- **encrypt_image(input_image_path, output_image_path, seed)**: Encrypts the image by scrambling pixels.
- **decrypt_image(input_image_path, output_image_path, seed)**: Decrypts the image by reversing the scrambling process.
- **get_seeded_random(seed)**: Returns a seeded random generator for consistent scrambling.
