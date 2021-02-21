---
title: "Zero Trust in Azure Identity - Part 3: MFA! Is there a right way?"
date: 2021-01-16T14:59:57
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
- Zero Trust
- Hardening

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

## Is there a right way to implement MFA

MFA has become more prevalent with many providers on the Internet. This definitely also includes the Microsoft world and the logon to Azure AD or Microsoft 365. The distribution of MFA, or switching on when which user has to log on with a second factor in Azure AD, is linked to powerful policies. The topic as a whole has a multi-layered structure, and this is especially true for licensing, i.e. costs, in addition to the options for deployment. Here, unfortunately, as with other Azure features, the cost and capabilities depend on which Azure AD plan they are using. For example, the ability to use SMS as a times factor is not available in all editions. A good overview of all tariffs with the corresponding functionalities can be found in the following Microsoft Docs article (https://docs.microsoft.com/de-de/azure/active-directory/authentication/concept-mfa-licensing). At this point we are looking at the technology, primarily the provision of MFA.

## Good planning is important

The easiest way to get MFA to users is to do it statically. This no "ifs" and "buts" method can be found somewhat hidden in the Azure AD Portal, in the display of all users in the command bar at the top. This method also requires you to specify a CSV file as the source with the contents of the desired user accounts. You should think twice about this but rather antiquated method. In today's dynamic times, a rather smart method of distributing MFA is required, preferably if this can be tied to conditions. And there you have several options at hand. The most common, and the one recommended by Microsoft, is to enable it via "Conditional Access Policies". They offer many more options than controlling the distribution of MFA, MFA is only one part of it, but more on that later.

## Exploit the possibilities

If you have Identity Protection in place, you can define MFA as part of the logon risk policy. If a user logon risk is detected, you can react in several ways, one of them is to allow logon using MFA.
A typical case is, for example, a logon using the TOR browser, which hides the actual IP address, or when a logon is made from two different geographical locations, which is also atypical in normal cases. However, it is always possible that this is legitimate, for example when a developer is testing something, so the logon can be granted via MFA. Identity Protection can also be used to roll out MFA to all users by enabling the MFA registration policy in the Identity Protection Dashboard. Unlike the manual approach mentioned above, here it is possible to specify AD groups, which allows us to make the activation selective for specific users.