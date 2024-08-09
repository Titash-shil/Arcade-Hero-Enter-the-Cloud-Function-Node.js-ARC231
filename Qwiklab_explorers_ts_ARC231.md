# Arcade Hero: Enter the Cloud Function Node.js || [ARC231](https://www.cloudskillsboost.google/focuses/98840?catalog_rank=%7B%22rank%22%3A1%2C%22num_filters%22%3A0%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=34929288) ||

# # Like, comment, share & Don't forget to subscribe [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN) 👍😄🤝

### Run the following Commands in CloudShell

```
export REGION=
```
```
gcloud config set compute/region $REGION
export PROJECT_ID=$(gcloud config get-value project)


mkdir quicklab && cd quicklab

cat > index.js <<'EOF_END'
const functions = require('@google-cloud/functions-framework');

// Register an HTTP function with the Functions Framework that will be executed
// when you make an HTTP request to the deployed function's endpoint.
functions.http('helloGET', (req, res) => {
  res.send('Subscribe to Quicklab!');
});
EOF_END

cat > package.json <<EOF_END
"dependencies": {
  "@google-cloud/functions-framework": "^3.1.0"
}

EOF_END

gcloud functions deploy cf-demo \
  --gen2 \
  --runtime=nodejs20 \
  --region=$REGION \
  --source=. \
  --entry-point=helloGET \
  --trigger-http \
  --allow-unauthenticated \
  --quiet

```

# Congratulations ..!!🎉  You completed the lab shortly..😃💯

# *Well done..!* 👏

# Thank you for visiting.... :) 🗯️

# [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN)
