---
title: "Writing and formating blogarticles!"
date: 2019-12-01T12:34:12-04:00
categories:
  - blog
tags:
---

You'll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

<!--Referenz einfach zweimal einfpgen,that's it-->
Overview of supported languages can be found here [here][SuppLanguages]

##Code Cighlighting

```posh
# VerifyMaxInactiveTime
If ($MaxInactiveTime -lt 1) { Write-Log -LogFile $Logfile -Message "The value specified for MaxInactiveTime must be greater than 0." -Console -LogLevel ERROR; Break }

# Check for existing Azure AD Connection
Try
{
	$TestAzureAD = Get-AzureADTenantDetail
}
Catch [Microsoft.Open.Azure.AD.CommonLibrary.AadNeedAuthenticationException]
{
	Write-Host "You're not connected.";
	Connect-AzureAD -credential $cred
}
```

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[SuppLanguages]: https://simpleit.rocks/ruby/jekyll/what-are-the-supported-language-highlighters-in-jekyll/