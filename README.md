# PyReader a pdf and text file manpulating package v0.0.1:-

### PyReader will be uploaded soon to Pypi.

Now PyReader can even read both pdf and text file.

## Methods inside PyReader Read class :-

* read().
* readtxt().
* pdf_pages().
* pdf_pageNum().
* pdf_page().
* pdf_info().
* pdf_text().



#### Installing process:-

* Make sure you have python3 installed in your system.

### Run the following command in cmd to install PyReader.

    
    pip install PyReader


# Example:-

## Reading a pdf and converting to tts.

    import PyReader

    pdf = PyReader.Read('filename\location of the pdf')
    pdf.read()

## PyReader reads the first page by default , pass the page number in the read method for reading a perticular page.

    import PyReader

    pdf = PyReader.Read('filename\location of the pdf.')
    pdf.read(pageno = 10)

## Tts engine voice is default to female , pass 'm' in the read method to change the engine voice.
{m : male ,f : female}

    import PyReader

    pdf = PyReader.Read('filename\location of the pdf.')
    pdf.read(voice = 'm')

## Change the speech rate.

    import PyReader
        
    pdf = PyReader.Read('filename\location of the pdf.')
    pdf.read(speech_rate = -10)

## Save the tts as mp3.

    import PyReader

    pdf = PyReader.Read('filename\location of the pdf.')
    pdf.read(save = True)


    # saves the audio file in the current directory as pdf_audio.mp3 .


## Save and read the text from pdf.

    import PyReader

    pdf = PyReader.Read('filename\location of the pdf.')
    pdf.read(save = 'sr')


## Change default filename.

    import PyReader

    pdf = PyReader.Read('filename\location of the pdf.')
    pdf.read(save = True,filename = 'any_name.mp3')

## Extract text from pdf.

    import PyReader

    pdf = PyReader.Read('filename\location of the pdf.')
    extracted_txt = pdf.pdf_text()

    print(extracted_txt)

### PyReader extracts text from first page by default , pass the page number to extract text from a perticular page.

## Reading the text  passed in input function.

    import PyReader

    pdf = PyReader.Read()
    name = input('Enter your name :')
    pdf.readtxt(name,voice = 'm')

    """{m : male ,f : female} pass any of these to change the voice of the engine.
        defaults to female."""