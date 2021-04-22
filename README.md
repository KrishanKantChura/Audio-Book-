# Audio-Book-
If You Hate Reading Book .. Then this is the Solution for you 

import pyttsx3
import PyPDF2
book = open('power-subconscious-mind.pdf', 'rb')
pdfReader = PyPDF2.PdfFileReader(book)
pages = pdfReader.numPages
print(pages)
speaker = pyttsx3.init()
for num in range(0 , 117):
    page = pdfReader.getPage(0)
    text = page.extractText()
    speaker.say(text)
    speaker.runAndWait()
