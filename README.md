# mypackages

# Psush a image to github Packages (GHCR)
1. Create an image

docker build -t hello .
 docker run hello
 docker tag hello ghcr.io/<githubusername>/<image>:latest

2. Create (PAT) on Github --give r-w accesss to 

'''
value
'''

3. Authenricate  GH container Registry (GHCR)

'''
export CR_PAT=<TOKEN>
echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin

'''
then

4. tag and push our image to GHCR

docker push ghcr.io/<githubusername>/<image>:latest

# Use Github Actions to Publish a Docker image to Github Packages (GHCR)