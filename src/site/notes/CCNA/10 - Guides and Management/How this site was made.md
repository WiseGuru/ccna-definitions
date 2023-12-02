---
{"dg-publish":true,"permalink":"/ccna/10-guides-and-management/how-this-site-was-made/"}
---

I published most of my CCNA notes using Ole's [GitHub - oleeskild/digitalgarden](https://github.com/oleeskild/digitalgarden) and [Cloudflare Pages](https://pages.cloudflare.com/). There are a couple of guides out there on this, but few of them actually solved my problems with Cloudflare specifically, so here you go!

>Here's a link to the guide I used initially to setup this site and others. It's a little chaotic and includes some incorrect information, but here it is for posterity: [How I Published My Knowledge Base Online for Free](https://sharaf.cc/40-49-toolbox/40-note-taking/40-01-obsidian/guides/publish-obsidian-vault-for-free/)

The *KEY* when publishing to Cloudflare is the **Build Configuration**. Specifically, set the "*Build command*" to `npm run build` and the "*Build output directory*" to `/dist`.

![How this site was made-1.png](/img/user/Attachments/How%20this%20site%20was%20made-1.png)

Anywhere, here you go:
## Steps to Publish Cloudflare (WIP)
1. Install the [Digital Garden plugin](obsidian://show-plugin?id=digitalgarden) on your [Obsidian app](https://obsidian.md/)
2. Create a GitHub account (if you don't already have one).
3. Create a Cloudflare account.
4. Go to [this repo](https://github.com/oleeskild/digitalgarden), click "*Use this Template*," and select "*Create a new repository*"
	1. ![How this site was made-4.png](/img/user/Attachments/How%20this%20site%20was%20made-4.png)
		1. **NOTE**: If you don't see the *Template* button, you may need to either maximize the page or zoom out.
5. Configure the new repo
	1. **Do not** check the box to "*Include all branches*"
	2. Enter a name and description for the repository
	3. Set the repository as *Public* or *Private*
		1. I don't think this should have any impact on the how the repo functions, since you give explicit permission to everything
	4. Example configuration:^[I definitely didn't fix the branches button in post.] 
	   ![How this site was made-20.png](/img/user/Attachments/How%20this%20site%20was%20made-20.png)
6. Create an access token to the Repo for Digital Garden^[Oleeskild's guide to create a [fine grained access token](https://dg-docs.ole.dev/advanced/fine-grained-access-token/)]
	1. Click on your profile icon at the top-right corner
	2. Select "*Settings*"
	3. In the left bar, select "*Developer Settings*"
	4. In the left bar, expand "*Personal access tokens*" and select "*Fine-grained tokens*"
	5. Click "*Generate new token*"
	6. Enter the following information:
		1. Main settings
			1. Token name
			2. Token expiration date
				1. Cannot go further than a year.
				2. Once a token expires, it will need to be regenerated.
				3. IIRC, you can just reactivate the token, but you may need to copy/paste the token back into the plugin.
		2. Repository Access
			1. "*Only select repositories*" and select the repository
		3. Repository Permissions
			1. *Contents*: Read and write
			2. *Pull Requests*: Read and write
	7. Generate token - **DO NOT EXIT THIS PAGE**
		1. This is the only time on GitHub that you will be able to see this token
		2. Feel free to save it to your preferred password manager or copy it right into the Obsidian plugin
7. Configure the Digital Garden plugin in Obsidian
	1. You may have to re-apply these settings after you configure Cloudflare
	2. Nothing here is hard and fast, but some observations I've made:
		1. I like turning almost all of the Features on
			1. Excluding Frontmatter, which can break the site
		2. Under appearance, I change the theme to match my current theme so I know what it will look like
		3. Set a site name
		4. Favicon needs to be an *svg* file and square
			1. If you update the Favicon after you create your site, you may need to purge your browser's cache before you will see it reflected
		5. WARNING: Add Timestamps to pages
			1. When I did this, it brought down CCNADefinitions, so I will need to experiment with another site until I can get it working.
	3. If you have any questions, check out the [Digital Garden guide](https://dg-docs.ole.dev/) or [join the Discord server](https://discord.gg/Z46n2RNX8e)
8. Create some content
	1. Set up a homepage and configure it to publish
	   ![How this site was made-10.png|250](/img/user/Attachments/How%20this%20site%20was%20made-10.png)
		1. You must have ONE homepage with a checkbox
		2. Every page you wish to publish must have this flag enabled 
	2. When ready, *Publish all notes* from the command pane
		1. ![How this site was made-11.png](/img/user/Attachments/How%20this%20site%20was%20made-11.png)
		2. **NOTE**: You can configure hotkeys to make publication easier.
			1. ![How this site was made-21.png](/img/user/Attachments/How%20this%20site%20was%20made-21.png)
1. Configure Cloudflare
	1. Log in to Cloudflare, expand the left menu bar, expand *Workers and Pages*, select *Overview*, and click *Create Application*
	   ![How this site was made-6.png](/img/user/Attachments/How%20this%20site%20was%20made-6.png)
	2. Connect it to your GIT account
	   ![How this site was made-7.png](/img/user/Attachments/How%20this%20site%20was%20made-7.png)
		1. NOTE: If you've done this before, you'll have to select "*Add account*" for the new repo to appear 
		   ![How this site was made-8.png|500](/img/user/Attachments/How%20this%20site%20was%20made-8.png)
	3. Configure the deployment 
	   ![How this site was made-9.png|500](/img/user/Attachments/How%20this%20site%20was%20made-9.png)
		1. Enter the project name (default is the Repo name)
		2. Set production branch to *Main*
		3. Leave the *Framework* preset as default or set to *Eleventy*
			1. I don't think this matters, as we immediately change the commands afterward
		4. Set the *Build command* to `npm run build`
		5. Set the *Build output directory* to `dist`
10. Configure Security and Dependency Updates in GitHub
	1. **NOTE**: If you apply updates through Dependabot, *Digital Garden* updates overwrite them, and you may be required to re-apply them. However, *it's better to be running patched* than unpatched, and *it's not that hard*.
	2. In the Repo, navigate to "*Settings*," *Code security and analysis*, and enable Dependabot *Alerts* and *Security Updates*
		1. ![How this site was made-12.png](/img/user/Attachments/How%20this%20site%20was%20made-12.png)
		2. When there is a dependency update or security issue, Dependabot will create a pull request, and Cloudflare will test the build in a preview to make sure it builds correctly.
			1. ![How this site was made-13.png](/img/user/Attachments/How%20this%20site%20was%20made-13.png)
		3. To merge the pull request, click the *green button above* and then click *confirm merge*
			1. ![How this site was made-14.png](/img/user/Attachments/How%20this%20site%20was%20made-14.png)
	3. **This is strongly recommended**; familiarize yourself with *Visual Studio Code*, Node.js, and *GitHub Desktop*^[What, you thought you were signing up for some free and easy way to upload your notes to the internet? Well with great power comes great security risks, and if you don't want some script kiddie owning your base, you should assume the people making free tools have overlooked something. Sometimes you gotta fix dependencies yourself for security updates, and boy howdy, knowing how these tools work is key]
		1. **This section will be updated later**
			1. Relevant: [Package.json vs Package-lock.json](https://www.atatus.com/blog/package-json-vs-package-lock-json/)
12. Add other security features
	1. From [your Cloudflare dashboard](https://dash.cloudflare.com), select your site. From the main panel or left column, choose:
		1. Quick Start Guide
			1. Click "*Review Settings*" in the *Quick Start Guide* pane
				1. ![How this site was made-15.png](/img/user/Attachments/How%20this%20site%20was%20made-15.png)
			2. Enable Automatic HTTPS rewrites
			3. Enable *Always Use HTTPS*
			4. Your choice whether to enable or disable Brotli compression; I couldn't find anything indicating it was insecure to use, and is apparently a [A Fast Alternative to GZIP Compression](https://kinsta.com/blog/brotli-compression/)
		2. SSL/TLS
			6. In the left column, select "*SSL/TLS*"
			7. Under "*Overview*", select "*Full (Strict)*"
				1. If you're squeamish, choose "*Full*"
				2. Because the whole site is hosted on Cloudflare, you shouldn't have to create any additional certificates
			8. Under "*Edge Certificates*"
				1. Enable "*HTTP Strict Transport Security (HSTS)*";^[[HSTS Preload List Submission](https://hstspreload.org)]^[[The HTTPS-Only Standard - HTTP Strict Transport Security](https://https.cio.gov/hsts/)] this brings up a big scary menu. Check the box and click *Next*, and choose the options in the following menu:
					1. Enable HSTS
					2. Max Age - 1 Year
						1. Required for *Preload*
					3. Enable Apply HSTS Policy to Subdomains
					4. Enable Preload
					5. Enable No-Sniff Header
						1. This prevents us from having to add it manually later on
				2. Set "*Minimum TLS Version*" to *TLS 1.3* (or minimum *TLS 1.2*)
					1. The default *TLS 1.0* is busted, and *TLS 1.1* was deprecated in 2021.
					2. *TLS 1.2* is less secure and slower than *1.3*, but you may have a use-case for needing it. However, that's unlikely for this kind of site.
		3. Security
			1. Security level: *Low* or *Medium*
				1. Choose what level of visitors should receive a *Challenge* (like a CAPTCHA or similar) if they are deemed sufficiently threatening
				2. Default is *Essentially Off*, and going from *Low* to *High* increases the likelihood of suspicious visitors getting prompted
				3. I would advocate *Medium* and doing some testing from different browsers, using a VPN, etc., and downgrading if you feel it's necessary
			2. Challenge Passage: *Your preference* (Default 30 minutes)
				1. If a suspicious visitor gets past the challenge, this dictates how frequently they are re-challenged
				2. *Default* is *30* *minutes*, and based on your testing for Security Level (e.g., if it trips when you're using a VPN), I would set the time period higher^[[Life of a Tor user : r/TOR](https://www.reddit.com/r/TOR/comments/187rfbh/life_of_a_tor_user/)]
	2. Headers
		1. Cloudflare allows you to install custom headers^[[Headers · Cloudflare Pages docs](https://developers.cloudflare.com/pages/platform/headers/)] into your site
			1. **This is critical**, as it can improve your site's security and reduce the likelihood of your visitors getting owned.
			2. **NOTE**: I anticipate these headers will get overwritten when the *Digital Garden* releases an update, so you will have to re-apply them each time.
				1. This re-application is made much easier if you use *Github Desktop* and *Visual Studio Code* as mentioned before
			3. You can check your site's headers and see ways to remediate security issues with [Analyze your HTTP response headers](https://securityheaders.com)
		2. To add security headers:
			1. Create a file called `_headers`^[Not `_headers.txt`, not `headers`, and for godsake not `TheseAreMySecurityHeadersForMyCloudflareSite.txt.xml.zip.tar.gz`] in the folder "/src/site"
				1. Enter the following code:
					1. 
<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



```
/*
  X-Frame-Options: SAMEORIGIN
  Permissions-Policy: document-domain=(self)
```

</div></div>

				2. If you run a [header security scan](https://securityheaders.com) against your site, you will get warnings about"*Content Security Policy (CSP)*", and you're screaming at my through your monitor "Oh Max, HOW could you have led me astray?!?" Instead, be thankful for the madness I spared you from.
					1. *Digital Garden* is absolutely **broken** when it comes to CSP
						2. Tons of on-page scripts make it effectively impossible to implement
						3. Additionally, there are tons of remotely-hosted scripts, and literally nothing I do works.
					2. Feel free to experiment with something like [Csper](https://csper.io/), though it's going to require constant maintenance whenever there's an update^[You can find additional CSP source values here: [CSP source values - HTTP | MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/Sources)]
						1. For reference, here was my "*CSP*" policy after several rounds. Note that just adding the domain should have worked, but I just could not get it working.
						2. ![How this site was made-19.png](/img/user/Attachments/How%20this%20site%20was%20made-19.png)
						3. If you use Csper^[[Chrome (CSP) Generator](https://chromewebstore.google.com/detail/content-security-policy-c/ahlnecfloencbkpfnpljbojmjkfgnmdc) and [Firefox (CSP) Generator](https://addons.mozilla.org/en-US/firefox/addon/csp-generator/)] to generate CSP code for your site, you will only have a 24-hour evaluation period before it's $50 a month *minimum*.
							1. And if you install the extension and add the CSP policy to your headers, you will need to make it all one line
							2. Also, add a `?v=1` to the end of the report-uri (like `endpoint.csper.io?v=1;`) to track changes in policy.
								1. This is important for when you try to update your code with Csper, and for some reason doesn't happen by default.
								2. Once added, it increments automatically.
			2. Modify the `.eleventy.js` file to add a passthrough for the `_headers` file
				1. `eleventyConfig.addPassthroughCopy("src/site/_headers");`
				2. ![How this site was made-18.png](/img/user/Attachments/How%20this%20site%20was%20made-18.png)
		3. To verify that your headers have been added, under "*Deployment Details*", you can click on the *Headers* tab and see what was added
			2. Successful addition of headers
				1. ![How this site was made-16.png](/img/user/Attachments/How%20this%20site%20was%20made-16.png)
			3. Failed addition of headers
				1. ![How this site was made-17.png](/img/user/Attachments/How%20this%20site%20was%20made-17.png)
		4. You can also go to [Security Header Scanner by Probely](https://securityheaders.com) to view your site's current headers
13. Troubleshooting
	1. You see a bunch of Failed deployments in Cloudflare to "Filetree"
		1. Make sure the *Main* branch is set as "Default" in GitHub







