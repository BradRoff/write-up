In this lab, I will demonstrate encrypting and decrypting a created file in kali linux linux using symmetric encryption and AES.
<details><summary>creating the file I’m going to encrypt</summary>
I begin by using the following command:
	
```bash echo "This is a sample file for AES encryption lab." > test_file.txt ```
	<details><summary>Code explanation</summary>
	```bash echo``` outputs a string of text.
	```bash '>' ``` Redirects the new string of text to the file named test_file.txt
	</details>
</details>

<details><summary>Generating a Secret Key</summary>
	I then get a random 256-bit (32-byte) key for the AES generation:
	
	```bash openssl rand -base64 32 > aes_key.bin```
&nbsp;
	<details><summary>Code explanation:</summary>
	```bash openssl rand``` uses openssl command line tool to generate random number
	```bash base64``` encodes random number into base64 format
	```bash 32``` will generate 32 bytes or 256 bits
	</details>
</details>

<details><summary>Encrypting the file using the generated AES key</summary>
I then use the following command to encrypt the file, however the encryption seems outdated. While it would still work I will reencrypt as suggested in the warning for more security.


```
bashopenssl enc -aes-256-cbc -salt -in test_file.txt -out encrypted_file.bin -pass file:aes_key.bin
WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
```

&nbsp;
	<details><summary>Code explanation</summary>
	```bash openssl enc```: OpenSSL’s symmetric encryption utility.
	```-aes-256-cbc```: Specifies the AES algorithm with 256-bit encryption in CBC mode
	```salt```: adds a random value or salt to the key.
	```-pass file``` uses generated key from aes_key.bin
	</details>
</details>
<details><summary>Inproving Encryption</summary>
I then encrypted the file with pbkdf2 and iter for increased security.

	```bash
 	openssl enc -aes-256-cbc -salt -in test_file.txt -out encrypted_file.bin -pass file:aes_key.bin -iter 10000

 	’’’

 &nbsp;
 	<details><summary>Code explanation</summary>
	
 	
  ```-pbkdf2```: Specifies use of Password-Based Key Derivation Function 2.
```-iter 100000```: Specifies the number of iterations of the PBKDF2 key derivation function, in this case 100,000 times. Helpful vs brute force attacks.	</details>
</details>
<details><summary>Checking if file is encrypted</summary>
Now we can check if the file is encrypted by 'cat' ing the file.

```
bashcat encrypted_file.bin
 Salted__�#3�r�Ո�TN��H
```
</details>
<details><summary>Decrypting the file.</summary>
To decrypt the file, I use the following command. Only difference is adding the new -out destination and the variable for decryption.

`bashopenssl enc -d -aes-256-cbc -salt -in encrypted_file.bin -out decrypted_file.txt -pass file:aes_key.bin -iter 10000`
	<details><summary>Code explanation</summary>
	```bash-d``` indicates that you want to <b>d</b>ecrypt the file instead of encrypting it.
</details>
<h3>Summary</h3>
<p>Going through this lab was useful. I find it helpful to break down the lines by code bit by bit. It’s amazing seeing how far encryption has evolved over the years.
