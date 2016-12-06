# Submitting a draft for SitePoint's Peer Review

This section will thoroughly teach you how to submit your article for Peer Review. It contains important information about what to consider before submitting.

### Markdown
We only accept drafts in a MarkDown (.md) file. If you are not familiar with MarkDown files, [here is a great resource to get you started.](http://www.markdowntutorial.com/)

The MD editor we recommend is [StackEdit](https://stackedit.io/editor) and [Dillinger](http://www.dillinger.io/). 

### Video: How to create a draft for Peer Review
Please watch this [video](https://www.youtube.com/watch?v=Iwo5hcqzX5k) on creating a draft for peer review.

### Submitting your draft
**Note:** If if you have not familiarized yourself with Github, please read this [tutorial](https://guides.github.com/activities/hello-world/) before proceeding. 

### Step by Step submission:
1. Fork the peer review repo you’ve joined. If you have a fork already, synchronize it with the original version (in case the original was updated with other people’s posts since you forked it, for example) as per this post. 
![Step 1](https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2015/06/1434739145peers-forking.gif)

2. Create a new branch for every article you intend to write – this is very important. Make sure every new branch is based off of the master branch of your fork. A common error is branching when already on another branch, which will cause your pull requests to be turned into a single pull request if you commit that way. All draft pull requests submitted on the `master` branch will be rejected.

3. If there is no folder matching your name yet under the Authors folder, please make one. Make it your full name, but remove local characters. For example, Bruno Škvorc will have the folder “Bruno Skvorc” or “Bruno-Skvorc”.
![Step 3](https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2015/06/1434742814peers-author-folder.gif)

4. Make a sub-folder for your post. Prefix the name with the number of posts in your folder. For example, if this is your first post in this repository, prefix with 01. For example, if your tutorial is called “How to set up ACL with Sentry in Laravel”, a good folder name is “01 – Sentry ACL in Laravel” and a bad name is “01 – sentrylar” 
![Step 4](https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2015/06/1434742805peers-article-folder.gif)

5. Inside that folder, put the draft in MarkDown format (the file name doesn’t matter as long as it ends in .md) and related images (if you wish to include any in the post).
![Step 5](https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2015/06/1434742797peers-article-draft.gif)

6. Commit the changes you have made, then push them to your fork on GitHub. Notice that we are pushing the branch we created, not the master:
```sh
git add .
git commit -m "My first article"
git push origin my-new-article
```
7. Send a [pull request](https://help.github.com/articles/about-pull-requests/).
(EMBED GIF - ‘SBS - STEP 3’)

**Multi-part articles:**
If you got approval from the editor to submit a multi-part post, then put each part in its own folder.
(ADD IN IMAGE - 'MULTI=PART ARTICLES - IMAGE')

**When submission is complete:**
Once a draft PR is submitted, it will be given a label of peer review:
(ADD IN IMAGE - AFTER SUBMISSION IMAGE 1)

It will then have to be in peer review mode for a specific amount of time or reviewed by a specific number of people before moving into editor review stage:
(ADD IN IMAGE - AFTER SUBMISSION IMAGE 2)

The duration and number of needed reviews will vary per channel. Wait for feedback from other authors, or for feedback from the channel editor and make the changes accordingly. 
