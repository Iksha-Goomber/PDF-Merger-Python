# PDF-Merger-Python
# The PDF Merger is a Python tool that combines multiple PDF files into a single document, making file management simple and efficient.
# https://pypdf2.readthedocs.io/en/3.x/
from PyPDF2 import PdfWriter

merger = PdfWriter()

pdfs = []
n = int(input("How many PDFs do you want to merge?\n"))

for i in range(0, n):
    name = input(f"Enter the name of PDF {i + 1}: ")
    pdfs.append(name)

for pdf in pdfs:
    merger.append(pdf)

merger.write("merged-pdf.pdf")
merger.close()
