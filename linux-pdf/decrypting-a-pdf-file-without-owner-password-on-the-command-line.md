# Decrypting a PDF file without OWNER password on the command line

Briefly, a secured PDF file has two types of password: OWNER and USER.
<br />
The OWNER password is used to enforce permissions. The USER password is used to open the pdf file.
<br />
<br />
Sometimes, downloaded pdf (such as your bank statements) are secured/encrypted by default. We can decrypt this even without OWNER password using qpdf.
<br />
<br />
1. Make sure qpdf is installed, on Debian-based systems: `sudo apt-get install qpdf`
1. Run `qpdf --decrypt <source pdf> <destination pdf>`
<br />
<br />
You can decrypt it if it's secured with a USER password as well, but you need to know the password.
