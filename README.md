# local-file-server
## A local nginx file server in a docker container
- Edit nginx.conf and compose yaml by replacing  `/path/to/folder/on/your/vm/` with actual folder to be served on the host VM
- You can change the port number too, just make sure they match in both nginx.conf and compose yaml
- Then make sure you create the folder at the path and make sure nginx.conf exists with the content at the path specified
- Next you go to coolify (if using it) and edit the service url to https://sub.custom-domain.com:{port}
- This ensures that when types in browser it will route correctly
- Finally, add a test file into the /path/to/folder/on/your/vm/, to have something like `/path/to/folder/on/your/vm/test_file.txt`
- Run `docker compose up -d` and then
- Visit  `https://sub.custom-domain.com/path/to/folder/on/your/vm/test_file.txt` and you should see the content served
