# To Create String Literal Secret
`kubectl create secret generic mysql-pswd --from-literal=password=abc@123`

# To list the Persisten volume
`kubectl get pvc`


# To encode text with base64
`echo -n <text> | base64`

# To decode text with base64
`echo -n <base64-encoded-text> | base64 -d`


# To encode file with base64
`base64 <filename>`

# To decode file with base64
`base64 -d <filename>`