# mypackages

# Psush a image to github Packages (GHCR)
1. Create an image

 docker build -t hello .
 docker run hello
 docker tag hello ghcr.io/ayeshaaayub/hello:latest

2. Create personal Access Token (PAT) on Github --give r-w accesss to 

'''
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
'''

3. Authenricate  GH container Registry (GHCR)

'''
export CR_PAT=<TOKEN>
echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin
'''
then

docker push ghcr.io/ayeshaaayub/hello:latest


4. tag and push our image to GHCR
# Use Github Actions to Publish a Docker image to Github Packages (GHCR)