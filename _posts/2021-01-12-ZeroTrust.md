---
title: "Zero Trust in Azure Identity - A Journey"
date: 2021-01-12T10:59:57
#search: true
#classes:
#  - wide
#layout: splash
#permalink: /splash-page/
toc: true
toc_label: "In this article"
toc_sticky: true
toc_icon: "list"
# find more icons here
# https://fontawesome.com/icons?d=gallery&s=solid&m=free

categories:
- AzureAD
- Security
- Identity

tags:
- Azure Active Directory
- Identity

#header:
#   overlay_image: /MyPics/CP1_1.png
#   overlay_color: "#5e616c"
#   overlay_filter: "0.5"
#   #overlay_filter: rgba(255, 0, 0, 0.5)
#   teaser: /MyPics/CP1_1.png
   
#feature_row:
#  - image_path: /MyPics/CP_Filtergruppen.bmp
#    url: "/MyPics/CP_Filtergruppen.bmp"
#    title: "Placeholder 1"
#    excerpt: "Sample text 1 with **markdown** formatting."
#
#
#  - image_path: "/MyPics/CP_GET_Prinzipal_ID.bmp"
#    title: "Placeholder 2"
#    excerpt: "This is some sample content that goes here with **Markdown** formatting."
#    url: "#test-link"
#    btn_label: "Read More"
#    btn_class: "btn--secondar"
---

My customers often ask me: when is a user identity trustworthy? This is an important question that must be answered if users from an IT landscape access services in the cloud. In Azure AD, Microsoft provides tools that allow you to control and document access.
**"Zero Trust"** is a familiar buzzword here. In this blog series, we will take a look at what is important here and how identities can be protected, whether for standard users or for administrators.

## Whats the point here?

If users at the company site or from a remote office access services located in the local data center, the situation regarding trusted identities is relatively simple: the users are connected to the company network, whether devices are plugged directly into the network socket or connected to the WLAN. The same applies to access from outside, since a VPN is used here. In this context, the term perimeter network often appears. It describes a network area protected by a firewall. In theory, access to services there can be classified as secure and trustworthy.
The emphasis here is on "theory", because in practice administrators always have to deal with threats, whether internal or external. Thoxe must be secured in any case, regardless of where access is coming from. However, the topic comes into focus particularly in the cloud context, since access with initial authentication takes place via the Internet, which brings us directly to our topic.

## Ban everything first

This brings us back to the term "Zero Trust". This has been around for a long time and does not have anything to do exclusively with the cloud and public access to services there. Zero Trust is a strategic approach to restricting access and prohibiting everything for the time being. Every successful authentication and authorization is then linked to situational conditions in which, among other things, the user context is decisive. From where is the user trying to log in? With which device? To give just two examples. Microsoft describes "Zero Trust" as a journey that is permanently contested. It is not a concept that is implemented once. Rather, the challenge is to constantly put policies to the test, challenge them, and review the potential use of new features in Azure AD. A permanent cycle. A journey that never ends. A central component of "Zero Trust" is the handling of identities. In the following series, we will take a look at the functions that Microsoft provides in Azure AD in this regard so that the journey, to stay with the example, remains successful for you.



## The most strategic tools in the Identity related Zero Trust approach

Part of the blog series is my favourite collection of Azure Identity Technologies. The tool family is growing and Microsoft did a cool job with lots of tools and features around the Azure Identity portfolio. I wrote one article for each of the below technologies:

- Tenant Security
- MFA deployment
- Conditional Access
- Access Reviews
- Monitoring critical rolles and groups
- Passwordless


## Summarize

I have seen many articles around the Zero Trust topic in the Internet and also in the paper press. Why describe such technologies again?

It is like "driving a car" You can do this many ways: defensive or offensive! Being a beginner or an experienced driver! like this you can have a varied view to the Zero Trust topic. In that series I share my experiences from my projects and from my day to day use of that journey. 

