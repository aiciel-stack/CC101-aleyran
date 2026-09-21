# Mission Reflection

1. Why is object storage better suited for storing millions of photos compared to a traditional block storage
hard drive?

Object storage is better suited for millions of photos than a traditional block storage hard drive because it scales almost without limit and is not tied to a single server or disk. Block storage is attached to one machine and limited by its capacity, while object storage keeps each photo as an object with its own unique ID and metadata in a flat structure that can be retrieved over HTTP. It is also more cost-effective for large amounts of unstructured data.

2. How did using Docker make it easier to deploy the MinIO storage server?
 
Docker made deploying MinIO much easier. Instead of downloading files, installing dependencies, and configuring the server by hand, one docker run command pulled the image, started the server, set the login credentials, and mapped the ports in a matter of moments. It also kept MinIO isolated from the rest of the system.

3. What is a "bucket" in the context of cloud storage?

A bucket is a top-level container in cloud storage that holds objects. It works like a uniquely named folder, although it is flat rather than hierarchical, and it is where settings and access permissions can be applied. In this lab, the client-photos bucket held my uploaded test file.

4. How do you think large enterprise companies ensure their object storage data is not lost if the physical
server crashes?

I think large enterprise companies protect their object storage data from server crashes through redundancy. They replicate data across multiple drives, servers, and even data centers, so if one fails, another copy is still available. Techniques such as erasure coding split data into pieces with extra parity so lost pieces can be rebuilt, and regular backups add another layer of protection.

5. How is your confidence in navigating the Linux command line growing?

My confidence with the Linux command line is growing. Commands like docker run, docker ps, and docker logs felt unfamiliar at first, but after Labs 4 and 5 I can type them more accurately and read the output to tell whether something worked. I am becoming more comfortable troubleshooting and understanding what each flag does.
