### Overview
Cloud Computing !!

back in time, companies were using thier own private servers to create services for storage. But now with the internet speeds becoming better, companies started understanding the power of cloud, therefore they are shifting thier data to the cloud for improved perfomance.

> **For example,** Netflix is a popular video streaming service which the whole world uses today, back in 2008 Netflix suffered a major database corruption, and for three days their operations were down. The problem was scaling, that is when they realized the need for a highly reliable, horizontally scalable, distributed systems in the cloud. Came in AWS, and since then their growth has been off the charts.

## What's AWS? 
Amazon web service (AWS) is an subCompany from Amazon which offers cloud computing services.

## Cloud Computing 
Cloud computing is the delivery of  it resources over the internet.
The cloud is like a virtual data center accessible via the internet that allows you to manage:
   1. Storing service like databases.
   2. Servers, compute power, networking.
   3. Analystics, Artificial inteligence,... etc.
   4. Security services for data and application.

## Chraacteristics for cloud computing.
1. **Pay as you go (PAYG):** you pay only for what you use and only when your code runs.
   - One major benefit of the PAYG method is that there are no wasted resources, since users pay only for services procured.
3. **AutoScalling:** the number of active servers can grow or shrink based on demand 
4. **Serverless:** Allow you to write and deploy code without having to worry about the underlying infrastructure.

## Types of Cloud Computing (As-a-Service).
"As-a-Service" generally means a cloud computing services that is provided by a third party so that you can foucs on what's more important to you.
![This is an image](https://www.redhat.com/cms/managed-files/iaas-paas-saas-diagram5.1-1638x1046.png)
1. **Infrastructure as a service (Iaas)**
   - The provider supplies virtual server instances, storage and machanism for you to manage servers
3. **Platform as a service (Paas)**
   - A platform of development tools hosted on a providers infrastructure
5. **Software as a service (Saas)**
   - a software application that runs over the internet and managed by the service provider.

For more details read this [IaaS vs PaaS vs SaaS](https://www.redhat.com/en/topics/cloud-computing/iaas-vs-paas-vs-saas?sc_cid=7013a000002pgROAAY&gclid=Cj0KCQjworiXBhDJARIsAMuzAuwcipV0OoImXC7GBN5C9qWxacTejgHzQZlK_WULlPFpEuxW8Mx2hYoaAvA8EALw_wcB&gclsrc=aw.ds)


## Cloud Deployment method

1. **Public Cloud**
   - a public cloud makes resources available over the internet to the general public 
3. **private Cloud**
   - a private cloud is a private network that supplies services to a limited number of people.
5. **Hybrid Cloud**
   - A hybird cloud models contains a combination of both a public & private cloud 
   - The hybrid model is a growing trend is the industry for those organization that have been slow to adapt the cloud due to being in heavily regulated industary
   - The hybird model gives the organiztion the flexibility to slowly migrate to the cloud.
 
 ### Benefits
 1. Stop gussing about capacity.
 2. Avoid huge Capital investments up front.
 3. Pay for only what you use.
 4. Scale globally in minutes.
 5. Deliver faster.
 
 - ![Public Cloud](https://www.spiceworks.com/tech/cloud/articles/what-is-public-cloud/#_002)
 - ![Private Cloud](https://www.spiceworks.com/tech/cloud/articles/what-is-private-cloud-storage/)
 - ![Hybird Cloud](https://www.spiceworks.com/tech/cloud/articles/what-is-hybrid-cloud/)

## Cloud infrastructure
1. Region
   - A region is considered as geographic location or an area on a map 
2. Availablity zone
   - An Availablity zone is an isolated location within a geographic region and is a physical data center with a specific region.
3. Edge location
   - An Edge Location is a mini-data center used solely to cache large data files closer to a user location.

### Additional Information 
- There are more avaliablity zones (AZs) tha there are regions.
- There's Should be at least two AZs per region.
- Each region is located in a sperate geographic area.
- AZs are distinct locations that are engineered to be isolated from failures.


### Shared Responsiblity model.
- AWS is responsible for sercurity of the cloud.
- We are responsible for security on the cloud.

#### Examples
##### AWS is responsible for :
- Security edge location.
- Monitoring physical device security.
- Providing physical access control to hardware/software.
- Database patching.
- Discarding physical storage devices.

##### we are responsible for :
- Managing AWS Identity and Access Management (IAM).
- Encrypting data.
- Preventing or detecting when an AWS account has been compromised.
- Restricting access to AWS services to only those users who need it.
