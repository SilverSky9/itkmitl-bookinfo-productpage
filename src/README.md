# How to run product page

## Prerequisite

* Python 3.8

```bash
pip install -r requirements.txt
python productpage.py 9080
```

```bash
# Build docker productpage service
docker build -t productpage $(pwd)/itkmitl-bookinfo-productpage

# Run productpage service
docker run -d --name productpage-service --rm -p 8083:9080 --link details-service:details-service --link ratings-service:ratings-service --link review-service:review-service  -e 'DETAILS_HOSTNAME=http://details-service:9080' -e 'RATINGS_HOSTNAME=http://ratings-service:8080' -e 'REVIEWS_HOSTNAME=http://review-service:9080' productpage
```
