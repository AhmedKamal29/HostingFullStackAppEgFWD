<h1>Infrastructure description</h1>

![deployment infra](https://user-images.githubusercontent.com/53512084/222455094-d09e47c3-5872-48dd-9649-e39faf1181b5.jpg)

1. User requests a specific operation
2. the s3 bucket sends the request to the api on elastic beanstalk
3. EB communicates with the database on RDS to retrieve the data requested
4. RDS responed with the data to EB 
5. EB sends the data to the s3 bucket to be displied to the cilent
6. s3 bucket display the data to the user of the frontend