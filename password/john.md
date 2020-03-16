# Identify
hash-identifier
hashid

# PDF
Extract the password hash from the PDF
/usr/local/share/john/pdf2john.py pdfpassword.pdf > pdf.txt

john --session=pdf --format=PDF pdf.txt

