DOCKER_HUB_USERNAME=amirvenkat
DOCKER_HUB_ACCESS_TOKEN=dckr_pat_aw95yYbao1eDZOQftOOh8fq1yqA

helm install kuberdemo ./helm/kuberdemo-chart


docker build -t kuberdemo:latest .   
   
docker run -p 8080:8080 kuberdemo:latest  (optional) 


docker tag kuberdemo:latest kraj28/kuberdemo:latest
docker push kraj28/kuberdemo:latest 

git init

git add . 
git commit -m "commit v1"
git push origin main


git remote add origin url
git branch -M main
git push -u origin main
