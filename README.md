Start digdag server.
```
docker-compose down 
docker-compose build
docker-compose up -d
```

Upload tarball(using GNU tar) to digdag server. 
```
docker run -v ${PWD}/project:/project -w /project ubuntu:18.04 tar zcvf project-ball.tar.gz wf.dig folder/ folder2/
digdag upload project/project-ball.tar.gz example-project -e "http://localhost:65432"
```

Check workflow files.  
[http://localhost:65432/projects/1/edit](http://localhost:65432/projects/1/edit)
