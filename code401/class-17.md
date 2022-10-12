# Class 17 - AWS: S3 and Lambda

## AWS S3

### What is Amazon S3?

Amazon S3 is a serverless cloud storage solution.

### Name some use cases for Amazon S3.  

S3 can be used for storing data backups/archives. It can also be used to store application files to be able to quickly spin up builds of an app.

### Name some benefits of using Amazon S3.

S3 has high availability and durability, and scales with your data. It also uses AWS access controls, so access to data/files can be controlled at a granular level.

## AWS Lambda

### What is AWS Lambda?

AWS Lambda is a service that allows for running code in a serverless environment. With Lambda, a developer can write code without worrying about running a server or configuring network settings.

### Name some use cases for AWS Lambdas.

Processing images - When an image is added to a bucket, Lambda can be triggered to run code that will convert the image into multiple sizes, such as a mobile-friendly and a desktop-friendly size.

### Describe “serverless” to a non-technical friend.

Think of serverless as simply meaning "I don't have to worry about where a thing happens." Take something like Google Drive, for example. When you drop an image or a document into a Drive folder, you don't need to specificy *where* that file is going to live.

Somewhere, servers exist and have your file stored on them. But you aren't responsible for managing which server it lives on, or how that file gets retrieved when you want to download it or share it. It exists, and there are ways to interact with it, and that's really all you as the user need to know.

That's what serverless does for developers, as well. It gives us a way to perform actions, store data, or interact with things without worrying about a server.

## CDN

### What is a CDN?
A CDN refers to a group of servers that provide quick delivery of content by geographically distributing the servers across a wide area. This allows users to quickly transfer data from the Internet, particularly things like HTML pages, JS files, images, and videos.

### How does a CDN work with relation to the website visitor?
Typically, the server closest to the website visitor will respond to the request for content. This often means first connecting to an originating server and being redirected to the nearer server within the CDN.
### What are the benefits of employing a CDN?
Servers on a CDN are able to cache data being used. Think of a video streaming service. They may have a CDN with servers in Oregon, New York, and Mumbai. The videos that often are watched in Mumbai may be very different from the videos that get watched in New York, so a CDN may be able to only cache the data necessary for its nearest userbase. If it doesn't have the data that a user wants, it can reach out to another server, or perhaps a main cluster of servers, and request that data, deciding later whether or not to cache it.