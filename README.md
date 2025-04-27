# book_recommender

data_set -> 7K books from kaggle

steps:
  1.Prepare text data
  2.Vector search
  3.Text classification
  4.Sentiment analysis
  5.Gradio dashboard

How I built it:

I used Hugging Face sentence embeddings to convert over 5,000 book descriptions into vector space.

Stored them in ChromaDB, which allows semantic search using vector similarity.

Then I used LangChain to parse and route user queries — especially when users say things like “I want something dark and philosophical”. LangChain helps bridge the user prompt to embedding search.

On top, I built a Gradio UI where users can filter by emotion and genre. It dynamically updates results based on the filters.

Results:

The system achieved 90%+ relevance in internal evaluations (based on user prompts and manual checks).

It’s modular and scalable — I could easily plug in more books or switch to other domains like movies or podcasts.
