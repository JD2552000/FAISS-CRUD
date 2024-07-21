# FAISS-CRUD
Implement CRUD operations with fails-python

FAISS (Facebook AI Similarity Search) is a library that allows developers to quickly search for embeddings of multimedia documents that are similar to each other.

Install FAISS:
import faiss
import numpy as np

# Initialize the FAISS index
dimension = 384 #we can keep it as per our requirements
index = faiss.IndexFlatL2(dimension)  # Using L2 distance

#Install all requirement using 
pip install -r requirements.txt

Run below command to run the python app
uvicorn main:app --reload
 
Method: POST API
URL: http://127.0.0.1:8000/create/
Body:
json
{
  "text": "This is an example sentence."
}

Method: GET API
URL: http://127.0.0.1:8000/read/{item_id}

Method: PUT API
URL: http://127.0.0.1:8000/update/{item_id}
Body:
json
{
  "text": "This is an updated sentence."
}

Method: DELETE API
URL: http://127.0.0.1:8000/delete/{item_id}
