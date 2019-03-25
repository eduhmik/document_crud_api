# document_crud_api
A simple nodeJS crud api built using express and mongo db. The api is deployed on a docker container and uses mongo client as the object document mapping (ODM) tool.

# How to run this application.

- git clone `https://github.com/eduhmik/document_crud_api.git`

- install all one node dependencies `yarn`

- build project using `yarn run build`

- then run the command `yarn run production`

- Once those have completed you can run `docker ps` to show all running containers which should show your MongoDB container and a container named `docker_backend`

- From you terminal, you can now run `curl localhost:80/api/documents/all` which should return
`{“error": “No documents in database"}`.

- You can add a new document from postman by using: `localhost:80/api/documents/new`

        ```payload:
            {
	            "title": "New doc",
	            "username": "eduhmik",
	            "body": "this is a test document"
            }```

- You can get a single document from postman by using: `localhost:80/api/documents/:id`

- You can edit a document from postman by using: `localhost:80/api/documents/edit/:id`

        ```payload:
                {
                    "title": "Edited doc",
                    "username": "eduhmik",
                    "body": "this is a edited document"
                }```

- You can delete a document from postman by using: `localhost:80/api/documents/delete/:id`

