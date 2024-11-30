# Digital_Signatures
It consists of two files: Sign and Authentication.

*In the Sign file, the main functions are:

1. Generate RSA Keys: Automatically generates a public-private key pair (RSA) if the private_key.pem and public_key.pem files do not exist. The private key is used for signing, while the public key is used for verification.

2. Sign files: Reads the content of each file in the directory. Signs the file using the private key (RSA) with the SHA-256 hash algorithm and PSS padding. Saves the original content and the signature (separated by ---SIGNATURE---) back into the file.

3. User Interface (Tkinter): A button allows the user to select a folder and sign all files within that folder. Displays the sign results (file name + signature) in the interface window.

4. Application: Ensures data integrity. Verifies the source. Used in: document storage, digital contracts, etc. Uses RSA with SHA-256.

*In the Authenticate file, the main functions are:

1. Verify file signatures: The code reads the public key (public_key.pem) and uses RSA with SHA-256 to verify the digital signature in the files. The verify_files(directory) function checks all files in the selected directory and verifies the digital signatures. If the signature is valid, it shows a success result; otherwise, it displays an error.

2. Read signature from file: The read_binary_signature(file_path) function looks for and reads the digital signature from the file (if available).

3. User Interface with Tkinter: The interface is built with the Tkinter library, providing buttons for the user to select a folder or file and display the verification result or signature. Interface buttons: Select folder, read signature from file.

4. Display Results: The signature verification results or signature information will be shown in a text window (Text widget).

