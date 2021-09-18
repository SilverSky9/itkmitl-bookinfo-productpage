# How to run product page

## Prerequisite

* Python 3.8

```bash
pip install -r requirements.txt
python productpage.py 9080
```

```bash
# Build docker 
docker build -t productpage .

# Run docker
docker run -d --rm -p 8084:9080 productpage
```
