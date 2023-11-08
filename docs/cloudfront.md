# CloudFront

## Overview

- Content Distribution Network (CDN)
    + Distributed network of servers which delivers web pages and content to users based on their geographical location, the origin of the webpage and a content delivery server
    + Used to deliver an entire website (static, dynamic and streaming content)
    + Request are served from the nearest Edge Location for the best possible performance
- Creates cached copies of yout website at various Edge Locations around the world

## Core concepts

- Origin: Location where all of original files are located
- Distribution: Collection of edge locations
    + Edge locations: AWS data centers designed to deliver services with the lowest latency possible
    + Specified origins (S3, EC2, ELB, Route 53)
    + Replicates copies based on your Price Class (define replica regions)
    + Behaviours (redirections, restrict access, TTLs), cache invalidations, error pages, geolocation restrictions
    + 2 types:
        * Web (static website content)
        * RTMP (streaming data)

## Lambda@Edge

- Use Lambda function to override the behaviour of request and responses of the origin and viewer
- There are 4 available Lambda@Edge functions (viewer <-> CloudFront <-> Origin)
    + Viewer request
    + Origin request
    + Origin response
    + Viewer response

## Protection

- OAI (legacy) & OAC: Virtual user identity that will be used to give CloudFront Distribution permission to fetch a private object.
- Signed URLs (OAI or OAC required): URL which provides temporary access to cached objects (S3 Presigned URL to S3)
- Signed Cookies (OAI or OAC required): cookie passed along with the request to CloudFront. You can provide access to multiple restricted files

![CloudFront Cheatsheet](./images.cloudfront/cloudfront.png)
