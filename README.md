# ERROR: FULL SCOPED PAT IS RESTRICTED BY YOUR ORGANISATION

Greetings my fellow Technology Advocates and Specialists.

In this Troubleshooting Session, I will demonstrate, how I resolved the encountered error - "__Full Scoped PAT is restricted by your Organisation__".

One day, in hour of need, I encountered the above error, when I tried creating a full scoped PAT (Personal Access Token) in my DevOps Organisation.  

Details of my DevOps Organisation follows below:-

| __KEY__ | __VALUE__ |
| --------- | --------- |
| __DevOps Organisation URL__ | https://dev.azure.com/AM0704 |
| __DevOps Organisation Owner__ | AM@mitra008.onmicrosoft.com |
| __DevOps Project__ | AMCLOUD |
| __DevOps Service Connection__ | amcloud-cicd-service-connection |

Generate a Full Scoped PAT in DevOps Organisation:-

| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zkeotews1onzv6mngl3f.jpg) |
| --------- |
| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ou1z3cmamyunctmlk1e1.jpg) |

Below is how the error looks like with "__Full Access__" Scope option greyed out:-

| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/fd1mtn07impw8u10vy02.jpg) |
| --------- |

The User Account/Identity in reference is:-

1. Owner of DevOps Organisation.
2. Global Administrator of the Directory.

| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rajg9pzjqqqeghfmtrax.jpg) |
| --------- |
| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ar3fwuxq8g6h94nv5ao0.jpg) |

Also, DevOps Organisation policies __CANNOT__ be viewed from the same User Account/Identity:-

| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/sojcyomhxvdszp8dfdr5.jpg) |
| --------- |

When referred to Microsoft documentation [Use policies to manage personal access tokens for users](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/manage-pats-with-policies-for-administrators?view=azure-devops), it clearly states that the User Account/Identity must be an __"Azure DevOps Administrator"__ in Azure AD to manage DevOps Organisation Policies.

| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/y9nuysly3ht7bisqqd6i.jpg) |
| --------- |

We now proceed to Assign __"Azure DevOps Administrator"__ Role to the reference User Account/Identity:-

| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ym6e3cx6zpee7violb4u.jpg) |
| --------- |
| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ihp3lq8tev9qol3usny6.jpg) |
| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/v7p7raehs0xs4wi054z2.jpg) |
| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jeupt1w3aykbj62hzofi.jpg) |

As observed, 
1. We are able to successfully view the DevOps Organisation policies using the same reference User Account/Identity. 

2. The Policy __"Restrict full-scoped personal access token creation"__ is enabled with __No users in allow list__. Hence the above error.

| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/wji7qjomq3crfz1vu0r5.jpg) |
| --------- |

In order to be able to create Full Scope PAT, below actions should be taken:-

1. Keep the Policy enabled but add one or more User account/Identity in the allow list; __OR__
2. Disable the Policy.

| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/udp8gz29sr09f6jxabqo.jpg) |
| --------- |
| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ycvsxpn2ydoslxsto3h4.jpg) |

In both cases, User will be allowed to create Full Scoped PAT.

| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/sb74dqz10jq3te4qz53r.jpg) |
| --------- |


__Hope You Enjoyed the Session!!!__

__Stay Safe | Keep Learning | Spread Knowledge__
