# To create Secret 
`kubectl create secret generic user --from-file=./username.txt`
`kubectl create secret generic pswd --from-file=./password.txt`

# To see details of secret
`kubectl describe secret pswd`
