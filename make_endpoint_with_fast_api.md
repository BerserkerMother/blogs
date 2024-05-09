# Creating a FastAPI Endpoint to Say Hello World

**Date:** 2024-05-09  
**Author:** Kave Bahraman  

In this tutorial, we'll create a simple FastAPI application that exposes an endpoint to say "Hello, World!".

## Prerequisites

Before we begin, ensure you have Python and FastAPI installed on your system. You can install FastAPI using pip:

```bash
pip install fastapi
```

## Step 1: Import FastAPI

First, let's create a new Python file, for example, `main.py`, and import the necessary modules:

```python
from fastapi import FastAPI
```

## Step 2: Create an Instance of FastAPI

Next, let's create an instance of the `FastAPI` class:

```python
app = FastAPI()
```

## Step 3: Define a Hello World Endpoint

Now, let's define a route for our endpoint using a Python decorator:

```python
@app.get("/")
def read_root():
    return {"message": "Hello, World!"}
```

Here, `@app.get("/")` creates a route for the root URL ("/"), and `def read_root():` defines the function that will be executed when this route is accessed.

## Step 4: Run the Application

Finally, let's run our FastAPI application. Add the following code at the end of your `main.py` file:

```python
if __name__ == "__main__":
    import uvicorn
    uvicorn.run(app, host="0.0.0.0", port=8000)
```

This code starts a development server using Uvicorn.

## Step 5: Test the Endpoint

Now that our application is running, open a web browser or use a tool like cURL to access the endpoint:

```bash
curl http://localhost:8000/
```

You should see a JSON response containing our "Hello, World!" message:

```json
{"message": "Hello, World!"}
```

Congratulations! You've successfully created a FastAPI application with an endpoint to say "Hello, World!".

