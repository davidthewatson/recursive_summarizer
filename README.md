# Recursive Summarizer

This is a basic implementation of a recursive summarizer using openai, GPT-3, and requests-html to crawl, parse, and summarize text of any length by chunk.

The usual instructions apply: lin, mac, or win + [python 3](https://docs.python.org/3.11/whatsnew/3.11.html). Then:

    python -m venv .venv
    source .venv/bin/activate{.fish} # or whatever shell you're using today
    pip install -r requirements.txt

The only thing missing is that you have to [get an OPENAI API Key](https://beta.openai.com/account/api-keys) and place it in a .env file as follows: 
     ╭─watson@acer in repo: recursive_summarizer on  main [!] via  v3.10.8 (.venv) took 14ms
     ╰─λ cat .env
     File: .env

    export OPENAI_API_KEY="YOUR_KEY_GOES_HERE"

After that, just adjust the crawling frontier URLs in the source to your liking. Mine is tuned for my custom CMS system that I wrote from scratch. 

It starts with an index of content for which this crawler is designed to limit it's crawl to the corpus of text cascading from that index. It's generally easy to edit the filter to limit the crawl by keyword or whatever. 

This is not scrapy, it's a quick weekend hack.

