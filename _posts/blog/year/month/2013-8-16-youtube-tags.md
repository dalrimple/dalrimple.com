---  
title: Youtube. Y U No show tags in feed  
layout: post  
published: true  
tags: [hosting]  

---

I've been working on a mobile app that uses the Youtube Feed API to aggregate videos from various Youtube Channels. I wanted a convenient way to filter the results by asking the administrators of these channels to add **tags** to their Youtube videos.  
Buh-bow. Youtube says no.

Even through their API documentation says that you can search using custom tags: <https://developers.google.com/youtube/2.0/developers_guide_protocol_category_keyword_browsing>  
It appears that Youtube decided that the tags were being abused and not enough people were using them. So, they simply removed them <http://apiblog.youtube.com/2012/08/video-tags-just-for-uploaders.html>.

I can understand why the decision was made to remove them, but to not provide and alternative means of filtering API results, and leaving the official documentation up is incredibly frustrating.

So if you've got a similar requirement for your app your only options is to ask admins to put search terms in the video description. This is an unreliable and hacky solution. Thanks Youtube.

#####End rant
The tone of this article is probably unnecessarily short and sarcastic. But that's what happens when you spend 6 hours looking for why their service doesn't work as documented.