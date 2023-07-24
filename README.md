# PDFAgent

Most accurate, production-ready PDF agent for reading, analysing and conversing with your PDF.

# Features

✅ Production-ready PDFReaderAgent - built with Rest API (see docs.twilix.io for more information)
✅ Built-in observability (via Twilix dashboard)  
✅ Built-in easily swappable read/write API keys (so no one can over-write your data)  
✅ Production-ready insertion and retrieval pipelines built in (via Twilix)  
✅ Multi-line citations, references built out of the box.  


## Installation

You can install it easily using the following: 

```bash
pip install pdfagent
```

## QuickStart

You can get started quickly by grabbing your API key from https://app.twilix.io/.

```python
from pdfagent import PDFAgent
agent = PDFAgent(
    api_key="XXX"
)
```

### Inserting a PDF 

You can insert a PDF in just 1 line of code - under the hood, we take care of OCR, preprocessing,
vectorising, splitting and storage.

```python
agent.insert_pdf(
    "https://www.w3.org/WAI/WCAG21/working-examples/pdf-table/table.pdf"
)
```

Once it's inserted, we recommend giving it 1 or 2 minutes to properly index.

## Now ask it questions!

```python
agent.ask("What is this PDF about?")
```

## Ask for a co-pilot analysis!

```python
agent.ask("How many participants are there in total?")
```

## Powerful templating for any desired output:

You can then use out-of-the-box templating such as from the following:

```python
agent.template("""Please summarise the information below:

{reference}
HTML:""")
```
